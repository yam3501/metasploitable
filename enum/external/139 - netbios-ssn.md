# nmap 

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:31 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp139/tcp_139_smb_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp139/xml/tcp_139_smb_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.0018s latency).
Scanned at 2025-02-08 02:17:32 EST for 436s

PORT    STATE SERVICE     REASON         VERSION
139/tcp open  netbios-ssn syn-ack ttl 64 Samba smbd 3.0.20-Debian (workgroup: WORKGROUP)
MAC Address: 00:0C:29:95:39:3E (VMware)

Host script results:
| smb-os-discovery: 
|   OS: Unix (Samba 3.0.20-Debian)
|   Computer name: metasploitable
|   NetBIOS computer name: 
|   Domain name: localdomain
|   FQDN: metasploitable.localdomain
|_  System time: 2025-02-08T02:17:47-05:00
| smb-ls: Volume \\192.168.190.129\tmp
| SIZE   TIME                 FILENAME
| <DIR>  2025-02-08T07:24:44  .
| <DIR>  2012-05-20T19:36:12  ..
| 0      2025-02-08T06:05:54  5181.jsvc_up
|_
|_smb2-capabilities: SMB 2+ not supported
|_smb-print-text: false
|_smb2-security-mode: Couldn't establish a SMBv2 connection.
|_smb-enum-sessions: ERROR: Script execution failed (use -d to debug)
|_smb2-time: Protocol negotiation failed (SMB2)
| smb-protocols: 
|   dialects: 
|_    NT LM 0.12 (SMBv1) [dangerous, but default]
| smb-enum-shares: 
|   account_used: <blank>
|   \\192.168.190.129\ADMIN$: 
|     Type: STYPE_IPC
|     Comment: IPC Service (metasploitable server (Samba 3.0.20-Debian))
|     Users: 1
|     Max Users: <unlimited>
|     Path: C:\tmp
|     Anonymous access: <none>
|   \\192.168.190.129\IPC$: 
|     Type: STYPE_IPC
|     Comment: IPC Service (metasploitable server (Samba 3.0.20-Debian))
|     Users: 1
|     Max Users: <unlimited>
|     Path: C:\tmp
|     Anonymous access: READ/WRITE
|   \\192.168.190.129\opt: 
|     Type: STYPE_DISKTREE
|     Comment: 
|     Users: 1
|     Max Users: <unlimited>
|     Path: C:\tmp
|     Anonymous access: <none>
|   \\192.168.190.129\print$: 
|     Type: STYPE_DISKTREE
|     Comment: Printer Drivers
|     Users: 1
|     Max Users: <unlimited>
|     Path: C:\var\lib\samba\printers
|     Anonymous access: <none>
|   \\192.168.190.129\tmp: 
|     Type: STYPE_DISKTREE
|     Comment: oh noes!
|     Users: 1
|     Max Users: <unlimited>
|     Path: C:\tmp
|_    Anonymous access: READ/WRITE
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| nbstat: NetBIOS name: METASPLOITABLE, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| Names:
|   METASPLOITABLE<00>   Flags: <unique><active>
|   METASPLOITABLE<03>   Flags: <unique><active>
|   METASPLOITABLE<20>   Flags: <unique><active>
|   \x01\x02__MSBROWSE__\x02<01>  Flags: <group><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WORKGROUP<1d>        Flags: <unique><active>
|   WORKGROUP<1e>        Flags: <group><active>
| Statistics:
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_  00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_smb-mbenum: ERROR: Script execution failed (use -d to debug)
|_smb-vuln-ms10-061: false
| smb-enum-users: 
|   METASPLOITABLE\backup (RID: 1068)
|     Full name:   backup
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\bin (RID: 1004)
|     Full name:   bin
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\bind (RID: 1210)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\daemon (RID: 1002)
|     Full name:   daemon
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\dhcp (RID: 1202)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\distccd (RID: 1222)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\ftp (RID: 1214)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\games (RID: 1010)
|     Full name:   games
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\gnats (RID: 1082)
|     Full name:   Gnats Bug-Reporting System (admin)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\irc (RID: 1078)
|     Full name:   ircd
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\klog (RID: 1206)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\libuuid (RID: 1200)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\list (RID: 1076)
|     Full name:   Mailing List Manager
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\lp (RID: 1014)
|     Full name:   lp
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\mail (RID: 1016)
|     Full name:   mail
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\man (RID: 1012)
|     Full name:   man
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\msfadmin (RID: 3000)
|     Full name:   msfadmin,,,
|     Flags:       Normal user account
|   METASPLOITABLE\mysql (RID: 1218)
|     Full name:   MySQL Server,,,
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\news (RID: 1018)
|     Full name:   news
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\nobody (RID: 501)
|     Full name:   nobody
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\postfix (RID: 1212)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\postgres (RID: 1216)
|     Full name:   PostgreSQL administrator,,,
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\proftpd (RID: 1226)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\proxy (RID: 1026)
|     Full name:   proxy
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\root (RID: 1000)
|     Full name:   root
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\service (RID: 3004)
|     Full name:   ,,,
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\sshd (RID: 1208)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\sync (RID: 1008)
|     Full name:   sync
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\sys (RID: 1006)
|     Full name:   sys
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\syslog (RID: 1204)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\telnetd (RID: 1224)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\tomcat55 (RID: 1220)
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\user (RID: 3002)
|     Full name:   just a user,111,,
|     Flags:       Normal user account
|   METASPLOITABLE\uucp (RID: 1020)
|     Full name:   uucp
|     Flags:       Normal user account, Account disabled
|   METASPLOITABLE\www-data (RID: 1066)
|     Full name:   www-data
|_    Flags:       Normal user account, Account disabled
|_smb-system-info: ERROR: Script execution failed (use -d to debug)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:24:48 2025 -- 1 IP address (1 host up) scanned in 437.16 seconds

```
# enum4linux-ng

```
[92mENUM4LINUX - next generation (v1.3.4)[0m

 ==========================
|    Target Information    |
 ==========================
[94m[*] Target ........... 192.168.190.129[0m
[94m[*] Username ......... ''[0m
[94m[*] Random Username .. 'tpowytbd'[0m
[94m[*] Password ......... ''[0m
[94m[*] Timeout .......... 5 second(s)[0m

 ========================================
|    Listener Scan on 192.168.190.129    |
 ========================================
[94m[*] Checking LDAP[0m
[91m[-] Could not connect to LDAP on 389/tcp: connection refused[0m
[94m[*] Checking LDAPS[0m
[91m[-] Could not connect to LDAPS on 636/tcp: connection refused[0m
[94m[*] Checking SMB[0m
[92m[+] SMB is accessible on 445/tcp[0m
[94m[*] Checking SMB over NetBIOS[0m
[92m[+] SMB over NetBIOS is accessible on 139/tcp[0m

 ==============================================================
|    NetBIOS Names and Workgroup/Domain for 192.168.190.129    |
 ==============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmp1dvtq1gy -A 192.168.190.129
[92m[+] Got domain/workgroup name: WORKGROUP[0m
[92m[+] Full NetBIOS names information:
- METASPLOITABLE  <00> -         B <ACTIVE>  Workstation Service
- METASPLOITABLE  <03> -         B <ACTIVE>  Messenger Service
- METASPLOITABLE  <20> -         B <ACTIVE>  File Server Service
- ..__MSBROWSE__. <01> - <GROUP> B <ACTIVE>  Master Browser
- WORKGROUP       <00> - <GROUP> B <ACTIVE>  Domain/Workgroup Name
- WORKGROUP       <1d> -         B <ACTIVE>  Master Browser
- WORKGROUP       <1e> - <GROUP> B <ACTIVE>  Browser Service Elections
- MAC Address = 00-00-00-00-00-00[0m

 ============================================
|    SMB Dialect Check on 192.168.190.129    |
 ============================================
[94m[*] Trying on 445/tcp[0m
[92m[+] Supported dialects and settings:
Supported dialects:
  SMB 1.0: true
  SMB 2.02: false
  SMB 2.1: false
  SMB 3.0: false
  SMB 3.1.1: false
Preferred dialect: SMB 1.0
SMB1 only: true
SMB signing required: false[0m
[94m[*] Enforcing legacy SMBv1 for further enumeration[0m

 ==============================================================
|    Domain Information via SMB session for 192.168.190.129    |
 ==============================================================
[94m[*] Enumerating via unauthenticated SMB session on 445/tcp[0m
[92m[+] Found domain information via SMB
NetBIOS computer name: METASPLOITABLE
NetBIOS domain name: ''
DNS domain: localdomain
FQDN: metasploitable.localdomain
Derived membership: workgroup member
Derived domain: unknown[0m

 ============================================
|    RPC Session Check on 192.168.190.129    |
 ============================================
[94m[*] Check for null session[0m
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c help '//192.168.190.129/ipc$'
[92m[+] Server allows session using username '', password ''[0m
[94m[*] Check for random user[0m
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U tpowytbd% -s /tmp/tmp1dvtq1gy -t 5 -c help '//192.168.190.129/ipc$'
[91m[-] Could not establish random user session: STATUS_LOGON_FAILURE[0m

 ======================================================
|    Domain Information via RPC for 192.168.190.129    |
 ======================================================
[V] Attempting to get domain SID, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c lsaquery 192.168.190.129
[92m[+] Domain: WORKGROUP[0m
[92m[+] Domain SID: NULL SID[0m
[92m[+] Membership: workgroup member[0m

 ==================================================
|    OS Information via RPC for 192.168.190.129    |
 ==================================================
[94m[*] Enumerating via unauthenticated SMB session on 445/tcp[0m
[92m[+] Found OS information via SMB[0m
[94m[*] Enumerating via 'srvinfo'[0m
[V] Attempting to get OS info with command, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c srvinfo 192.168.190.129
[92m[+] Found OS information via 'srvinfo'[0m
[92m[+] After merging OS information we have the following result:
OS: Linux/Unix (Samba 3.0.20-Debian)
OS version: '4.9'
OS release: not supported
OS build: not supported
Native OS: Unix
Native LAN manager: Samba 3.0.20-Debian
Platform id: '500'
Server type: '0x9a03'
Server type string: Wk Sv PrQ Unx NT SNT metasploitable server (Samba 3.0.20-Debian)[0m

 ========================================
|    Users via RPC on 192.168.190.129    |
 ========================================
[94m[*] Enumerating users via 'querydispinfo'[0m
[V] Attempting to get userlist, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c querydispinfo 192.168.190.129
[92m[+] Found 35 user(s) via 'querydispinfo'[0m
[94m[*] Enumerating users via 'enumdomusers'[0m
[V] Attempting to get userlist, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c enumdomusers 192.168.190.129
[92m[+] Found 35 user(s) via 'enumdomusers'[0m
[94m[*] Enumerating users details[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1010' 192.168.190.129
[92m[+] Found details for user 'games' (RID 1010)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 501' 192.168.190.129
[92m[+] Found details for user 'nobody' (RID 501)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1210' 192.168.190.129
[92m[+] Found details for user 'bind' (RID 1210)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1026' 192.168.190.129
[92m[+] Found details for user 'proxy' (RID 1026)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1204' 192.168.190.129
[92m[+] Found details for user 'syslog' (RID 1204)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 3002' 192.168.190.129
[92m[+] Found details for user 'user' (RID 3002)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1066' 192.168.190.129
[92m[+] Found details for user 'www-data' (RID 1066)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1000' 192.168.190.129
[92m[+] Found details for user 'root' (RID 1000)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1018' 192.168.190.129
[92m[+] Found details for user 'news' (RID 1018)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1216' 192.168.190.129
[92m[+] Found details for user 'postgres' (RID 1216)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1004' 192.168.190.129
[92m[+] Found details for user 'bin' (RID 1004)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1016' 192.168.190.129
[92m[+] Found details for user 'mail' (RID 1016)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1222' 192.168.190.129
[92m[+] Found details for user 'distccd' (RID 1222)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1226' 192.168.190.129
[92m[+] Found details for user 'proftpd' (RID 1226)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1202' 192.168.190.129
[92m[+] Found details for user 'dhcp' (RID 1202)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1002' 192.168.190.129
[92m[+] Found details for user 'daemon' (RID 1002)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1208' 192.168.190.129
[92m[+] Found details for user 'sshd' (RID 1208)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1012' 192.168.190.129
[92m[+] Found details for user 'man' (RID 1012)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1014' 192.168.190.129
[92m[+] Found details for user 'lp' (RID 1014)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1218' 192.168.190.129
[92m[+] Found details for user 'mysql' (RID 1218)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1082' 192.168.190.129
[92m[+] Found details for user 'gnats' (RID 1082)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1200' 192.168.190.129
[92m[+] Found details for user 'libuuid' (RID 1200)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1068' 192.168.190.129
[92m[+] Found details for user 'backup' (RID 1068)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 3000' 192.168.190.129
[92m[+] Found details for user 'msfadmin' (RID 3000)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1224' 192.168.190.129
[92m[+] Found details for user 'telnetd' (RID 1224)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1006' 192.168.190.129
[92m[+] Found details for user 'sys' (RID 1006)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1206' 192.168.190.129
[92m[+] Found details for user 'klog' (RID 1206)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1212' 192.168.190.129
[92m[+] Found details for user 'postfix' (RID 1212)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 3004' 192.168.190.129
[92m[+] Found details for user 'service' (RID 3004)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1076' 192.168.190.129
[92m[+] Found details for user 'list' (RID 1076)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1078' 192.168.190.129
[92m[+] Found details for user 'irc' (RID 1078)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1214' 192.168.190.129
[92m[+] Found details for user 'ftp' (RID 1214)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1220' 192.168.190.129
[92m[+] Found details for user 'tomcat55' (RID 1220)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1008' 192.168.190.129
[92m[+] Found details for user 'sync' (RID 1008)[0m
[V] Attempting to get detailed user info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'queryuser 1020' 192.168.190.129
[92m[+] Found details for user 'uucp' (RID 1020)[0m
[92m[+] After merging user results we have 35 user(s) total:
'1000':
  username: root
  name: root
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\root
    Dir Drive: ''
    Profile Path: \\metasploitable\root\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3e8'
    group_rid: '0x3e9'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1002':
  username: daemon
  name: daemon
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\daemon
    Dir Drive: ''
    Profile Path: \\metasploitable\daemon\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3ea'
    group_rid: '0x3eb'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1004':
  username: bin
  name: bin
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\bin
    Dir Drive: ''
    Profile Path: \\metasploitable\bin\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3ec'
    group_rid: '0x3ed'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1006':
  username: sys
  name: sys
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\sys
    Dir Drive: ''
    Profile Path: \\metasploitable\sys\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3ee'
    group_rid: '0x3ef'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1008':
  username: sync
  name: sync
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\sync
    Dir Drive: ''
    Profile Path: \\metasploitable\sync\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3f0'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1010':
  username: games
  name: games
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\games
    Dir Drive: ''
    Profile Path: \\metasploitable\games\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3f2'
    group_rid: '0x461'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1012':
  username: man
  name: man
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\man
    Dir Drive: ''
    Profile Path: \\metasploitable\man\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3f4'
    group_rid: '0x401'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1014':
  username: lp
  name: lp
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\lp
    Dir Drive: ''
    Profile Path: \\metasploitable\lp\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3f6'
    group_rid: '0x3f7'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1016':
  username: mail
  name: mail
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\mail
    Dir Drive: ''
    Profile Path: \\metasploitable\mail\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3f8'
    group_rid: '0x3f9'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1018':
  username: news
  name: news
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\news
    Dir Drive: ''
    Profile Path: \\metasploitable\news\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3fa'
    group_rid: '0x3fb'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1020':
  username: uucp
  name: uucp
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\uucp
    Dir Drive: ''
    Profile Path: \\metasploitable\uucp\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x3fc'
    group_rid: '0x3fd'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1026':
  username: proxy
  name: proxy
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\proxy
    Dir Drive: ''
    Profile Path: \\metasploitable\proxy\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x402'
    group_rid: '0x403'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1066':
  username: www-data
  name: www-data
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\www-data
    Dir Drive: ''
    Profile Path: \\metasploitable\www-data\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x42a'
    group_rid: '0x42b'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1068':
  username: backup
  name: backup
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\backup
    Dir Drive: ''
    Profile Path: \\metasploitable\backup\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x42c'
    group_rid: '0x42d'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1076':
  username: list
  name: Mailing List Manager
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\list
    Dir Drive: ''
    Profile Path: \\metasploitable\list\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x434'
    group_rid: '0x435'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1078':
  username: irc
  name: ircd
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\irc
    Dir Drive: ''
    Profile Path: \\metasploitable\irc\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x436'
    group_rid: '0x437'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1082':
  username: gnats
  name: Gnats Bug-Reporting System (admin)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\gnats
    Dir Drive: ''
    Profile Path: \\metasploitable\gnats\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x43a'
    group_rid: '0x43b'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1200':
  username: libuuid
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\libuuid
    Dir Drive: ''
    Profile Path: \\metasploitable\libuuid\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4b0'
    group_rid: '0x4b3'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1202':
  username: dhcp
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\dhcp
    Dir Drive: ''
    Profile Path: \\metasploitable\dhcp\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4b2'
    group_rid: '0x4b5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1204':
  username: syslog
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\syslog
    Dir Drive: ''
    Profile Path: \\metasploitable\syslog\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4b4'
    group_rid: '0x4b7'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1206':
  username: klog
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\klog
    Dir Drive: ''
    Profile Path: \\metasploitable\klog\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4b6'
    group_rid: '0x4b9'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1208':
  username: sshd
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\sshd
    Dir Drive: ''
    Profile Path: \\metasploitable\sshd\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4b8'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1210':
  username: bind
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\bind
    Dir Drive: ''
    Profile Path: \\metasploitable\bind\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4ba'
    group_rid: '0x4cb'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1212':
  username: postfix
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\postfix
    Dir Drive: ''
    Profile Path: \\metasploitable\postfix\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4bc'
    group_rid: '0x4cf'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1214':
  username: ftp
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\ftp
    Dir Drive: ''
    Profile Path: \\metasploitable\ftp\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4be'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1216':
  username: postgres
  name: PostgreSQL administrator,,,
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\postgres
    Dir Drive: ''
    Profile Path: \\metasploitable\postgres\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4c0'
    group_rid: '0x4d3'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1218':
  username: mysql
  name: MySQL Server,,,
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\mysql
    Dir Drive: ''
    Profile Path: \\metasploitable\mysql\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4c2'
    group_rid: '0x4d5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1220':
  username: tomcat55
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\tomcat55
    Dir Drive: ''
    Profile Path: \\metasploitable\tomcat55\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4c4'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1222':
  username: distccd
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\distccd
    Dir Drive: ''
    Profile Path: \\metasploitable\distccd\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4c6'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1224':
  username: telnetd
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\telnetd
    Dir Drive: ''
    Profile Path: \\metasploitable\telnetd\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4c8'
    group_rid: '0x4d9'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'1226':
  username: proftpd
  name: (null)
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\proftpd
    Dir Drive: ''
    Profile Path: \\metasploitable\proftpd\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x4ca'
    group_rid: '0x203e5'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'3000':
  username: msfadmin
  name: msfadmin,,,
  acb: '0x00000010'
  description: (null)
  details:
    Home Drive: \\metasploitable\msfadmin
    Dir Drive: ''
    Profile Path: \\metasploitable\msfadmin\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 28 Apr 2010 03:56:18 EDT
    Password can change Time: Wed, 28 Apr 2010 03:56:18 EDT
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0xbb8'
    group_rid: '0xbb9'
    acb_info: '0x00000010'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: false
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'3002':
  username: user
  name: just a user,111,,
  acb: '0x00000010'
  description: (null)
  details:
    Home Drive: \\metasploitable\user
    Dir Drive: ''
    Profile Path: \\metasploitable\user\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Mon, 17 May 2010 22:39:25 EDT
    Password can change Time: Mon, 17 May 2010 22:39:25 EDT
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0xbba'
    group_rid: '0xbbb'
    acb_info: '0x00000010'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: false
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'3004':
  username: service
  name: ',,,'
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\service
    Dir Drive: ''
    Profile Path: \\metasploitable\service\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0xbbc'
    group_rid: '0xbbd'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false
'501':
  username: nobody
  name: nobody
  acb: '0x00000011'
  description: (null)
  details:
    Home Drive: \\metasploitable\nobody
    Dir Drive: ''
    Profile Path: \\metasploitable\nobody\profile
    Logon Script: ''
    Description: ''
    Workstations: ''
    Comment: (null)
    Remote Dial: ''
    Logon Time: Wed, 31 Dec 1969 19:00:00 EST
    Logoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Kickoff Time: Wed, 13 Sep 30828 22:48:05 EDT
    Password last set Time: Wed, 31 Dec 1969 19:00:00 EST
    Password can change Time: Wed, 31 Dec 1969 19:00:00 EST
    Password must change Time: Wed, 13 Sep 30828 22:48:05 EDT
    unknown_2[0..31]: ''
    user_rid: '0x1f5'
    group_rid: '0x202'
    acb_info: '0x00000011'
    fields_present: '0x00ffffff'
    logon_divs: '168'
    bad_password_count: '0x00000000'
    logon_count: '0x00000000'
    padding1[0..7]: ''
    logon_hrs[0..21]: ''
    Account Disabled: true
    Password not expired: false
    Account locked out: false
    Password expired: false
    Interdomain trust account: false
    Workstation trust account: false
    Server trust account: false
    Trusted for delegation: false[0m

 =========================================
|    Groups via RPC on 192.168.190.129    |
 =========================================
[94m[*] Enumerating local groups[0m
[V] Attempting to get local groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'enumalsgroups domain' 192.168.190.129
[92m[+] Found 0 group(s) via 'enumalsgroups domain'[0m
[94m[*] Enumerating builtin groups[0m
[V] Attempting to get builtin groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c 'enumalsgroups builtin' 192.168.190.129
[92m[+] Found 0 group(s) via 'enumalsgroups builtin'[0m
[94m[*] Enumerating domain groups[0m
[V] Attempting to get domain groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c enumdomgroups 192.168.190.129
[92m[+] Found 0 group(s) via 'enumdomgroups'[0m

 =========================================
|    Shares via RPC on 192.168.190.129    |
 =========================================
[V] Attempting to get share list using authentication, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -L //192.168.190.129 -g
[94m[*] Enumerating shares[0m
[92m[+] Found 5 share(s):
ADMIN$:
  comment: IPC Service (metasploitable server (Samba 3.0.20-Debian))
  type: IPC
IPC$:
  comment: IPC Service (metasploitable server (Samba 3.0.20-Debian))
  type: IPC
opt:
  comment: ''
  type: Disk
print$:
  comment: Printer Drivers
  type: Disk
tmp:
  comment: oh noes!
  type: Disk[0m
[94m[*] Testing share ADMIN$[0m
[V] Attempting to map share //192.168.190.129/ADMIN$, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c dir '//192.168.190.129/ADMIN$'
[92m[+] Mapping: DENIED, Listing: N/A[0m
[94m[*] Testing share IPC$[0m
[V] Attempting to map share //192.168.190.129/IPC$, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c dir '//192.168.190.129/IPC$'
[92m[+] Mapping: OK, Listing: NOT SUPPORTED[0m
[94m[*] Testing share opt[0m
[V] Attempting to map share //192.168.190.129/opt, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c dir //192.168.190.129/opt
[92m[+] Mapping: DENIED, Listing: N/A[0m
[94m[*] Testing share print$[0m
[V] Attempting to map share //192.168.190.129/print$, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c dir '//192.168.190.129/print$'
[92m[+] Mapping: DENIED, Listing: N/A[0m
[94m[*] Testing share tmp[0m
[V] Attempting to map share //192.168.190.129/tmp, running command: smbclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -t 5 -c dir //192.168.190.129/tmp
[92m[+] Mapping: OK, Listing: OK[0m

 ============================================
|    Policies via RPC for 192.168.190.129    |
 ============================================
[94m[*] Trying port 445/tcp[0m
[91m[-] SMB connection error on port 445/tcp: STATUS_ACCESS_DENIED[0m
[94m[*] Trying port 139/tcp[0m
[91m[-] SMB connection error on port 139/tcp: STATUS_ACCESS_DENIED[0m

 ============================================
|    Printers via RPC for 192.168.190.129    |
 ============================================
[V] Attempting to get printer info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmp1dvtq1gy -c enumprinters 192.168.190.129
[92m[+] No printers returned (this is not an error)[0m

Completed after 16.49 seconds


```
# smbclient

```
Anonymous login successful

	Sharename       Type      Comment
	---------       ----      -------
	print$          Disk      Printer Drivers
	tmp             Disk      oh noes!
	opt             Disk
	IPC$            IPC       IPC Service (metasploitable server (Samba 3.0.20-Debian))
	ADMIN$          IPC       IPC Service (metasploitable server (Samba 3.0.20-Debian))
Reconnecting with SMB1 for workgroup listing.
Anonymous login successful

	Server               Comment
	---------            -------

	Workgroup            Master
	---------            -------
	WORKGROUP            METASPLOITABLE

```
# netexec 

```

```
# enumeration

## anon



## with credentials

