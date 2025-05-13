# nmap

```
# Nmap 7.94SVN scan initiated Sat Feb  8 02:17:30 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp53/tcp_53_dns_nmap.txt -oX /home/kali/target/metasploitable2/__playground__/results/192.168.190.129/scans/tcp53/xml/tcp_53_dns_nmap.xml 192.168.190.129
Nmap scan report for 192.168.190.129
Host is up, received arp-response (0.00034s latency).
Scanned at 2025-02-08 02:17:31 EST for 21s

PORT   STATE SERVICE REASON         VERSION
53/tcp open  domain  syn-ack ttl 64 ISC BIND 9.4.2
| dns-nsid: 
|_  bind.version: 9.4.2
|_dns-nsec3-enum: Can't determine domain for host 192.168.190.129; use dns-nsec3-enum.domains script arg.
|_dns-nsec-enum: Can't determine domain for host 192.168.190.129; use dns-nsec-enum.domains script arg.
MAC Address: 00:0C:29:95:39:3E (VMware)

Host script results:
|_dns-brute: Can't guess domain of "192.168.190.129"; use dns-brute.domain script argument.

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Feb  8 02:17:52 2025 -- 1 IP address (1 host up) scanned in 22.05 seconds

```
# dig reverse lookup

```

; <<>> DiG 9.20.2-1-Debian <<>> -p 53 -x 192.168.190.129 @192.168.190.129
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 37720
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 1, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;129.190.168.192.in-addr.arpa.	IN	PTR

;; AUTHORITY SECTION:
168.192.in-addr.arpa.	10800	IN	SOA	prisoner.iana.org. hostmaster.root-servers.org. 1 604800 60 604800 604800

;; Query time: 4831 msec
;; SERVER: 192.168.190.129#53(192.168.190.129) (UDP)
;; WHEN: Sat Feb 08 02:17:35 EST 2025
;; MSG SIZE  rcvd: 134

```
# dig zone transfer

```

; <<>> DiG 9.20.2-1-Debian <<>> AXFR -p 53 @192.168.190.129
; (1 server found)
;; global options: +cmd
.			518400	IN	NS	g.root-servers.net.
.			518400	IN	NS	l.root-servers.net.
.			518400	IN	NS	e.root-servers.net.
.			518400	IN	NS	k.root-servers.net.
.			518400	IN	NS	f.root-servers.net.
.			518400	IN	NS	c.root-servers.net.
.			518400	IN	NS	h.root-servers.net.
.			518400	IN	NS	a.root-servers.net.
.			518400	IN	NS	d.root-servers.net.
.			518400	IN	NS	m.root-servers.net.
.			518400	IN	NS	i.root-servers.net.
.			518400	IN	NS	b.root-servers.net.
.			518400	IN	NS	j.root-servers.net.
a.root-servers.net.	518400	IN	A	198.41.0.4
a.root-servers.net.	518400	IN	AAAA	2001:503:ba3e::2:30
b.root-servers.net.	518400	IN	A	170.247.170.2
b.root-servers.net.	518400	IN	AAAA	2801:1b8:10::b
c.root-servers.net.	518400	IN	A	192.33.4.12
c.root-servers.net.	518400	IN	AAAA	2001:500:2::c
d.root-servers.net.	518400	IN	A	199.7.91.13
d.root-servers.net.	518400	IN	AAAA	2001:500:2d::d
e.root-servers.net.	518400	IN	A	192.203.230.10
e.root-servers.net.	518400	IN	AAAA	2001:500:a8::e
f.root-servers.net.	518400	IN	A	192.5.5.241
f.root-servers.net.	518400	IN	AAAA	2001:500:2f::f
g.root-servers.net.	518400	IN	A	192.112.36.4
g.root-servers.net.	518400	IN	AAAA	2001:500:12::d0d
h.root-servers.net.	518400	IN	A	198.97.190.53
h.root-servers.net.	518400	IN	AAAA	2001:500:1::53
i.root-servers.net.	518400	IN	A	192.36.148.17
i.root-servers.net.	518400	IN	AAAA	2001:7fe::53
j.root-servers.net.	518400	IN	A	192.58.128.30
j.root-servers.net.	518400	IN	AAAA	2001:503:c27::2:30
k.root-servers.net.	518400	IN	A	193.0.14.129
k.root-servers.net.	518400	IN	AAAA	2001:7fd::1
l.root-servers.net.	518400	IN	A	199.7.83.42
l.root-servers.net.	518400	IN	AAAA	2001:500:9f::42
m.root-servers.net.	518400	IN	A	202.12.27.33
m.root-servers.net.	518400	IN	AAAA	2001:dc3::35
;; Query time: 83 msec
;; SERVER: 192.168.190.129#53(192.168.190.129) (UDP)
;; WHEN: Sat Feb 08 02:17:31 EST 2025
;; MSG SIZE  rcvd: 811

```
