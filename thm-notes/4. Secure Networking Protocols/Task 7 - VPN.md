
**Virtual Private Network (VPN)**
----------------------
**Scenario:** Company with offices in different geographical locations. Can this company **connect all its offices and sites to the main branch** so that any device can access the shared resources as if physically located in the main branch?
- Focus: Virtual (V)


**Scenario:** What mechanism is in place to ensure that all data leaving or entering a computer is protected from **disclosure or alteration**
- Focus: Private (P)


**Requirements**
<> Internet Connectivity
<> VPN server and client


![[Pasted image 20250628112747.png]]

- Main Branch VPN and 2 Client VPNs
- Remote Branch 1 sends **Encrypted data** to Main Branch via tunnel (blue wire)
- Decrypted Data takes place in the green wire


**More** **Notes**
- Cannot view IP addresses (public)
- Local ISP sees only encrypted traffic (cannot censor internet access)
- Not all VPN connections route traffic over the VPN tunnel
- Some VPNs give you access to a private network, however do not route your traffic.




