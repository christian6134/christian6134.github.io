
`dir == ls`

`Get-ChildItem`- Lists the files and directories in a location specified with -Path or current working dir

`Set-Location` - Navigates to a different working directory
- `Set-Location -Path "./Documents"`
- Example to navigate to Documents directory from current directory

**To Create a New Item in PowerShell**
- Use `New-Item` 
- Must specify the path of the item and its **type**
- **File** or **Directory**
- `New-Item -Path .\captain-cabin\captain-wardrobe" -ItemType "Directory"`

**To Remove and Item**
- `Remove-Item` 
- `Remove-Item -Path "./path"`

**To Copy an Item**
- `Copy-Item` `-Path (path1) (path2)`

**To View File Contents**
- `Get-Content`
- `Get-Content -Path ".\captain-hat.txt"
`

**Questions**
- What CMDLET can you use instead of `type`
- `Get-Alias type`
- Answer: `Get-Content`

What PS Command would you use to display the content of the "C:\Users" directory? 
- `Get-ChildItem -Path C:\Users`

