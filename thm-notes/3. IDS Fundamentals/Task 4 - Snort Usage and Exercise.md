
Snort has some built-in rule files, a configuration file, and other files. These are stored in the `/etc/snort` directory. The key file for Snort is its configuration file `snort.conf`, where you can specify which rule files to enable and which network range to monitor and enable other settings. The rule files are stored in the `rules` folder. Let's use the `ls` command to list down all the files and folders present in Snort's main directory:

Snort Directory
```shell-session
ubuntu@tryhackme:~$ ls /etc/snort
classification.config  reference.config  snort.debian.conf
community-sid-msg.map  rules             threshold.conf
gen-msg.map            snort.conf        unicode.map
```

## Rule Format
-----
Now, let’s discuss how rules are created in Snort. There is a specific way of writing the rules. Following is a sample rule that would detect ICMP packets (usually used when you ping a host) coming from any IP address and port and reaching the home network (the network range is defined in Snort’s configuration file) to any port. Once such traffic is detected, it generates “Ping Detected” alerts.

![](https://tryhackme-images.s3.amazonaws.com/user-uploads/6645aa8c024f7893371eb7ac/room-content/6645aa8c024f7893371eb7ac-1725532438800.png)  

The details of the components involved in this rule are given below:

- **Action:** This specifies which action to take when the rule triggers. In this case, we have the action to "alert" when the traffic matches this rule.
    
- **Protocol:** This refers to the protocol that matches this rule. In this case, we use the protocol "ICMP," which is used when we ping a host.
    
- **Source IP:** This determines the IP from which the traffic is originating. Since we want to detect traffic from any source IP, we set this as "any".
    
- **Source port:** This determines the port from which the traffic is originating. Since we want to detect traffic from any source port, we set this as "any".
    
- **Destination IP:** This specifies the destination IP to which the matching traffic comes; it generates the alert. In this case, we used "$HOME_NET". This is a variable, and we defined its value as our whole network’s range in the Snort’s configuration file.
    
- **Destination port:** This specifies the port the traffic would reach. As we want to detect traffic coming to any port, we set it as "any".
    
- **Rule metadata:** Every rule has some metadata. That is defined at the end of the rule in parentheses. The following are its components:
    

- **Message (msg):** This describes the message to be displayed when the subject rule triggers. The message should indicate the type of activity detected. In this case, we used "Ping Detected".
    
- **Signature ID (sid):** Every rule has a unique identifier that differentiates it from the other rules. This identifier is called the signature ID (sid). In this case, we set the sid to "10001".
    
- **Rule revision (rev):** This sets the revision number of the rule. Every time the rule is modified, its revision number is incremented. This helps in tracking the changes to any rule.
    

## Rule Creation
---
Let’s paste the sample rule explained above into the custom "local.rules" file in the Snort rules directory.

Firstly, open the "local.rules" file in a text editor:

Edit Custom Rule File

```shell-session
ubuntu@tryhackme:~$ sudo nano /etc/snort/rules/local.rules
```

Now, add the following rule after the already present rules to the file:

`alert icmp any any -> 127.0.0.1 any (msg:"Loopback Ping Detected"; sid:10003; rev:1;)`

**Note:** We will need the other already present rules in the next task, so do not delete them.

Once you successfully edit the file, press "ctrl+x" and it will ask you to press "y" if you want to save the changes. Press "y" to save the changes.

## Rule Testing
---
Let’s first start the snort tool to detect any intrusions defined in the rule file. For this, we have to execute the following command with sudo privileges in our console:

Running Snort for Detections

```shell-session
ubuntu@tryhackme:~$ sudo snort -q -l /var/log/snort -i lo -A console -c /etc/snort/snort.conf
```

**Note:** In case your loopback interface is not called "lo", replace it with the correct interface name. 

As this rule is designed to alert us on any ICMP packets to our loopback address, let’s try to ping our loopback address to see if our rule works:

Ping Host

```shell-session
ubuntu@tryhackme:~$ ping 127.0.0.1
```

The screenshot below shows the Snort-generated "Loopback Ping Detected" alert when we ping our host's loopback IP. This means that our rule is working fine.

Running Snort for Detections

```shell-session
ubuntu@tryhackme:~$ sudo snort -q -l /var/log/snort -i lo -A console -c /etc/snort/snort.conf
07/24-10:46:52.401504  [**] [1:1000001:1] Loopback Ping Detected [**] [Priority: 0] {ICMP} 127.0.0.1 -> 127.0.0.1
07/24-10:46:53.406552  [**] [1:1000001:1] Loopback Ping Detected [**] [Priority: 0] {ICMP} 127.0.0.1 -> 127.0.0.1
07/24-10:46:54.410544  [**] [1:1000001:1] Loopback Ping Detected [**] [Priority: 0] {ICMP} 127.0.0.1 -> 127.0.0.1
```

## Running Snort on PCAP Files
---
We saw how Snort can be used for intrusion detection on real-time traffic. However, you may sometimes encounter a scenario where you have historical network traffic logged in a file, and you have to perform a forensic investigation to determine any signs of intrusion through that traffic. This traffic is usually logged in the standard packet capture format "PCAP". Snort is also equipped to perform detections on these PCAP files containing historical network traffic.

![Machine presenting the usage of Snort for analyzing PCAP files.](https://tryhackme-images.s3.amazonaws.com/user-uploads/6645aa8c024f7893371eb7ac/room-content/6645aa8c024f7893371eb7ac-1723014181865.png)  

The following command with sudo privilege can be used to perform this action:

Running Snort onPCAP

```shell-session
ubuntu@tryhackme:~$ sudo snort -q -l /var/log/snort -r Task.pcap -A console -c /etc/snort/snort.conf
```

**Note:** Replace the "Task.pcap" with the path to your PCAP file for analysis.




