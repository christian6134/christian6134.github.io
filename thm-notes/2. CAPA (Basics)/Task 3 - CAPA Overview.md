
#### Running CAPA

1. Open **PowerShell**.

2. Navigate to the correct directory:
    
    `cd C:\Users\Administrator\Desktop\capa`
    
3. Run CAPA on a binary:
    
    `capa.exe .\cryptbot.bin`
    

---

#### Useful Options

- `-h` → Show help (list of parameters).
    
- `-v` → Verbose results.
    
- `-vv` → Very verbose results (most detail, slower).
    

---

#### Example Command

`capa.exe .\cryptbot.bin -v`

---

#### Checking Pre-Processed Results

A processed file `cryptbot.txt` is available.  
View it with:

`Get-Content .\cryptbot.txt`

---

#### Quick Q&A

- **Check available parameters?** → `-h`
    
- **Detailed capabilities?** → `-v`
    
- **Very detailed capabilities?** → `-vv`
    
- **Read a file in PowerShell?** → `Get-Content`