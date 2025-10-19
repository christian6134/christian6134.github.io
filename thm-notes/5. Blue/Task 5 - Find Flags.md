
**Flag 1:**
- Location? (ROOT)
- Option 1: 
	- Navigate to root 'C:' and find flag1.txt
- Option 2:
	- search -f flag1.txt

**Flag 2:**
- Location? (C:/Windows/System32/Config)
- This holds all SAM Data base information (Security Account Manager)
- However the flag2.txt is present in the directory
- OR just `search -f flag2.txt`

**Flag 3:**
- Location? Administrator Documents
- We figured out that **Jon** is the administrator
- `C:/Windows/Users/Jon/Documents/Flag3.txt`

