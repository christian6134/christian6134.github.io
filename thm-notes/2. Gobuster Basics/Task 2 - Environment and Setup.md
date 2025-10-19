
For this room, we will use an Ubuntu 20.04 VM acting as a web server. This web server hosts multiple subdomains and vhosts. The web server also has two content management systems (CMS) installed. These are Wordpress and Joomla.

Important: We work in a local network with a DNS server on the web server. To ensure we can resolve the domains used throughout this room, you need to change the `/etc/resolv-dnsmasq` file:

- Open up a terminal on the the AttackBox and enter the command: `sudo nano /etc/resolv-dnsmasq`.
- Insert `nameserver MACHINE_IP` as the first line.
- Save the file by pressing CTRL+O, followed by pressing ENTER, and then exit the editor by pressing CTRL+X.
- Enter the command `/etc/init.d/dnsmasq restart` to restart the Dnsmasq service.

The file should look something like this:

AttackBox Terminal

```shell-session
root@tryhackme:~# cat /etc/resolv-dnsmasq 
nameserver MACHINE_IP
nameserver 169.254.169.253
```



I assigned the `MACHINE_IP` as the first `nameserver` in the `/etc/resolv-dnsmasq` file and restarted the Dnsmasq service.