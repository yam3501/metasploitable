# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 2049 "--script=banner,(rpcinfo or nfs*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp2049/tcp_2049_nfs_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp2049/xml/tcp_2049_nfs_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00061s latency).
Scanned at 2025-02-08 02:17:31 EST for 17s

PORT     STATE SERVICE REASON         VERSION
2049/tcp open  nfs     syn-ack ttl 64 2-4 (RPC #100003)
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:48 2025 -- 1 IP address (1 host up) scanned in 17.17 seconds

```