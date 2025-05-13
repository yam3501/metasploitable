# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 111 "--script=banner,(rpcinfo or nfs*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp111/tcp_111_nfs_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp111/xml/tcp_111_nfs_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00045s latency).
Scanned at 2025-02-08 02:17:31 EST for 18s

PORT    STATE SERVICE REASON         VERSION
111/tcp open  rpcbind syn-ack ttl 64 2 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2            111/tcp   rpcbind
|   100000  2            111/udp   rpcbind
|   100003  2,3,4       2049/tcp   nfs
|   100003  2,3,4       2049/udp   nfs
|   100005  1,2,3      52497/udp   mountd
|   100005  1,2,3      55067/tcp   mountd
|   100021  1,3,4      33213/tcp   nlockmgr
|   100021  1,3,4      54521/udp   nlockmgr
|   100024  1          49261/udp   status
|_  100024  1          58928/tcp   status
| nfs-showmount: 
|_  / *
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:49 2025 -- 1 IP address (1 host up) scanned in 18.22 seconds

```
# 