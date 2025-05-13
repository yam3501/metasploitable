# nmap 

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:30 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 22 --script=banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp22/tcp_22_ssh_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp22/xml/tcp_22_ssh_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00081s latency).
Scanned at 2025-02-08 02:17:31 EST for 2s

PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 64 OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)
| ssh2-enum-algos: 
|   kex_algorithms: (4)
|       diffie-hellman-group-exchange-sha256
|       diffie-hellman-group-exchange-sha1
|       diffie-hellman-group14-sha1
|       diffie-hellman-group1-sha1
|   server_host_key_algorithms: (2)
|       ssh-rsa
|       ssh-dss
|   encryption_algorithms: (13)
|       aes128-cbc
|       3des-cbc
|       blowfish-cbc
|       cast128-cbc
|       arcfour128
|       arcfour256
|       arcfour
|       aes192-cbc
|       aes256-cbc
|       rijndael-cbc@lysator.liu.se
|       aes128-ctr
|       aes192-ctr
|       aes256-ctr
|   mac_algorithms: (7)
|       hmac-md5
|       hmac-sha1
|       umac-64@openssh.com
|       hmac-ripemd160
|       hmac-ripemd160@openssh.com
|       hmac-sha1-96
|       hmac-md5-96
|   compression_algorithms: (2)
|       none
|_      zlib@openssh.com
|_banner: SSH-2.0-OpenSSH_4.7p1 Debian-8ubuntu1
| ssh-hostkey: 
|   1024 60:0f:cf:e1:c0:5f:6a:74:d6:90:24:fa:c4:d5:6c:cd (DSA)
| ssh-dss AAAAB3NzaC1kc3MAAACBALz4hsc8a2Srq4nlW960qV8xwBG0JC+jI7fWxm5METIJH4tKr/xUTwsTYEYnaZLzcOiy21D3ZvOwYb6AA3765zdgCd2Tgand7F0YD5UtXG7b7fbz99chReivL0SIWEG/E96Ai+pqYMP2WD5KaOJwSIXSUajnU5oWmY5x85sBw+XDAAAAFQDFkMpmdFQTF+oRqaoSNVU7Z+hjSwAAAIBCQxNKzi1TyP+QJIFa3M0oLqCVWI0We/ARtXrzpBOJ/dt0hTJXCeYisKqcdwdtyIn8OUCOyrIjqNuA2QW217oQ6wXpbFh+5AQm8Hl3b6C6o8lX3Ptw+Y4dp0lzfWHwZ/jzHwtuaDQaok7u1f971lEazeJLqfiWrAzoklqSWyDQJAAAAIA1lAD3xWYkeIeHv/R3P9i+XaoI7imFkMuYXCDTq843YU6Td+0mWpllCqAWUV/CQamGgQLtYy5S0ueoks01MoKdOMMhKVwqdr08nvCBdNKjIEd3gH6oBk/YRnjzxlEAYBsvCmM4a0jmhz0oNiRWlc/F+bkUeFKrBx/D2fdfZmhrGg==
|   2048 56:56:24:0f:21:1d:de:a7:2b:ae:61:b1:24:3d:e8:f3 (RSA)
|_ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAstqnuFMBOZvO3WTEjP4TUdjgWkIVNdTq6kboEDjteOfc65TlI7sRvQBwqAhQjeeyyIk8T55gMDkOD0akSlSXvLDcmcdYfxeIF0ZSuT+nkRhij7XSSA/Oc5QSk3sJ/SInfb78e3anbRHpmkJcVgETJ5WhKObUNf1AKZW++4Xlc63M4KI5cjvMMIPEVOyR3AKmI78Fo3HJjYucg87JjLeC66I7+dlEYX6zT8i1XYwa/L1vZ3qSJISGVu8kRPikMv/cNSvki4j+qDYyZ2E5497W87+Ed46/8P42LNGoOV8OcX/ro6pAcbEPUdUEfkJrqi2YXbhvwIJ0gFMb6wfe5cnQew==
| ssh-auth-methods: 
|   Supported authentication methods: 
|     publickey
|_    password
MAC Address: 00:0C:29:95:39:3E (VMware)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:33 2025 -- 1 IP address (1 host up) scanned in 2.79 seconds

```
# ssh-audit

```
# general
(gen) banner: SSH-2.0-OpenSSH_4.7p1 Debian-8ubuntu1
(gen) software: OpenSSH 4.7p1
(gen) compatibility: OpenSSH 4.7-6.6, Dropbear SSH 0.53+ (some functionality from 0.52)
(gen) compression: enabled (zlib@openssh.com)

# key exchange algorithms
(kex) diffie-hellman-group-exchange-sha256 (1024-bit) -- [fail] using small 1024-bit modulus
                                                      `- [info] available since OpenSSH 4.4
(kex) diffie-hellman-group-exchange-sha1 (1024-bit) -- [fail] using small 1024-bit modulus
                                                    `- [info] available since OpenSSH 2.3.0
(kex) diffie-hellman-group14-sha1           -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 3.9, Dropbear SSH 0.53
(kex) diffie-hellman-group1-sha1            -- [fail] using small 1024-bit modulus
                                            `- [fail] vulnerable to the Logjam attack: https://en.wikipedia.org/wiki/Logjam_(computer_security)
                                            `- [fail] using broken SHA-1 hash algorithm
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.28
                                            `- [info] removed in OpenSSH 6.9: https://www.openssh.com/txt/release-6.9

# host-key algorithms
(key) ssh-rsa (2048-bit)                    -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] 2048-bit modulus only provides 112-bits of symmetric strength
                                            `- [info] available since OpenSSH 2.5.0, Dropbear SSH 0.28
                                            `- [info] deprecated in OpenSSH 8.8: https://www.openssh.com/txt/release-8.8
(key) ssh-dss                               -- [fail] using small 1024-bit modulus
                                            `- [warn] using weak random number generator could reveal the key
                                            `- [info] available since OpenSSH 2.1.0, Dropbear SSH 0.28
                                            `- [info] disabled in OpenSSH 7.0: https://www.openssh.com/txt/release-7.0

# encryption algorithms (ciphers)
(enc) aes128-cbc                            -- [warn] using weak cipher mode
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.28
(enc) 3des-cbc                              -- [fail] using broken & deprecated 3DES cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [info] available since OpenSSH 1.2.2, Dropbear SSH 0.28
(enc) blowfish-cbc                          -- [fail] using weak & deprecated Blowfish cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [info] available since OpenSSH 1.2.2, Dropbear SSH 0.28
(enc) cast128-cbc                           -- [fail] using weak & deprecated CAST cipher
                                            `- [warn] using weak cipher mode
                                            `- [warn] using small 64-bit block size
                                            `- [info] available since OpenSSH 2.1.0
(enc) arcfour128                            -- [fail] using broken RC4 cipher
                                            `- [info] available since OpenSSH 4.2
(enc) arcfour256                            -- [fail] using broken RC4 cipher
                                            `- [info] available since OpenSSH 4.2
(enc) arcfour                               -- [fail] using broken RC4 cipher
                                            `- [info] available since OpenSSH 2.1.0
(enc) aes192-cbc                            -- [warn] using weak cipher mode
                                            `- [info] available since OpenSSH 2.3.0
(enc) aes256-cbc                            -- [warn] using weak cipher mode
                                            `- [info] available since OpenSSH 2.3.0, Dropbear SSH 0.47
(enc) rijndael-cbc@lysator.liu.se           -- [fail] using deprecated & non-standardized Rijndael cipher
                                            `- [warn] using weak cipher mode
                                            `- [info] available since OpenSSH 2.3.0
                                            `- [info] disabled in OpenSSH 7.0: https://www.openssh.com/txt/release-7.0
(enc) aes128-ctr                            -- [info] available since OpenSSH 3.7, Dropbear SSH 0.52
(enc) aes192-ctr                            -- [info] available since OpenSSH 3.7
(enc) aes256-ctr                            -- [info] available since OpenSSH 3.7, Dropbear SSH 0.52

# message authentication code algorithms
(mac) hmac-md5                              -- [fail] using broken MD5 hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.1.0, Dropbear SSH 0.28
(mac) hmac-sha1                             -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.1.0, Dropbear SSH 0.28
(mac) umac-64@openssh.com                   -- [warn] using encrypt-and-MAC mode
                                            `- [warn] using small 64-bit tag size
                                            `- [info] available since OpenSSH 4.7
(mac) hmac-ripemd160                        -- [fail] using deprecated RIPEMD hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.5.0
(mac) hmac-ripemd160@openssh.com            -- [fail] using deprecated RIPEMD hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.1.0
(mac) hmac-sha1-96                          -- [fail] using broken SHA-1 hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.5.0, Dropbear SSH 0.47
(mac) hmac-md5-96                           -- [fail] using broken MD5 hash algorithm
                                            `- [warn] using encrypt-and-MAC mode
                                            `- [info] available since OpenSSH 2.5.0

# fingerprints
(fin) ssh-rsa: SHA256:BQHm5EoHX9GCiOLuVscegPXLQOsuPs+E9d/rrJB84rk

# algorithm recommendations (for OpenSSH 4.7)
(rec) !diffie-hellman-group-exchange-sha256 -- kex algorithm to change (increase modulus size to 3072 bits or larger) 
(rec) -3des-cbc                             -- enc algorithm to remove 
(rec) -arcfour                              -- enc algorithm to remove 
(rec) -arcfour128                           -- enc algorithm to remove 
(rec) -arcfour256                           -- enc algorithm to remove 
(rec) -blowfish-cbc                         -- enc algorithm to remove 
(rec) -cast128-cbc                          -- enc algorithm to remove 
(rec) -diffie-hellman-group-exchange-sha1   -- kex algorithm to remove 
(rec) -diffie-hellman-group1-sha1           -- kex algorithm to remove 
(rec) -diffie-hellman-group14-sha1          -- kex algorithm to remove 
(rec) -hmac-md5                             -- mac algorithm to remove 
(rec) -hmac-md5-96                          -- mac algorithm to remove 
(rec) -hmac-ripemd160                       -- mac algorithm to remove 
(rec) -hmac-ripemd160@openssh.com           -- mac algorithm to remove 
(rec) -hmac-sha1                            -- mac algorithm to remove 
(rec) -hmac-sha1-96                         -- mac algorithm to remove 
(rec) -rijndael-cbc@lysator.liu.se          -- enc algorithm to remove 
(rec) -ssh-dss                              -- key algorithm to remove 
(rec) -ssh-rsa                              -- key algorithm to remove 
(rec) -aes128-cbc                           -- enc algorithm to remove 
(rec) -aes192-cbc                           -- enc algorithm to remove 
(rec) -aes256-cbc                           -- enc algorithm to remove 
(rec) -umac-64@openssh.com                  -- mac algorithm to remove 

# additional info
(nfo) For hardening guides on common OSes, please see: <https://www.ssh-audit.com/hardening_guides.html>
(nfo) Potentially insufficient connection throttling detected, resulting in possible vulnerability to the DHEat DoS attack (CVE-2002-20001).  38 connections were created in 0.082 seconds, or 462.1 conns/sec; server must respond with a rate less than 20.0 conns/sec per IPv4/IPv6 source address to be considered safe.  For rate-throttling options, please see <https://www.ssh-audit.com/hardening_guides.html>.  Be aware that using 'PerSourceMaxStartups 1' properly protects the server from this attack, but will cause this test to yield a false positive.  Suppress this test and message with the --skip-rate-test option.
```
