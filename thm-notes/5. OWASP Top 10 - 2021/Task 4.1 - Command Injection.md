
### Command Injection
------
Occurs when server-side code like **PHP** in a web app makes a call to a function that interacts with the server's console directly.
- Allows attacker to take advantage of calls to execute OS commands on the server
- Possibilities are **endless**
	- List files
	- Read contents
	- Recon on the server
	- As if they are were sitting on the machine using the terminal

**Code Example**

Let's consider a scenario: MooCorp has started developing a web-based application for cow ASCII art with customisable text. While searching for ways to implement their app, they've come across the `cowsay` command in Linux, which does just that! Instead of coding a whole web application and the logic required to make cows talk in ASCII, they decide to write some simple code that calls the cowsay command from the operating system's console and sends back its contents to the website.

Let's look at the code they used for their app.  See if you can determine why their implementation is vulnerable to command injection.  We'll go over it below.

```php
<?php
    if (isset($_GET["mooing"])) {
        $mooing = $_GET["mooing"];
        $cow = 'default';

        if(isset($_GET["cow"]))
            $cow = $_GET["cow"];
        
        passthru("perl /usr/bin/cowsay -f $cow $mooing");
    }
?>
```

In simple terms, the above snippet does the following:  

1. Checking if the parameter "mooing" is set. If it is, the variable `$mooing` gets what was passed into the input field.
2. Checking if the parameter "cow" is set. If it is, the variable `$cow` gets what was passed through the parameter.
3. The program then executes the function `passthru("perl /usr/bin/cowsay -f $cow $mooing");`. The passthru function simply executes a command in the operating system's console and sends the output back to the user's browser. You can see that our command is formed by concatenating the $cow and $mooing variables at the end of it. Since we can manipulate those variables, we can try injecting additional commands by using simple tricks. If you want to, you can read the docs on `passthru()` on [PHP's website](https://www.php.net/manual/en/function.passthru.php) for more information on the function itself.

![Command Injection](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/8c2e8030730682f9eb1304fa1d81d47a.png)  

Exploiting Command Injection

Now that we know how the application works behind the curtains, we will take advantage of a bash feature called "inline commands" to abuse the cowsay server and execute any arbitrary command we want. Bash allows you to run commands within commands. This is useful for many reasons, but in our case, it will be used to inject a command within the cowsay server to get it executed.

To execute inline commands, you only need to enclose them in the following format `$(your_command_here)`. If the console detects an inline command, it will execute it first and then use the result as the parameter for the outer command. Look at the following example, which runs `whoami` as an inline command inside an `echo` command:

![Inline commands](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/b7158502a9799698ec0ab29a850c8840.png)  

So coming back to the cowsay server, here's what would happen if we send an inline command to the web application:

![Sending our payload](https://tryhackme-images.s3.amazonaws.com/user-uploads/5ed5961c6276df568891c3ea/room-content/9f657b909062ac82af12548b4f346aec.png)

Since the application accepts any input from us, we can inject an inline command which will get executed and used as a parameter for cowsay. This will make our cow say whatever the command returns! In case you are not that familiar with Linux, here are some other commands you may want to try:

- **whoami**
- **id**
- **ifconfig/ip addr**
- **uname -a**
- **ps -ef**

To complete the questions below, navigate to [http://10.10.215.157:82/](http://10.10.215.157:82/)[](http://10.10.215.157:82/) and exploit the cowsay server.


### Exercise
--------
**What strange text file is in the website's root directory?**
- `$(ls)`
- drpepper.txt


**How many non-root/non-service/non-daemon users are there?**  
- `$(cat /etc/passwd)`
- Shows all users
- `0` all are under sbin -> system binary



**What user is this app running as?**  
- `$(whoami)`
- Apache


**What is the user's shell set as?**  
- Within cat /etc/passwd
- `/sbin/nologin`



**What version of Alpine Linux is running?**
- `$(cat /etc/os-release)`
- Version 3.16.0
