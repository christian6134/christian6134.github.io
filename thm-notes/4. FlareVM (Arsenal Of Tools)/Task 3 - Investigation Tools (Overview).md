
## 🛠️ Commonly Used Tools for Investigation

---

#### 📋 Tool Overview

|Tool|Investigative Value|
|---|---|
|**Procmon**|Tracks real-time system activity (file, registry, threads) — useful in malware research & forensics.|
|**Process Explorer**|Shows parent/child process relationships, loaded DLLs, and executable paths.|
|**HxD**|Hex editor for raw file/memory/disk inspection, useful for identifying executable headers.|
|**Wireshark**|Captures and analyzes network traffic, spotting suspicious connections.|
|**CFF Explorer**|Generates file hashes, inspects Portable Executable (PE) headers, validates system files.|
|**PEStudio**|Static analysis of executable properties without running them (safe pre-execution analysis).|
|**FLOSS**|Extracts & de-obfuscates strings from malware using advanced static analysis.|

---

#### 🔎 Process Monitor (Procmon)

- **Purpose:**
    
    - Records **real-time system activity**:
        
        - File system reads/writes
            
        - Registry queries/modifications
            
        - Thread & process actions
            
- **Investigative Use:**
    
    - Track malware behavior in action.
        
    - Detect **credential dumping attempts** (e.g., `lsass.exe` targeted by **Mimikatz**).
        
    - Look for unusual access to system processes.
        
- **Example:**
    
    - Filtered view on `lsass.exe`.
        
    - Shows it accessing `lsasrv.dll` (legit).
        
    - Suspicious if **foreign process** attempts memory access.
        

---

#### 🔎 Process Explorer (Procexp)

- **Purpose:**
    
    - Advanced Task Manager.
        
    - Displays running processes, parent-child hierarchy, and user context.
        
    - Identifies DLLs loaded by a process.
        
- **Investigative Use:**
    
    - Verify **process lineage** (e.g., Word doc spawning PowerShell → suspicious).
        
    - Validate PID and executable path.
        
    - Detect unusual spawns (e.g., `.lnk`, `.iso` dropping malware).
        
- **Example:**
    
    - Used to confirm **CFF Explorer** app process.
        
    - Shows **parent process**, confirming execution chain.
        

---

#### 🔎 HxD (Hex Editor)

- **Purpose:**
    
    - Directly view/edit raw file, memory, or disk bytes.
        
    - Supports searching, comparison, and data interpretation.
        
- **Investigative Use:**
    
    - Identify **file headers** (magic numbers).
        
    - Examine suspicious file structure.
        
    - Check for corruption or embedded payloads.
        
- **Example:**
    
    - File `possible_medusa.txt` opened.
        
    - Starts with `4D 5A` → indicates a **Windows executable (MZ header)**.
        
    - Data Inspector helps interpret values as int/float/etc.
        

---

#### 🔎 CFF Explorer

- **Purpose:**
    
    - Inspects PE (Portable Executable) files.
        
    - Generates **hashes (MD5, SHA-1, SHA-256)**.
        
    - Validates system file integrity.
        
- **Investigative Use:**
    
    - Confirm file authenticity.
        
    - Detect tampering (malicious injections in legit system files).
        
    - Compare hashes against threat intelligence feeds.
        
- **Example:**
    
    - File: `cryptominer.bin`
        
    - Type: **64-bit Portable Executable**
        
    - Built: **Sept 23, 2024**
        
    - Verified via hashes → integrity checks.
        

---

#### 🔎 Wireshark

- **Purpose:**
    
    - Network traffic capture and analysis.
        
    - Shows protocol, source, destination, ports.
        
- **Investigative Use:**
    
    - Detect **C2 (command & control)** traffic.
        
    - Spot suspicious encryption (e.g., TLS used by malware to hide comms).
        
    - Analyze exfiltration attempts.
        
- **Example:**
    
    - Captured packets show:
        
        - **Protocol:** TLSv1.2 over TCP
            
        - **Info:** Encrypted transmission
            
    - Encrypted payload may mask malicious behavior.
        

---

#### 🔎 PEStudio

- **Purpose:**
    
    - **Static executable analysis** — no execution required.
        
    - Extracts metadata, imports, libraries, entropy.
        
- **Investigative Use:**
    
    - Safe inspection of malware samples.
        
    - Spot **suspicious imports** (e.g., `VirtualAlloc`, `CreateRemoteThread`).
        
    - High entropy → likely packed/encrypted file.
        
- **Example:**
    
    - File: `PsExec.exe` (dual-use tool).
        
    - **Entropy:** 6.596 (possible packing/encryption).
        
    - Built with Visual C++ 8.
        
    - Commonly abused for **lateral movement** in attacks.
        

---

#### 🔎 FLOSS (FireEye Labs Obfuscated String Solver)

- **Purpose:**
    
    - Extracts **obfuscated & hidden strings** from binaries.
        
    - Improves upon `strings.exe`.
        
    - Supports integration with reverse engineering tools (IDA Pro, Binary Ninja).
        
- **Investigative Use:**
    
    - Reveals hidden configs:
        
        - Hardcoded **IP addresses**
            
        - **C2 domains**
            
        - Registry keys, encryption keys
            
        - Error messages
            
    - Detects obfuscation patterns.
        
- **Example:**
    
    `floss .\cobaltstrike.exe`
    
    - Extracted **189 static strings** (file paths, API calls, URLs).
        
    - No dynamic decoded strings (suggests runtime obfuscation).
        
    - Indicates **Cobalt Strike beacon** likely present.
        

---

## 🧾 Cheat-Sheet Summary

- **Procmon** → Monitor live system activity (registry, file, threads).
    
- **Procexp** → Parent-child processes, DLLs, execution tree.
    
- **HxD** → Hex-level file/memory inspection, magic bytes.
    
- **CFF Explorer** → File hashes, PE header inspection.
    
- **Wireshark** → Capture/analyze network traffic, detect C2.
    
- **PEStudio** → Static analysis (metadata, entropy, imports).
    
- **FLOSS** → Extract/de-obfuscate malware strings.