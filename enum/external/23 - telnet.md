# nmap
```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:30 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 23 --script=banner,telnet-encryption,telnet-ntlm-info -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp23/tcp_23_telnet-nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp23/xml/tcp_23_telnet_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00038s latency).
Scanned at 2025-02-08 02:17:31 EST for 8s

PORT   STATE SERVICE REASON         VERSION
23/tcp open  telnet  syn-ack ttl 64 Linux telnetd
|_banner: \xFF\xFD\x18\xFF\xFD \xFF\xFD#\xFF\xFD'
| telnet-encryption: 
|_  Telnet server does not support encryption
MAC Address: 00:0C:29:95:39:3E (VMware)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:39 2025 -- 1 IP address (1 host up) scanned in 8.44 seconds

```