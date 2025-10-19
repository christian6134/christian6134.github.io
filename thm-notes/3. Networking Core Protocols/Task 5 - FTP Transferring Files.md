
**File Transfer Protocol (FTP)**
-------------------
- Designed for transfer files
- Efficient for file transfer when all conditions are equal
- **Can** achieve higher speeds than HTTP

**FTP Commands**
- **USER**: used to input a **username**
- **PASS**: enter a **password**
- **RETR** (Retrieve): Download a file from the FTP server to **client**
- **STOR** (Store): Upload a file from the client to the FTP server

- Listens on TCP port 21: **default transfer** is conducted via another connection from the client to server

`ftp 10.10.207.121`
Name: `anonymous`
Pass: ` `
`ls` - lists all files available
`get flag.txt`


