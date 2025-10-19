`ipconfig` 
- Check network information
- IP Addr, Subnet mask, Default Gateway
- `ipconfig /all`

`ping target_name`
- Check if server can access a server on the web
- `ping example.com`

`tracert`
(traceroute)
- traces network route traversed
- TTL reached 0 -> packet dropped

`nslookup`
- Looks up host or domain -> Returns IP addr

`netstat`
- Displays current **network** **connections** and **listening** **ports**
- No arguments -> Established connections
- **Port** **22** -> **SSH**

`netstat -a` displays all established connections and listening ports
`netstat -b` shows the program associated with each listening port and connection
`netstat -o` reveals PID associated with connection
`netstat -n` numerical form for addr and port numbers
`