
### What is a Cryptographic Failure?
------
This refers to any vulnerability arising from the `misuse (lack of use)` of cryptographic algorithms for **protecting sensitive information.** 
- Web Apps require cryptography to **provide confidentiality for their users at many levels**

##### Example:
------
Secure Email Application:

- Ensure email account communication between client and server is encrypted
- No eavesdropper should be able to recover content of your email address
- Encrypting data between Client and Server ? --> **Encrypting in Transit**

- Since emails are stored in some backend server
- We need to make sure that the email provider cannot view the client emails
- Emails might be encrypted **when stored on servers**
- This is referred to **Encrypting At Rest**

### Man in The Middle Attacks (MiTM)
------
Attacker forces user connections through a device they control.
- Take advantage of weak encryption on any data to access the information
- Continue this exercise in following tasks.