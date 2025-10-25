
The **MITRE ATT&CK Framework** is a **globally accessible knowledge base** of tactics, techniques, and procedures (TTPs) that adversaries use in real-world cyberattacks.

- Created by **MITRE**, a U.S. nonprofit that supports federal R&D.
    
- ATT&CK = **Adversarial Tactics, Techniques, and Common Knowledge**.
    
- Used as a reference for **threat intelligence, detection, defense, and red/blue team exercises**.
    

---

## 🔹 Core Structure

The framework is organized into a **matrix** of:

1. **Tactics (the “why”)**
    
    - Adversary’s **objectives or goals** during an attack (e.g., initial access, persistence, exfiltration).
        
    - Think of them as _categories of intent_.
        
    - Current enterprise matrix has **14 tactics** (from _Reconnaissance_ to _Impact_).
        
2. **Techniques (the “how”)**
    
    - **Specific methods** adversaries use to achieve a tactic.
        
    - Example: Under _Persistence_, techniques include _Account Manipulation_ or _Scheduled Tasks_.
        
3. **Sub-Techniques**
    
    - More granular descriptions of a given technique.
        
    - Example: _Phishing_ → _Spearphishing Link_ vs. _Spearphishing Attachment_.
        
4. **Procedures**
    
    - **Real-world implementations** of techniques, often tied to known threat groups or malware.
        

---

## 🔹 Why It Matters

- **Defenders (Blue Teams):** Map detections and defenses to known attacker behaviors.
    
- **Attackers/Red Teams:** Simulate realistic adversary behavior for testing defenses.
    
- **Threat Intelligence Analysts:** Attribute attacks and profile threat groups.
    
- **SOC/IR Teams:** Identify coverage gaps and strengthen response playbooks.
    

---

## 🔹 Example Flow

- **Tactic:** Initial Access
    
- **Technique:** Phishing
    
- **Sub-Technique:** Spearphishing Attachment
    
- **Procedure:** APT28 sends Word docs with malicious macros.
    

---

## 🔹 Key Uses

- Security assessments & purple teaming
    
- Threat hunting
    
- Gap analysis of security controls
    
- Mapping alerts/logs to adversary techniques