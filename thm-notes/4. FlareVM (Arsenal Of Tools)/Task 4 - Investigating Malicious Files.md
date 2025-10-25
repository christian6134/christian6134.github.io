
### 1. **PEStudio → Static Analysis**

**What it does:**

- Inspects executable properties **without running them** (safe).
    
- Reveals metadata, entropy, imports, manifests, version info, etc.
    

**Why it’s used first:**

- Establishes an initial baseline:
    
    - File hash → compare with VirusTotal.
        
    - Entropy → detect packing/obfuscation.
        
    - Imports → see what functions malware _might_ use.
        

**What we found:**

- **Entropy:** `7.999` → almost max → suggests packed or encrypted.
    
- **Manifest:** `requireAdministrator` → malware wants elevated privileges.
    
- **Imports:**
    
    - `set_UseShellExecute` → spawn child processes.
        
    - `RijndaelManaged` → AES cryptography → could mean file encryption or C2 traffic.
        
- **Suspicious metadata:** Russian text, fake “Registry Editor” label.
    

➡ **Takeaway:** This binary is **not normal software** — it’s disguised, possibly packed, and requests admin rights. Static red flags raised.

---

### 2. **FLOSS → String Extraction**

**What it does:**

- Pulls **hardcoded or obfuscated strings** from executables.
    
- Can reveal: file paths, IPs, C2 domains, registry keys, commands.
    

**Why it follows PEStudio:**

- Validates what PEStudio showed (API imports, suspicious functions).
    
- Provides **human-readable indicators** to pivot on.
    

**What we found:**

- Strings confirming **Crypto functions** (AES, decryption routines).
    
- Matches with PEStudio’s import table (consistency check).
    
- Warning: `.NET` support is limited → not all strings extracted.
    

➡ **Takeaway:** Confirms malware is built with cryptography in mind. Prepares us to watch for **encrypted traffic** during dynamic analysis.

---

### 3. **Process Explorer → Runtime Process Analysis**

**What it does:**

- Shows live processes with **parent-child relationships**.
    
- Lets you check **network connections per process**.
    

**Why it’s important:**

- Malware often spawns from parent apps (Word, Explorer).
    
- Network tab shows **real connections in real time**.
    

**What we found (cobaltstrike.exe):**

- Parent process: `explorer.exe` → user double-clicked it.
    
- Child process: `cobaltstrike.exe`.
    
- **TCP/IP tab:** connected to IP `47.120.46.210` on **port 81**.
    

➡ **Takeaway:** Malware establishes outbound C2 connection immediately. This aligns with cobaltstrike’s behavior (beaconing).

---

### 4. **Procmon (Process Monitor) → Deep Event Tracing**

**What it does:**

- Monitors **system-wide events** (registry, file, network, threads).
    
- Captures far more granular info than Process Explorer.
    

**Why we use it after Procexp:**

- Process Explorer gives a snapshot; Procmon gives **full trace logs**.
    
- Useful for verification and deeper inspection.
    

**Workflow:**

- Filtered by process name (`cobaltstrike.exe`).
    
- Captured network requests confirming connection to **47.120.46.210:81**.
    

➡ **Takeaway:** Verified suspicious network activity independently. **Two tools agreeing → high confidence.**

---

### 🔗 Workflow Summary

1. **PEStudio (static)** → Is file suspicious before execution? (Entropy, metadata, imports).
    
2. **FLOSS (static)** → What hardcoded clues are inside? (Strings, configs, crypto calls).
    
3. **Process Explorer (dynamic)** → How does it behave when launched? (Parent process, network connections).
    
4. **Procmon (dynamic + verification)** → Confirm details with system-level tracing.
    

---

### 📊 Case Study Answers in Context

- **Entropy of windows.exe:** `7.999` → Packed/obfuscated.
    
- **Manifest (requestedExecutionLevel):** `requireAdministrator` → Needs admin rights.
    
- **Function to spawn processes:** `set_UseShellExecute`.
    
- **Crypto API used:** `RijndaelManaged`.
    
- **Imphash of cobaltstrike.exe:** `92EEF189FB188C541CBD83AC8BA4ACF5`.
    
- **Defanged C2 IP:** `47[.]120[.]46[.]210`.
    
- **Destination port:** `81`.
    
- **Parent process:** `explorer.exe`.
    

---

### 🧾 Big Picture Takeaway

- **Static tools (PEStudio, FLOSS):** Safe, quick intel → "Is this suspicious? What does it claim to do?"
    
- **Dynamic tools (Procexp, Procmon):** Real-time behavior → "What does it actually do when executed?"
    
- **Cross-verification:** Use more than one tool to **increase confidence** and reduce false positives.