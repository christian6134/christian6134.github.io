**TLS**
------------
- Like SSL (parent), TLS is a **cryptographic protocol** operating on the **OSI Model's** transport layer
- Allows secure communication between **client and server** over an **insecure network**
- Ensures that no one can read or modify the exchanged data


**TLS Procedure**
-------------------------
**For every server or client**
- Identify itself to receive a **signed TLS Certificate**
- Server admin creates a **Certificate Signing Request (CSR)** 
- Submits **CSR** to the Certificate Authority (CA)
- CA verifies CSR and issues a **Digital Certificate**
**Then certificate is used** to identify the server or client to others who can confirm validity of a signature

- Self signed certificates cannot prove the servers authenticity
- Need a 3rd party to confirm