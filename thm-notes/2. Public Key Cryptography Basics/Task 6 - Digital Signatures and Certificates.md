
**In the Analog world:**
- You are asked to sign a paper every now and then
	- It can confirm that you agree to the terms and conditions, authorize a transaction or acknowledge receiving an item

**In the Digital World:**
- You cannot use your signature, stamp or fingerprint
- Require a **Digital Signature**

**What is a Digital Signature?**
-------------------------------------------------------
Digital signatures provide a way to:
- Verify the authenticity and integrity of a digital message or document
- We know who created or modified these documents

Using **Asymmetric Cryptography**
- You can produce a signature with your private key, which is verified using your public key.

**In its Simplest Form**
- Digital Signature ---> Encrypting the Document with your own private key
- If someone wants to verify this signature, they would decrypt with your public key and check if the files match


--------------------------------------------------------


**Ceritificates "Prove Who You Are!"**
-------------------------------------------------------------------
Essential application of public key cryptography & are linked to digital signatures
- Commonly used for HTTPs
- How does your web browser know that the server you're talking to is the real tryhackme.com?

**Certificates:
- Web servers have certificates to verify it is the real "------"
- **Certificate Authority (CA)** ---> Creates a chain of trust starting with (root) (CA)
- Certificates are trusted only when the ROOT CAs say they trust the organization that signed them
- Browsers trust the certificates.... **long chains of trust**


**HTTPs requires a TLS Certificate**

