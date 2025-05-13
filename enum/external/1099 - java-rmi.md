# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 1099 --script=banner,rmi-vuln-classloader,rmi-dumpregistry -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp1099/tcp_1099_rmi_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp1099/xml/tcp_1099_rmi_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00042s latency).
Scanned at 2025-02-08 02:17:31 EST for 22s

PORT     STATE SERVICE  REASON         VERSION
1099/tcp open  java-rmi syn-ack ttl 64 GNU Classpath grmiregistry
| rmi-vuln-classloader: 
|   VULNERABLE:
|   RMI registry default configuration remote code execution vulnerability
|     State: VULNERABLE
|       Default configuration of RMI registry allows loading classes from remote URLs which can lead to remote code execution.
|       
|     References:
|_      https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/multi/misc/java_rmi_server.rb
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:53 2025 -- 1 IP address (1 host up) scanned in 22.17 seconds

```