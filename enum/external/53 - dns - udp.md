# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:21:14 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sU -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/udp53/udp_53_dns_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/udp53/xml/udp_53_dns_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00087s latency).
Scanned at 2025-02-08 02:21:14 EST for 1s

PORT   STATE SERVICE REASON              VERSION
53/udp open  domain  udp-response ttl 64 ISC BIND 9.4.2
| dns-cache-snoop: 1 of 100 tested domains are cached.
|_www.wikipedia.org
|_dns-nsec3-enum: Can't determine domain for host 192.168.190.129; use dns-nsec3-enum.domains script arg.
|_dns-nsec-enum: Can't determine domain for host 192.168.190.129; use dns-nsec-enum.domains script arg.
|_dns-recursion: Recursion appears to be enabled
| dns-nsid: 
|_  bind.version: 9.4.2
MAC Address: 00:0C:29:95:39:3E (VMware)

Host script results:
|_dns-brute: Can't guess domain of "192.168.190.129"; use dns-brute.domain script argument.

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:21:15 2025 -- 1 IP address (1 host up) scanned in 1.63 seconds

```
# dig reverse lookup

```

; <<>> DiG 9.20.2-1-Debian <<>> -p 53 -x 192.168.190.129 @192.168.190.129
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 36105
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 1, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;129.190.168.192.in-addr.arpa.	IN	PTR

;; AUTHORITY SECTION:
168.192.in-addr.arpa.	10582	IN	SOA	prisoner.iana.org. hostmaster.root-servers.org. 1 604800 60 604800 604800

;; Query time: 3 msec
;; SERVER: 192.168.190.129#53(192.168.190.129) (UDP)
;; WHEN: Sat Feb 08 02:21:14 EST 2025
;; MSG SIZE  rcvd: 134

```
# dig zone transfer

```

; <<>> DiG 9.20.2-1-Debian <<>> AXFR -p 53 @192.168.190.129
; (1 server found)
;; global options: +cmd
.			518177	IN	NS	e.root-servers.net.
.			518177	IN	NS	f.root-servers.net.
.			518177	IN	NS	d.root-servers.net.
.			518177	IN	NS	l.root-servers.net.
.			518177	IN	NS	m.root-servers.net.
.			518177	IN	NS	h.root-servers.net.
.			518177	IN	NS	c.root-servers.net.
.			518177	IN	NS	j.root-servers.net.
.			518177	IN	NS	k.root-servers.net.
.			518177	IN	NS	a.root-servers.net.
.			518177	IN	NS	g.root-servers.net.
.			518177	IN	NS	b.root-servers.net.
.			518177	IN	NS	i.root-servers.net.
a.root-servers.net.	518177	IN	A	198.41.0.4
a.root-servers.net.	518177	IN	AAAA	2001:503:ba3e::2:30
b.root-servers.net.	518177	IN	A	170.247.170.2
b.root-servers.net.	518177	IN	AAAA	2801:1b8:10::b
c.root-servers.net.	518177	IN	A	192.33.4.12
c.root-servers.net.	518177	IN	AAAA	2001:500:2::c
d.root-servers.net.	518177	IN	A	199.7.91.13
d.root-servers.net.	518177	IN	AAAA	2001:500:2d::d
e.root-servers.net.	518177	IN	A	192.203.230.10
e.root-servers.net.	518177	IN	AAAA	2001:500:a8::e
f.root-servers.net.	518177	IN	A	192.5.5.241
f.root-servers.net.	518177	IN	AAAA	2001:500:2f::f
g.root-servers.net.	518177	IN	A	192.112.36.4
g.root-servers.net.	518177	IN	AAAA	2001:500:12::d0d
h.root-servers.net.	518177	IN	A	198.97.190.53
h.root-servers.net.	518177	IN	AAAA	2001:500:1::53
i.root-servers.net.	518177	IN	A	192.36.148.17
i.root-servers.net.	518177	IN	AAAA	2001:7fe::53
j.root-servers.net.	518177	IN	A	192.58.128.30
j.root-servers.net.	518177	IN	AAAA	2001:503:c27::2:30
k.root-servers.net.	518177	IN	A	193.0.14.129
k.root-servers.net.	518177	IN	AAAA	2001:7fd::1
l.root-servers.net.	518177	IN	A	199.7.83.42
l.root-servers.net.	518177	IN	AAAA	2001:500:9f::42
m.root-servers.net.	518177	IN	A	202.12.27.33
m.root-servers.net.	518177	IN	AAAA	2001:dc3::35
;; Query time: 3 msec
;; SERVER: 192.168.190.129#53(192.168.190.129) (UDP)
;; WHEN: Sat Feb 08 02:21:14 EST 2025
;; MSG SIZE  rcvd: 811

```
