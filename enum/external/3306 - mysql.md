# nmap 

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 3306 "--script=banner,(mysql* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp3306/tcp_3306_mysql_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp3306/xml/tcp_3306_mysql_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00060s latency).
Scanned at 2025-02-08 02:17:32 EST for 1s

PORT     STATE SERVICE REASON         VERSION
3306/tcp open  mysql   syn-ack ttl 64 MySQL 5.0.51a-3ubuntu5
|_mysql-vuln-cve2012-2122: ERROR: Script execution failed (use -d to debug)
|_ssl-ccs-injection: No reply from server (TIMEOUT)
|_mysql-empty-password: ERROR: Script execution failed (use -d to debug)
| mysql-info: 
|   Protocol: 10
|   Version: 5.0.51a-3ubuntu5
|   Thread ID: 24
|   Capabilities flags: 43564
|   Some Capabilities: SupportsCompression, SupportsTransactions, LongColumnFlag, SwitchToSSLAfterHandshake, Support41Auth, Speaks41ProtocolNew, ConnectWithDatabase
|   Status: Autocommit
|_  Salt: &DfSNkP.5\TmKjXY4:di
| banner: >\x00\x00\x00\x0A5.0.51a-3ubuntu5\x00\x16\x00\x00\x00(N0DDkkZ\x
| 00,\xAA\x08\x02\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00
|_^LBEp)xC""!!\x00
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:33 2025 -- 1 IP address (1 host up) scanned in 2.49 seconds

```