
#### Malware Behavior Catalogue (MBC)

- **Definition:** A catalogue of **malware objectives and behaviours** used for labeling, similarity analysis, and standardized reporting.
    
- **Relationship to MITRE ATT&CK:**
    
    - **MBC Objectives** ≈ **MITRE ATT&CK Tactics** (but tailored for malware analysis).
        
    - **MBC Behaviors** ≈ **ATT&CK Techniques** (document actions).
        
    - **MBC Methods** ≈ **ATT&CK Sub-Techniques** (specific ways behaviors are performed).
        
    - **Identifiers:** `[Bxxxx / Cxxxx / Exxxx]` tags unique to MBC.
        

---

#### Objectives

High-level malware goals (similar to **ATT&CK tactics**).

- **Anti-Behavioral Analysis** → evade sandbox/debugger.
    
- **Anti-Static Analysis** → hinder reverse engineering.
    
- **Collection** → gather info/data.
    
- **Command & Control** → maintain communication with attacker.
    
- **Credential Access** → steal usernames/passwords.
    
- **Defense Evasion** → bypass detection.
    
- **Discovery** → system/network reconnaissance.
    
- **Execution** → run malicious code/commands.
    
- **Exfiltration** → steal and extract data.
    
- **Impact** → disrupt/damage systems.
    
- **Lateral Movement** → spread through network.
    
- **Persistence** → remain on the system.
    
- **Privilege Escalation** → gain higher-level access.
    

---

#### Micro-Objectives

Smaller categories of behaviour (often not inherently malicious, but can be abused).

- **PROCESS** → creating/terminating processes, mutex checks.
    
- **MEMORY** → allocation, changing protections.
    
- **COMMUNICATION** → DNS, HTTP, SMTP, etc.
    
- **DATA** → encoding, compressing, string manipulation.
    

---

#### Behaviors (Examples)

- **VM Detection** [B0009] → checks if running in virtual environment.
    
- **Executable Code Obfuscation** [B0032] → hides code to hinder analysis.
    
- **Command Interpreter** [E1059] → abuse PowerShell, CMD, Bash, etc.
    
- **File & Directory Discovery** [E1083] → enumerate files/folders.
    
- **Obfuscated Files/Info** [E1027] → encode/encrypt to evade detection.
    

---

#### Micro-Behaviors (Low-level actions)

- **MEMORY → Allocate Memory** [C0007]
    
- **PROCESS → Create Process** [C0017]
    
- **COMMUNICATION → HTTP Communication** [C0002]
    
- **DATA → Check String** [C0019]
    
- **DATA → Encode Data (Base64, XOR)** [C0026]
    
- **FILE SYSTEM → Create Directory [C0046], Delete File [C0047], Read File [C0051], Write File [C0052]**
    

---

#### Methods (Sub-techniques)

Detail how a behaviour is implemented.

- **Executable Code Obfuscation**
    
    - Argument Obfuscation [B0032.020]
        
    - Stack Strings [B0032.017]
        
- **HTTP Communication**
    
    - Read Header [C0002.014]
        
- **Encode Data**
    
    - Base64 [C0026.001]
        
    - XOR [C0026.002]
        
- **Obfuscated Files**
    
    - Encoding using standard algorithm [E1027.m02]
        

---

#### Example Recap (From CAPA Result)

- **Objective:** DATA
    
- **Behavior:** Encode Data
    
- **Method:** Base64
    
- **Identifier:** C0026.001  
    ➡ Malware is capable of encoding data with Base64.
    

---

#### Q&A

**Q1:** What serves as a catalogue of malware objectives and behaviours?  
**A1:** Malware Behavior Catalogue (MBC)

**Q2:** Which field is based on ATT&CK tactics in malware behaviour?  
**A2:** Objective

**Q3:** Identifier of “Create Process” micro-behavior?  
**A3:** C0017

**Q4:** What is the behaviour with Identifier B0009?  
**A4:** Virtual Machine Detection

**Q5:** Malware can obfuscate data using Base64/XOR. What is the related micro-behavior?  
**A5:** Encode Data

**Q6:** Which micro-behavior refers to “Malware is capable of initiating HTTP communications”?  
**A6:** HTTP Communication