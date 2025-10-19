
Uses a separate part of the John suite of tools to convert the ZIP file into a format the John will understand. 


### Zip2John
--------------
Similar to the `unshadow` tool, we will use `Zip2John` tool to convert the Zip File into a **hash format** that John can understand and crack. 

`zip2john [options] [zip file] > [output file]`

- [options] -> Pass specific checksum options to zip2john (not typically necessary)
- [zip file] -> Path to zip file you wish 
- > redirects output to [output file]


- Then take the output file `zip_hash.txt` and feed it into John as an argument.

- (1) zip2John -> converts ZIP file into a hash format
- (2) Invoke john regularly 


**Exercise**
----------------
- What is the password for the `secure.zip file`?
  - `zip2john secure.zip > unzipped.txt`
  - `john --wordlist=/usr/share/wordlists/rockyou.txt unzipped.txt`
  - Password: **pass123**


What is the contents of the flag inside the zip file?
- `unzip secure.zip`
- Input password: pass123
- Flag contents: `THM{w3ll_d0n3_h4sh_r0y4l}`

