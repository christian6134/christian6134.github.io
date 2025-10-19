
**A shell script** is just a set of commands
Suppose:
- A repetitive task requires entering multiple commands through a shell
- Combine them into a script, execute all commands through executing the script
- Scripting helps with **Automation**
Scripting can be done in **various programming languages**

1. Open a terminal
2. Select a shell
3. Create file using text editor
4. Extension needed is **.sh** ---> default for bash scripts
5. `nano first_script.sh`

**Shebang**
---
Every script should start from **shebang**
**Shebang**:
- Combination of some characters that are added at the **beginning of a script**
- Start with **#!** followed by the name of the interpreter `\bin\bash`

**Fundamentals of a Script**
---
1. Shebang

**Variables**
- Store values inside it
- Can store URLs, File Paths, etc...

![[Pasted image 20250624161046.png]]

- Give permissions to execute the script
- `chmod +x first_script.sh`

**Script has execution permissions, use** `./` before the script to execute it
- ./ tells the shell to execute the file that is present in the current directory
- 
![[Pasted image 20250624161217.png]]

**LOOPS**
---
![[Pasted image 20250624161417.png]]
`do and done` signify the enclosure of the code desired to be looped. In this case it is
- echo $i


**Conditional Statements**
--
![[Pasted image 20250624161944.png]]
- Takes user as input and stores as variable
- Conditional starts with if and compares value to Stewart
- fi is used to end the condition




