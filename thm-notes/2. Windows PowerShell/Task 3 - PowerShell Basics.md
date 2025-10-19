
**Launching Powershell**
- Start menu: Type `powershell`
- Search: `Windows PowerShell`
- `Win + R` ---> Run ---> Powershell
- File Explorer: navigate to any folder, then type powershell in the address bar
- Task Manager: Open task Manager --> File ---> Run New Task ---> powerShell

**cmdlets (command-lets)**
- Follows the convention `Verb-Noun`
- **Verb** - Describes the Action
- **Noun** - Specifies the action

**Examples**
- `Get-Content`: (GETS) the content of a file and displays it in the console
- `Set-Location`: Changes (sets) the current working directory

`Get-Command`
- Lists all available cmdlets 

`-CommandType Function`
- Filters the list of Get-Command into only Commands that are of type Function

`Get-Help` : Provides detailed info about cmdlets, usages, parameters and examples

`Get-Alias` - Lists all aliases available
`dir` is an Alias for `Get-ChildItem`
`cd` is an Alias for `Set-Location`

`Find-Module` - Searches modules (collection of cmdlets) in online repositories
- `Find-Module -Name "Name"`
- 
`Install-Module` 


**Questions**
- How to retieve a list of commands that start with the verb "Remove"
- `Get-Command -Name Remove*`

- Alias for ECHO?
- `Get-Alias ECHO` --> `Write-Output`

- What is the command to retrieve some example usage for the cmdlet New-LocalUser?
- `Get-Help New-LocalUser -examples`

