
#### File Information

- **Hashes:** Used to uniquely identify the file.
    
    - **md5:** 3b9d26d2e7433749f2c32edb13a2b0a2
        
    - **sha1:** 969437df8f4ad08542ce8fc9831fc49a7765b7c5
        
    - **sha256:** ae7bc6b6f6ecb206a7b957e4bb86e0d11845c5b2d9f7a00a482bef63b567ce4c
        
- **analysis:** `static` → CAPA looked at the binary without execution.
    
- **os:** `windows` → context for capabilities.
    
- **format:** `pe` → Portable Executable file.
    
- **arch:** `i386` → 32-bit architecture.
    
- **path:** location of the file analyzed.
    

---

#### MITRE ATT&CK

- **Definition:** Global framework documenting adversary tactics, techniques, and procedures (TTPs). CAPA maps file behaviour to MITRE techniques.
    
- **Format Example:**
    
    - **Tactic** = high-level attacker goal (e.g., Defense Evasion).
        
    - **Technique** = method (e.g., Obfuscated Files).
        
    - **Sub-Technique** = more specific method (e.g., Indicator Removal).
        
    - **Identifier** = Txxxx ID.
        

**Findings in cryptbot.bin:**

- **Defense Evasion**
    
    - Obfuscated Files [T1027]
        
    - Indicator Removal from Tools [T1027.005]
        
    - VM/Sandbox Evasion: System Checks [T1497.001]
        
- **Discovery**
    
    - File & Directory Discovery [T1083]
        
- **Execution**
    
    - PowerShell [T1059.001]
        
    - Shared Modules [T1129]
        
- **Impact**
    
    - Resource Hijacking [T1496]
        
- **Persistence**
    
    - Scheduled Task via `at` [T1053.002]
        
    - Scheduled Task [T1053.005]
        

---

#### MAEC (Malware Attribute Enumeration and Characterization)

- **Definition:** Standard language for describing malware attributes and behaviours. Helps analysts compare and track malware.
    
- **CAPA Output:**
    
    - **Category:** malware-category
        
    - **Value:** `launcher`
        

**Common Values:**

- **Launcher** → behaves like a dropper/activator:
    
    - Drops extra payloads
        
    - Activates persistence mechanisms
        
    - Connects to C2 servers
        
    - Executes functions
        
- **Downloader** → focuses on fetching resources:
    
    - Downloads payloads/configs
        
    - Pulls updates
        
    - Executes secondary stages
        

---

#### Questions & Answers

**Q1:** What is the sha256 of cryptbot.bin?  
**A1:** `ae7bc6b6f6ecb206a7b957e4bb86e0d11845c5b2d9f7a00a482bef63b567ce4c`

**Q2:** What is the Technique Identifier of Obfuscated Files or Information?  
**A2:** `T1027`

**Q3:** What is the Sub-Technique Identifier of Indicator Removal from Tools?  
**A3:** `T1027.005`

**Q4:** Which MAEC value shows persistence behaviour?  
**A4:** `Launcher`

**Q5:** Which MAEC value shows downloading payloads/resources?  
**A5:** `Downloader`