# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:19:52 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 3632 --script=banner,distcc-cve2004-2687 --script-args=distcc-cve2004-2687.cmd=id -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp3632/tcp_3632_distcc_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp3632/xml/tcp_3632_distcc_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.0010s latency).
Scanned at 2025-02-08 02:19:52 EST for 17s

PORT     STATE SERVICE REASON         VERSION
3632/tcp open  distccd syn-ack ttl 64 distccd v1 ((GNU) 4.2.4 (Ubuntu 4.2.4-1ubuntu4))
| distcc-cve2004-2687: 
|   VULNERABLE:
|   distcc Daemon Command Execution
|     State: VULNERABLE (Exploitable)
|     IDs:  CVE:CVE-2004-2687
|     Risk factor: High  CVSSv2: 9.3 (HIGH) (AV:N/AC:M/Au:N/C:C/I:C/A:C)
|       Allows executing of arbitrary commands on systems running distccd 3.1 and
|       earlier. The vulnerability is the consequence of weak service configuration.
|       
|     Disclosure date: 2002-02-01
|     Extra information:
|       
|     uid=1(daemon) gid=1(daemon) groups=1(daemon)
|   
|     References:
|       https://distcc.github.io/security.html
|       https://nvd.nist.gov/vuln/detail/CVE-2004-2687
|_      https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2004-2687
MAC Address: 00:0C:29:95:39:3E (VMware)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:20:09 2025 -- 1 IP address (1 host up) scanned in 17.00 seconds

```