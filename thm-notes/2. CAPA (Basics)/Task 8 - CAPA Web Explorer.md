
#### CAPA Rule Matching with `-vv`

- CAPA by default shows **high-level capabilities** (e.g., “schedule task via schtasks”).
    
- If you run with **`-vv` (very verbose)**, you see **every match condition** that triggered a capability, including:
    
    - Exact strings (regex matches like `/VMWare/i`)
        
    - API calls (e.g., `RegQueryValueEx`)
        
    - Nested logical conditions (AND/OR groups).
        
- Problem: this produces **thousands of lines** → difficult to read in terminal or text editor.
    

➡ Solution: output results in **JSON format** using `-j`.

`capa.exe -j -vv .\cryptbot.bin > cryptbot_vv.json`

This JSON can then be explored visually instead of scrolling raw text.

---

#### CAPA Web Explorer

- **Tool:** Web-based viewer for CAPA JSON files.
    
- Available online **and** offline (HTML file on the VM desktop).
    
- **Why it’s useful:**
    
    - Converts thousands of lines into a **clickable, searchable UI**.
        
    - Lets analysts drill down into rules → see which _features_ were matched.
        
    - Provides filtering and a **Global Search Box** for quick navigation.
        
- **Benefit for analysis:** You can instantly answer _why_ a rule fired instead of digging manually in text.
    

---

#### Example 1: Anti-VM Strings (VMWare)

- **Capability:** `reference anti-VM strings targeting VMWare`
    
- **Rule YAML:** `reference-anti-vm-strings-targeting-vmware.yml`
    
- **Matched Feature:**
    
    `string: /VMWare/i`
    
- **Interpretation:** Malware contains VMWare-related strings (registry keys, process names, or tools).
    
- **Meaning:** Likely anti-analysis → malware checking if it’s inside a VM before executing.
    

---

#### Example 2: Scheduled Task via schtasks

- **Capability:** `schedule task via schtasks`
    
- **Rule YAML:** `schedule-task-via-schtasks.yml`
    
- **Matched Features:**
    
    `string: /schtasks/i string: /\/create /i`
    
- **Interpretation:** These are command-line arguments that Windows malware often uses to register itself as a **scheduled task**.
    
- **MITRE Mapping:** Persistence → `T1053.005 (Scheduled Task/Job: Scheduled Task)`.
    
- **Meaning:** Malware is trying to maintain persistence by ensuring execution at specific intervals or reboots.
    

---

#### Why This Matters for Analysts

- **Raw capabilities** tell you _what_ the malware might do.
    
- **Very verbose output** + Web Explorer tell you _why CAPA thinks so_.
    
- This helps analysts:
    
    - Validate matches (reduce false positives).
        
    - See **exact artifacts** malware relies on (strings, APIs).
        
    - Map behaviour back to ATT&CK or MBC frameworks for reporting.
        

Think of it as going from _“Malware might create a scheduled task”_ → _“Confirmed: it references schtasks.exe with the /create flag”_.

---

#### Q&A

**Q1:** Which parameter outputs CAPA results into JSON?  
**A1:** `-j`

**Q2:** What tool allows interactive exploration of CAPA results?  
**A2:** CAPA Web Explorer

**Q3:** Which feature of CAPA Web Explorer allows filtering and quick searching?  
**A3:** Global Search Box

---

✅ With `-vv` + `-j` → CAPA Web Explorer, you move from **surface-level detection** to **deep validation of features**.