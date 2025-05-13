# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:19:52 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 55067 "--script=banner,nfs* and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp55067/tcp_55067_mountd_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp55067/xml/tcp_55067_mountd_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00079s latency).
Scanned at 2025-02-08 02:19:52 EST for 21s

PORT      STATE SERVICE REASON         VERSION
55067/tcp open  mountd  syn-ack ttl 64 1-3 (RPC #100005)
| nfs-showmount: 
|_  / *
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:20:13 2025 -- 1 IP address (1 host up) scanned in 21.56 seconds

```