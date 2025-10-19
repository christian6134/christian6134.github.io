
**Telnet**: Used to login to remote systems, however it is risky because traffic is sent in cleartext

Alternatively, 

**Secure Shell (SSH) Protocol**
-------------------
Key Features:
- **Secure Authentication**: Password-Based authentication, Public Key, 2FA
- **Confidentiality**: OpenSSH provides end-to-end encryption
	- No eavesdropping
	- Notifies of new server keys to protect against MiTM attacks
- **Integrity**: Cryptography protects integrity of traffic
- **Tunneling**: Creates a secure "tunnel" to route other protocols through SSH (Example: VPN Connections)
- **X11 Forwarding**: Unix systems with GUIs, use GUIs over a network

`ssh username@hostname`
- Use public key

`-X` argument allows support for running GUIs
- (Local system must have them installed)
- Ex, KALI LINUX

- Listens on **22**


**SSH File Transfer Protocol** (SFTP)
-----------
- Allows Secure file transfer
- Apart of SSH protocol

`sftp username@hostname`
`get filename`
`put filename`

**Not to be confused with FTPS**
- FTPS -> File Transfer Protocol Secure
- Uses TLS