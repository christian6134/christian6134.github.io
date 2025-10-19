
**Thus Far**, we have been using John's wordlist to brute-force simple and not-so-simple hashes.

**Single-Crack Mode:**
- John uses only information provided in the username to try and workout possible passwords **heuristically**
- Slightly changing the letters and numbers contained within the username


**Word Mangling**
Assume: 
- User: Markus
- Passwords (Possible)
	- Markus1, Marku2, Markus3...
	- MArkus, MARKus, MARkus...

**Note:** John is building a dictionary based on the information it has been fed and uses a **set of rules called mangling rules**. 

**Mangling Rules**: Define how John can mutate the word it started with to generate a wordlist thats relevant to the target being cracked. 



### GECOS
-------
General Electric Comprehensive Operating System

**GECOS Field**:
- Stores general information about the user, full name, office number, telephone number.
- John can utilize these records and generate them towards his own wordlist


-------

### USING Single Crack Mode
-----
`john --single -format=[format] [path to file]`
- Must change the file format so john knows what data to create a wordlist from
- Prepend hash with username that the hash belongs to
- Example: (hashes.txt)
	- 1efee03cdcb96d90 
	- mike:1efee03cdcb96d90


**Exercise**
- What is Jokers password?

**Procedure**
- Determine HASH ID
- Prepend the hash with Joker:
- Run John in single crack mode
- **Password: Jok3r**