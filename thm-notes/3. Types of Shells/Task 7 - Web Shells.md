
A web shell is a script written in a language supported by a compromised web server that executes commands through the web server itself. A web shell is usually a file containing the code that executes commands and handles files. It can be hidden within a compromised web application or service, making it difficult to detect and very popular among attackers.

------

![[ex-php-shell.png]]

- Saved into a file with the PHP extension
- Uploaded into the web server by exploiting vulnerabilities such as ### [Unrestricted File Upload](https://tryhackme.com/r/room/uploadvulns), [File Inclusion](https://tryhackme.com/r/room/fileinc), [Command Injection](https://tryhackme.com/r/room/oscommandinjection), among others, or by gaining unauthorized access to it.

**What now?**
- `Web shell deployed in the server`
- `accessed through URL where the shell is hosted`
-  provide a GET method and the value of the variable `cmd`, which should contain the command the attacker wants to execute. For example, if we want to execute the command **whoami** the request to the URL should be: http://victim.com/uploads/shell.php?cmd=whoami


### Existing Web Shells
--------
- [p0wny-shell](https://github.com/flozz/p0wny-shell) - A minimalistic single-file PHP web shell that allows remote command execution.
    
    ![The image is a screenshot of the web shell p0wny-shell showing commands being executed in a GUI similar to a real terminal](https://tryhackme-images.s3.amazonaws.com/user-uploads/66c513e4445cb5649e636a36/room-content/66c513e4445cb5649e636a36-1727563529557.png)
    
- [b374k shell](https://github.com/b374k/b374k) - A more feature-rich PHP web shell with file management and command execution, among other functionalities.  
    
    ![The image is a screenshot of b374k shell displaying the file manager feature that allows to manipulate files](https://tryhackme-images.s3.amazonaws.com/user-uploads/66c513e4445cb5649e636a36/room-content/66c513e4445cb5649e636a36-1727563529904.png)
    
- [c99 shell](https://www.r57shell.net/single.php?id=13) - A well-known and robust PHP web shell with extensive functionality.  
    
    ![The image is a screenshot of  c99 shell displaying the command execution feature and the file manipulation one](https://tryhackme-images.s3.amazonaws.com/user-uploads/66c513e4445cb5649e636a36/room-content/66c513e4445cb5649e636a36-1727563530257.png)
    

You can find more web shells at: [https://www.r57shell.net/index.php](https://www.r57shell.net/index.php).