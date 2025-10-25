
#### 🔧 Tool Overview
---
- **Volatility 3**
    
    - A memory forensics framework.

    - Extracts **artifacts** (processes, files, DLLs, command lines, injected code, etc.) from memory images.

    - Useful in malware cases (like ransomware Wcry).

    - Preprocessing = run multiple plugins and save outputs for later analysis.
        

---

#### 📌 File Under Analysis
---
- **Memory image:** `wcry.mem`
    
- **Directory:** `/home/ubuntu/Desktop/tasks/Wcry_memory_image/`
    
- **Command base:**
    
    `vol3 -f wcry.mem <plugin>`
    

---

#### 🔍 Key Plugins (Windows)
---
- **`windows.pstree.PsTree`** → Lists processes in a tree by parent PID.
    
- **`windows.pslist.PsList`** → Lists all active processes.
    
- **`windows.cmdline.CmdLine`** → Lists command-line arguments of processes.
    
- **`windows.filescan.FileScan`** → Scans memory for file objects (open/closed).
    
- **`windows.dlllist.DllList`** → Lists DLLs (loaded modules) in processes.
    
- **`windows.psscan.PsScan`** → Scans for processes in memory (even hidden/unlinked).
    
- **`windows.malfind.Malfind`** → Identifies process memory regions with potential injected code.
    

---

#### 🖥️ Example Usage
---
`vol3 -f wcry.mem windows.pstree.PsTree vol3 -f wcry.mem windows.pslist.PsList vol3 -f wcry.mem windows.cmdline.CmdLine vol3 -f wcry.mem windows.filescan.FileScan vol3 -f wcry.mem windows.dlllist.DllList vol3 -f wcry.mem windows.psscan.PsScan vol3 -f wcry.mem windows.malfind.Malfind`

---

#### ⚡ Preprocessing in Bulk (Loop)
----
Instead of running each plugin manually, use a loop:

`for plugin in windows.malfind.Malfind windows.psscan.PsScan windows.pstree.PsTree \ windows.pslist.PsList windows.cmdline.CmdLine windows.filescan.FileScan \ windows.dlllist.DllList; \ do vol3 -q -f wcry.mem $plugin > wcry.$plugin.txt; done`

**Breakdown:**

- `for plugin in ...` → Iterates through listed plugins.
    
- `-q` → Quiet mode (suppresses progress output).
    
- `> wcry.$plugin.txt` → Redirects output to file, naming convention: `wcry.<plugin>.txt`.
    
- **Result:** 7 text files created, one for each plugin.
    

---

#### 📝 Preprocessing with Strings
---
Extract human-readable text from memory (helps find URLs, commands, malware names).

`# ASCII strings strings wcry.mem > wcry.strings.ascii.txt    # 16-bit Little Endian Unicode strings -e l wcry.mem > wcry.strings.unicode_little_endian.txt    # 16-bit Big Endian Unicode strings -e b wcry.mem > wcry.strings.unicode_big_endian.txt`  

- **`strings`** → Extracts ASCII text.
    
- **`-e l`** → Extracts UTF-16 little endian text.
    
- **`-e b`** → Extracts UTF-16 big endian text.
    
- Output = 3 text files.
    

---

#### 📂 Practical Findings (Wcry Case)
-----
- **Malfind plugin:**
    
    - 1st process with suspected injected code → **`csrss.exe`**
        
    - 2nd process → **`winlogon.exe`**
        
- **DllList plugin:**
    
    - Detected ransomware binary → **`@WanaDecryptor@.exe`**
        
    - File path: `C:\Intel\ivecuqmanpnirkt615`
        

---

#### 📝 Q&A Review
---
- Plugin listing processes in a tree by parent PID? → **PsTree**
    
- Plugin listing all active processes? → **PsList**
    
- Linux utility extracting ASCII + Unicode strings? → **strings**
    
- First process flagged by Malfind? → **csrss.exe**
    
- Second process flagged by Malfind? → **winlogon.exe**
    
- File path of `@WanaDecryptor@.exe`? → **C:\Intel\ivecuqmanpnirkt615**
    

---

## 🧾 Cheat-Sheet Summary
-----
- **Volatility base command:**
    
    `vol3 -f <image> <plugin>`
    
- **Common Plugins:**
    
    - `PsTree` → process tree
        
    - `PsList` → active processes
        
    - `PsScan` → hidden processes
        
    - `CmdLine` → command line args
        
    - `DllList` → loaded DLLs
        
    - `FileScan` → file handles
        
    - `Malfind` → injected code
        
- **Bulk Processing:**
    
    `for plugin in <list>; do vol3 -q -f <image> $plugin > <image>.$plugin.txt; done`
    
- **Strings Extraction:**
    
    `strings file > ascii.txt strings -e l file > unicode_little.txt strings -e b file > unicode_big.txt`
    
