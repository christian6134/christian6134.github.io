
#### CAPA: Capability & Namespace

- **Capability** → What the malware can do (e.g., “reference anti-VM strings”).
    
- **Namespace** → Where that capability belongs in CAPA’s rule hierarchy.
    
- **Format:**
    
    `Capability :: Top-Level Namespace (TLN) / Namespace`
    
    Example:  
    `reference anti-VM strings :: anti-analysis/anti-vm/vm-detection`
    

---

#### Namespaces Overview

Namespaces group related rules to help analysts quickly map behaviours.

**Top-Level Namespaces (TLN):**

- **anti-analysis** → Detects malware behaviours that try to evade analysis (e.g., obfuscation, anti-debugging, VM detection).
    
- **collection** → Rules about gathering system/user data for exfiltration.
    
- **communication** → Rules about network activity (HTTP, DNS, C2).
    
- **compiler** → Recognize build environments or compilers used.
    
- **data-manipulation** → Actions that transform data (e.g., encoding, encryption).
    
- **executable** → Rules related to PE sections or executable attributes.
    
- **host-interaction** → Malware interacting with host system (file creation, process injection).
    
- **impact** → Potential harm malware can cause (e.g., ransomware, cryptocurrency mining).
    
- **persistence** → How malware maintains long-term access.
    
- **linking** → Linking to external libraries or APIs.
    
- **load-code** → Injecting or dynamically loading code at runtime.
    
- **malware-family** → Behaviours unique to specific malware families.
    
- **nursery** → Staging ground for rules still being developed.
    
- **runtime** → Rules identifying the runtime/language.
    
- **targeting** → Special targeting cases (e.g., ATMs).
    

---

#### Example Breakdown (Anti-Analysis TLN)

- **Namespace:** `anti-vm/vm-detection`
    
    - Detects VM environments (VMware strings, registry keys, VirtualBox markers).
        
    - Rules: `reference-anti-vm-strings-targeting-virtualbox.yml`, etc.
        
- **Namespace:** `obfuscation`
    
    - Covers techniques like String Encryption, Packing, Code Obfuscation.
        
    - Rules: `obfuscated-with-dotfuscator.yml`, `obfuscated-with-smartassembly.yml`.
        

➡ **Relationship:**  
Think of **TLN as ATT&CK tactics** (big goals), and **Namespaces as ATT&CK techniques** (specific methods). Rules inside are like **sub-techniques**.

---

#### Why Namespaces Matter

- They let analysts map **Capabilities → Namespace → TLN** to see how malware achieves its objectives.
    
- For example:
    
    - **Capability:** encode data using XOR
        
    - **Namespace:** data-manipulation/encoding/xor
        
    - **TLN:** data-manipulation
        
    - **Meaning:** Malware is manipulating data to conceal its true purpose.
        

---

#### Q&A

**Q1:** Which TLN detects behaviours like obfuscation, packing, and anti-debugging?  
**A1:** `anti-analysis`

**Q2:** Which namespace detects VM environments?  
**A2:** `anti-vm/vm-detection`

**Q3:** Which TLN focuses on maintaining persistence in compromised systems?  
**A3:** `persistence`

**Q4:** Which namespace covers String Encryption, Code Obfuscation, Packing, and Anti-Debugging tricks?  
**A4:** `obfuscation`

**Q5:** Which TLN is a staging ground for unfinished rules?  
**A5:** `nursery`