
### Netfilter
---
Netfilter is the framework inside the Linux OS with core firewall functionalities, including packet filtering, NAT, and connection tracking. This framework serves as the foundation for various firewall utilities available in Linux to control network traffic. Some common firewall utilities that utilize this framework are listed below:

- **iptables:** This is the most widely used utility in many Linux distributions. It uses the Netfilter framework that provides various functionalities to control network traffic.
- **nftables:** It is a successor to the “iptables” utility, with enhanced packet filtering and NAT capabilities. It is also based on the Netfilter framework.
- **firewalld:** This utility also operates on the Netfilter framework and has predefined rule sets. It works differently from the others and comes with different pre-built network zone configurations.

### ufw 
----
ufw (Uncomplicated Firewall), as the name says, eliminates the complications of making rules in a complex syntax in “iptables”(or its successor) by giving you an easier interface. It is more beginner-friendly. Basically, whatever rules you need in “iptables”, you can define them with some easy commands via ufw, which would then be configuring your desired rules in “iptables”. Let’s have a look at some basic ufw commands down below.

To check the status of the firewall, you could use the command below:

Check status

```shell-session
user@ubuntu:~$ sudo ufw status
Status: inactive
```

If it appears inactive, you can enable it using the following command:

Enablefirewall

```shell-session
user@ubuntu:~$ sudo ufw enable
Firewall is active and enabled on system startup
```

To turn off the firewall, type “disable” instead of “enable” in the above command.

Below is a rule created to allow all the outgoing connections from a Linux machine. The `default` in the command means that we are defining this policy as a default policy allowing all the outgoing traffic unless we define an outgoing traffic restriction on any specific application in a separate rule. You can also make a rule to allow/deny traffic coming into your machine by replacing `outgoing` with `incoming` in the following command:

Allow all outgoing traffic

```shell-session
user@ubuntu:~$ sudo ufw default allow outgoing
Default outgoing policy changed to 'allow'
(be sure to update your rules accordingly)
```

You can deny incoming traffic at any port in your system. Let's say that we want to block incoming SSH traffic. We can achieve this with the command `ufw deny 22/tcp`. As you can see, we first specified the action, `deny` in this case; furthermore, we specified the port and the transport protocol, which is TCP port 22, or simply `22/tcp`.

Deny incomingSSHtraffic

```shell-session
user@ubuntu:~$ sudo ufw deny 22/tcp
Rule added
Rule added (v6)
```

To list down all the active rules in a numbered order, you can use the following command:

List all rules

```shell-session
user@ubuntu:~$ sudo ufw status numbered
     To                         Action      From
     --                         ------      ----
[ 1] 22/tcp                     DENY IN     Anywhere                  
[ 2] 22/tcp (v6)                DENY IN     Anywhere (v6)   
```

To delete any rule, execute the following command with the rule number to delete:

Delete a rule

```shell-session
user@ubuntu:~$ sudo ufw delete 2
Deleting:
 deny 22/tcp
Proceed with operation (y|n)? y
Rule deleted (v6)
```

These different utilities can be used to manage Netfilter. Choosing the right utility for the Linux OS depends on multiple factors, such as familiarity with the OS and your requirements. You can test your knowledge of Linux firewalls by creating some rules defined in this task and testing them to ensure they are working as expected.