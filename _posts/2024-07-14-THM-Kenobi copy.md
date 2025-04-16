---
title: "Try Hack Me - Kenobi"
date: 2024-07-14T02:31:30-04:00
categories:
  - blog
tags:
  - Linux
  - THM
---

**Room Name:** Kenobi  
**Level:** Easy  
**Platform:** TryHackMe  

![kenobi](https://jstgs.github.io/jsteg.github.io/images/kenobi.png)

The "Kenobi" room on TryHackMe is an introductory level capture the flag (CTF) style challenge focused on penetration testing skills. Participants are tasked with exploiting a fictional Linux machine named Kenobi to gain root access. The room emphasizes enumeration techniques, basic exploitation, and privilege escalation methods commonly encountered in real-world scenarios. By completing this room, participants gain practical experience in identifying vulnerabilities, exploiting them, and escalating privileges to achieve administrative access.

## Key Skills:
- Service enumeration using tools like Nmap.
- Exploiting vulnerable services (in this case, exploiting a vulnerability in an outdated version of ProFTPD).
- Escalating privileges through misconfigurations (exploiting a writable NFS share to gain root access).

Overall, the Kenobi room provides a hands-on learning experience suitable for beginners aiming to develop their penetration testing and ethical hacking skills in a controlled environment.


Starting off with a NMAP Null Scan

{% highlight bash %}
sudo nmap -sN 10.10.110.204
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-07-10 17:24 EDT
Nmap scan report for 10.10.110.204
Host is up (0.019s latency).
Not shown: 993 closed tcp ports (reset)
PORT     STATE         SERVICE
21/tcp   open|filtered ftp
22/tcp   open|filtered ssh
80/tcp   open|filtered http
111/tcp  open|filtered rpcbind
139/tcp  open|filtered netbios-ssn
445/tcp  open|filtered microsoft-ds
2049/tcp open|filtered nfs

Nmap done: 1 IP address (1 host up) scanned in 1.63 seconds

{% endhighlight %}
