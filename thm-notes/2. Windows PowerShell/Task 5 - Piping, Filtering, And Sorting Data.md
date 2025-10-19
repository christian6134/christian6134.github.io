

**Piping** : Technique used in CLI that **allows the output of one command to be used as the input for another**
- Allows for a **sequence of operations**
- Data flows from 1 command to the next
- `| -> Pipe`


Why is it powerful in **PowerShell**? 
- Passes **objects** rather than **just text**
- Objects can **carry data** and **properties / methods** that describe and interact with the data
- Allows combination of piping and cmdlets --> **Advanced data manipulation and analysis**


**Example**
- Listing files within a directory **piped** into Sort-Object Length
- `Get-ChildItem | Sort-Object Length`

- Displaying all files that end with `.txt.`
- `Get-ChildItem | Where-Object -Property "Extension" -eq ".txt`

- `Get-ChildItem | Where-Object -Property "Name" -like "ship*"`


**Comparison Operators**
- `-ne` - not equal (excludes objects from results)
- `-gt`- greater than (filter objects that exceed a value)
- `-ge` - greater than or equal to
- `-lt` - less than 
- `-le` - less than or equal to


**Select-Object**
- Used to select specific properties from objects or limit the number of objects returned
- Used when refining output to show only details one needs


**Select-String**
- Searches text pattern within files (similar to **grep**)
- `Select-String -Path ".\captain-hat.txt` -Pattern "hat"


**Questions**
- As an exercise, try and build a pipeline of cmdlets to sort and filter the output with the goal of displaying the largest file in the C:\Users\captain\Documents\captain-cabin directory
- `Get-ChildItem | Sort-Object Length -Descending | Select-Object -First 1`

- How would you retrieve the items in the current directory with size greater than 100? 
- `Get-ChildItem | Where-Object -Property "Length" -gt 100`










