
**Note**: Downloading and receiving emails from one device e.g Desktop Computer
- When using multiple devices, need synchronization use Task 8 - **IMAP**

**Scenario:** You received an email and want to download it to your local mail client

**Post Office Protocol Version 3 (POP3)**
--------------------------------------------------
- Similar to handling your envelope or package
- **POP3** checks your local mailbox for new letters and packages

**POP3 Commands**
- **USER (username)** ---> Identifies the user
- **PASS (password)** ----> Provides the user's password
- **STAT** -----> Requests the number of messages and total size
- **LIST** ------> Lists all messages and their sizes
- **RETR (message_number)** -----> Retrieves the specified message
- **DELE (message_number)** ---> Marks message for deletion
- **QUIT** --> ends the POP3 session applying changes

Listens on **TCP Port 110 by Default**

`telnet MACHINE_IP 110`
`AUTH`
`User: user`
`Pass: pass`
`LIST`
`RETR 1..2..3..4`
`Found FLAG!`
