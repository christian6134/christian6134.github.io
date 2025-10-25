#### How CAPA Maps Capabilities

- **Capability**: The rule name that matched (what the sample _did_).
    
- **Namespace**: Where that rule lives: `TLN / namespace/subnamespace`.
    
- **Rule YAML**: File whose logic matched; **Capability name ≈ rule name** (spaces → dashes).
    

Example:  
`reference anti-VM strings :: anti-analysis/anti-vm/vm-detection`  
→ Rule: `reference-anti-vm-strings.yml`

---

#### Common TLNs (Top-Level Namespaces)

- **anti-analysis**: Obfuscation, anti-debug, VM checks.
    
- **communication**: HTTP/DNS/C2 behaviors.
    
- **data-manipulation**: Encoding/encryption (e.g., Base64, XOR).
    
- **host-interaction**: Files, processes, memory, TLS.
    
- **persistence**: Scheduled tasks, autoruns.
    
- **linking / load-code**: Dynamic linking, PE parsing, PowerShell.
    
- **impact**: Outcomes (e.g., crypto strings) — sometimes rules live in **nursery** (staging).
    

---

#### Worked Examples

- **“reference anti-VM strings”** → TLN: **anti-analysis** → NS: **anti-vm/vm-detection** → Rule: `reference-anti-vm-strings.yml`  
    Meaning: Looks for VM artifacts (evasion).
    
- **“schedule task via schtasks”** → TLN: **persistence** → NS: **scheduled-tasks** → Rule: `schedule-task-via-schtasks.yml`  
    Meaning: Windows persistence via scheduled task.
    

---

#### Quick Recap (Base64)

- **Capability**: `reference Base64 string`
    
- **TLN**: `data-manipulation`
    
- **Namespace**: `encoding/base64`
    
- **Rule**: `reference-base64-string.yml`
    
- **Meaning**: The file can use Base64 encoding.
    

---

### Q&A

**1) What rule yaml file was matched for “check HTTP status code”?**  
`check-http-status-code.yml`

**2) What is the Capability name for `reference-anti-vm-strings.yml`?**  
`reference anti-VM strings`

**3) Which TLN includes the Capability “run PowerShell expression”?**  
`load-code`

**4) In `check-for-windows-sandbox-via-registry.yml`, which API ending with “Ex” is it looking for?**  
`RegQueryValueEx`