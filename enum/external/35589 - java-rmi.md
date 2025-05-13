# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:19:52 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 35589 --script=banner,rmi-vuln-classloader,rmi-dumpregistry -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp35589/tcp_35589_rmi_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp35589/xml/tcp_35589_rmi_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00077s latency).
Scanned at 2025-02-08 02:19:52 EST for 142s

PORT      STATE SERVICE  REASON         VERSION
35589/tcp open  java-rmi syn-ack ttl 64 GNU Classpath grmiregistry
|_rmi-vuln-classloader: ERROR: Script execution failed (use -d to debug)
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:22:14 2025 -- 1 IP address (1 host up) scanned in 141.68 seconds

```