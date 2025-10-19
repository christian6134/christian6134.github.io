
### What are Custom Rules?
-----
- Similar to mangling patterns, you can define your rules, which **John** will use to create passwords **dynamically**.
		- Ability to define such rules is beneficial once you know more information about **password** **structure**


**Common Custom Rules**
- Lowercase letters
- Uppercase letters
- Numbers
- Symbols

All of these contribute to **password** **complexity**
	- However, these predictable locations of symbols can be used against the security of individuals.

`Example: Polopassword!`


### Creating Custom Rules
----
Defined in the `john.conf` file
- Path=`/opt/john/john.conf on AttackBox
- Path=`/etc/john/john.conf` on local machine

More Info Here:
https://arc.net/l/quote/nqoqedjm


**Custom Rules Syntax**
*The First Line:*
- `[List.Rules:THMRules]` is used to **define the name** of your rule; this is what you will call a **John Argument**

*Regex Style Pattern Match to define where the word will be **modified***
- Az: Takes the word and appends it to the character you define
- A0: Takes the word and prepends it to the character you define
- c: Capitalizes the character positionally

*Define what Characters should be appended, prepended`
- Use `[ ]` where they should be used
	- 0-9: one through nine
	- 0 : 0
	- A-z: both
	- A-Z : upper
	- a-z : lower

**Note:**
- `[a]`: Will include only `a`
- `[!£$%@]`: Will include the symbols `!`, `£`, `$`, `%`, and `@`



**Example**
Scenario: To generate a wordlist from the rules that match the example `Polopassword1` 

Assume: `polopassword` is in the word list.

1) `[List.Rules:PoloPassword`
2) `cAz"[0-9] [!£$%@]"



### Using Custom Rules
---
Call the rule `--rule=PoloPassword`
`john --wordlist=[path] --rule=PoloPassword [path to file]`



**Exercises**
- What do custom rules allow us to exploit?
	- **Password Complexity Predictability**


- What flag would we use to call a custom rule called `THMRules`?
	- `--rule=THMRules`


- What rule would we use to add all capital letters to the end of the word?
	- `Az"[A-Z]"`
	- Az --> Appends to the end of the word
	- "[A-Z]" ---> All capital characters