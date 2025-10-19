
**Recall:**
- `A reverse shell will connect from the compromised target to the attacker's machine.`
- `Netcat can handle the connection and allow the attacker to interact with the exposed shell`
- `There are other utilities that can do this...`


### Other Utilities
---------
**RLWrap**
- Utilitie that uses GNU readline library to provide `editing keyboard and history`

**Example**
- `rlwarp nc -lvnp 443`
- Wraps NC with rlwrap allow the use of features like arrow keys and history for better interaction.


**Ncat**
- Improved version of netcat
- Provides extra features like `encryption (SSL)`
- `ncat -lvnp 444` or `ncat -ssl -lvnp 4444`


**Socat** (socket cat)
- `Utility that allows you to create a socket connection between two data sources (two different hosts`
- `socat -d -d TCP-LISTEN:433 STDOU`
- The command above used the `-d` option to enable verbose output; using it again (`-d -d`) will increase the verbosity of the commands. The `TCP-LISTEN:443` option creates a TCP listener on port `443`, establishing a server socket for incoming connections. Finally, the STDOUT option directs any incoming data to the terminal.