
**Recall**:
- RAR Archives are compressed files created by the WinRAR archive manager
- Compress folders and files



### Rar2John
------
- `rar2john` converts the RAR file into a hash format that john can understand

**Basic Syntax**
- `rar2john [rar file] > [output file]`
- once we convert it to hash format we can then feed it to john and retrieve the password.


**Exercise**
What is the password for the secure.rar file?
- `password`


What is the contents of the flag inside the zip file?
- `unrar x secure.rar`
- `THM{r4r_4rch1ve5_th15_t1m3}`



