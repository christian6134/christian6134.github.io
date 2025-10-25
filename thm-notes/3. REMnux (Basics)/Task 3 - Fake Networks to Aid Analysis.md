
#### 🔧 Tool Overview

- **INetSim (Internet Services Simulation Suite)**
    
    - Simulates common internet services (DNS, HTTP/S, FTP, SMTP, etc.).
        
    - Provides a **controlled “fake internet”** environment.
        
    - Used in **dynamic malware analysis** to safely observe network behavior.
        
    - Logs **connections, requests, and downloads** malware attempts to make.
        

---

#### 📌 Lab Setup

- **Machines Used:**
    
    - **REMnux VM** → Runs INetSim (fake internet).
        
    - **AttackBox VM** → Simulates malware behavior (makes network calls).
        
- **Step 1: Get REMnux IP**
    
    `ifconfig`
    
    Note: IP shown after `ubuntu@`.
    
- **Step 2: Configure INetSim**
    
    `sudo nano /etc/inetsim/inetsim.conf`
    
    - Find:
        
        `#dns_default_ip 0.0.0.0`
        
    - Change to machine’s IP (uncomment line):
        
        `dns_default_ip  MACHINE_IP`
        
- **Step 3: Verify config change**
    
    `cat /etc/inetsim/inetsim.conf | grep dns_default_ip`
    
    Should show:
    
    `dns_default_ip  MACHINE_IP`
    
- **Step 4: Start INetSim**
    
    `sudo inetsim`
    
    Must see:
    
    `Simulation running.`
    

---

#### 🌍 AttackBox Interaction

- From **AttackBox browser**, visit:
    
    `https://MACHINE_IP`
    
    - Accept risk → redirected to INetSim homepage.
        
- **Simulating malware download:**
    
    `sudo wget https://MACHINE_IP/second_payload.zip --no-check-certificate sudo wget https://MACHINE_IP/second_payload.ps1 --no-check-certificate`
    
    - Files saved in working directory.
        
    - All are fake placeholders (open safely).
        

---

#### 📑 Connection Report

- Stop INetSim → generates log report.
    
- Default path: `/var/log/inetsim/report/`
    
- Example:
    
    `sudo cat /var/log/inetsim/report/report.2594.txt`
    
- **Sample log content:**
    
    `HTTPS connection, method: GET, URL: https://MACHINE_IP/, file name: /var/lib/inetsim/http/fakefiles/sample.html HTTPS connection, method: GET, URL: https://MACHINE_IP/test.exe, file name: /var/lib/inetsim/http/fakefiles/sample_gui.exe HTTPS connection, method: GET, URL: https://MACHINE_IP/second_payload.ps1, file name: /var/lib/inetsim/http/fakefiles/sample.html HTTPS connection, method: GET, URL: https://MACHINE_IP/second_payload.zip, file name: /var/lib/inetsim/http/fakefiles/sample.html`
    
- Logs show:
    
    - Protocol (HTTPS)
        
    - Method (GET/POST)
        
    - Requested URL
        
    - Fake file delivered
        

---

#### 📝 Q&A Review

- **Flag download:**
    
    `sudo wget https://MACHINE_IP/flag.txt --no-check-certificate`
    
    **Flag:** `Tryhackme{remnux_edition}` ✅
    
- **Report check:**
    
    - URL method used to get `flag.txt`: **GET**
        

---

## 🧾 Cheat-Sheet Summary

- **Config INetSim:**
    
    - Edit `/etc/inetsim/inetsim.conf` → set `dns_default_ip MACHINE_IP`
        
    - Start with: `sudo inetsim`
        
- **Test from AttackBox:**
    
    - Visit `https://MACHINE_IP` in browser.
        
    - Use `wget` to simulate downloads.
        
- **Reports:**
    
    - Location: `/var/log/inetsim/report/`
        
    - Shows URL, method, and fake file served.
        
- **Key Q&A:**
    
    - Flag: `Tryhackme{remnux_edition}`
        
    - URL Method for flag retrieval: **GET**