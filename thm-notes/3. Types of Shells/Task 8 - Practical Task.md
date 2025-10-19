
- `MACHINE_IP:8080 hosts the landing page
- `MACHINE_IP:8081 hosts the web application that is vulnerable to command injection.
- `MACHINE_IP:8082 hosts the web application that is vulnerable to an unrestricted file upload.`


**Using a reverse or bind shell, exploit the command injection vulnerability to get a shell. What is the content of the flag saved in the / directory?**  
- `Create a listener on the attacker machine`
- `nc lvnp -8080`
- Go to MACHINE_IP:8081 and insert payload in text field (refer to task 3) for reverse shells
- From there reverse shell is granted and now you can access the flag.



**Using a web shell, exploit the unrestricted file upload vulnerability and get a shell. What is the content of the flag saved in the / directory?- MACHINE_IP:8080 hosts the landing page**
- `Create a basic php script that invokes GET (CMD) and name it shell.php`
- `Navigate to MACHINE_IP:8082 and upload said file`
- `Navigate to URL path/uploads/shell.php`
- `Now you have access to the shell output through the browser`
- Retrieve the FLAG



