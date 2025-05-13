# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:21:14 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -sV -p 2049 "--script=banner,(rpcinfo or nfs*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/udp2049/udp_2049_nfs_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/udp2049/xml/udp_2049_nfs_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.0015s latency).
Scanned at 2025-02-08 02:21:14 EST for 10s

PORT     STATE SERVICE REASON              VERSION
2049/udp open  nfs     udp-response ttl 64 2-4 (RPC #100003)
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:21:24 2025 -- 1 IP address (1 host up) scanned in 10.58 seconds

```