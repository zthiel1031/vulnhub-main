# This is the write up for the Vulnhub box STAR WARS CTF 1 

Box Ip Address: 10.38.1.114

Attacking Machine Ip: 10.38.1.110
## **Information Gathering**
---
Starting with an Nmap port Scan we see this output:

![](Images/nmap.JPG)

The two open ports are the HTTP port 80 and the SSH port of 22. With port 80 being open, we can assume that this is a web server. Upon navigating to the address `10.38.1.114` we are greeted with this page:

![](Images/websitemain.JPG)

It seems as if there is something hidden on this page. If we look at the inspector code through firefox we see this:

![](Images/websitecode.JPG)

This tips us off that there is, in fact, something hidden here. WWe can use this command to download both the files:

```
wget http://10.38.1.114/images/yoda.jpg
```
and

```
wget http://10.38.1.114/images/yoda.png
```

