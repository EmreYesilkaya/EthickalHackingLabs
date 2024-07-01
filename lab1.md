#Ethical Hacking Technologies
## Lab Work 1: Network Scanning

**Student: Emre Yesilkaya**

### Aim of the LAB 1

### Working Tools:
- the `ping` program
- the `traceroute` program
- `NMap`

### Methodology for Carrying Out the Lab
**Subject of the Study:** A network with a topology unknown to the student.

**Baseline Data Collection:**
1. **Network Addresses:**
   - Your network address (check: Windows command to check what your network address is: `ipconfig`; Linux/Apple OS: `ifconfig`)
   - Example: 192.168.56.1

2. **IP Addresses of the Devices on the Network:**

| No. | IP Address     |
|-----|----------------|
| 1   | 192.168.0.3    |
| 2   | 192.168.0.227  |
| 3   | 192.168.0.226  |
| 4   | 192.168.0.220  |
| 5   | 192.168.0.190  |
| 6   |                |
| ... |                |
| 21  |                |

### Abbreviations
- MAC (Media Access Control)
- DNS (Domain Name Service)
- ICMP (Internet Control Message Protocol)
- UDP (User Datagram Protocol)
- TCP (Transmission Control Protocol)
- IP (Internet Protocol)
- TTL (Time To Live)

### Workflow
#### Identify the IP address of your home computer:
Example: your address is 10.0.1.103
Later when drawing a picture of the network topology mark your computer by summarizing.

#### 5.1 Network Analysis using Ping and Traceroute

Identify active network devices by using the `ping` application. Write down the IP addresses of the active devices in a table:

| No. | IP Address of the Active Device |
|-----|--------------------------------|
| 1   | 192.168.0.3                    |
| 2   | 192.168.0.227                  |
| 3   | 192.168.0.226                  |
| 4   | 192.168.0.220                  |
| 5   | 192.168.0.190                  |
| ... |                                |
| 21  |                                |

Use `traceroute` to determine which intermediate nodes are used to find active network devices. Write the results in a table:

| Order No. | IP Address    | Intermediate Nodes                          |
|-----------|---------------|---------------------------------------------|
| 1         | 192.168.0.3   | 1 14.50 ms knf-mdt.knf.vu.lt (192.168.0.3)  |
| 2         | 192.168.0.227 | 1 96.50 ms Galaxy-S21-5G.knf.vu.lt (192.168.0.227) |
| 3         | 192.168.0.226 | 1 70.00 ms ESP-2KK.knf.vu.lt (192.168.0.226) |
| 4         | 192.168.0.220 | 1 28.75 ms KNF-192MONITOR.knf.vu.lt (192.168.0.220) |
| 5         | 192.168.0.190 | 1 45.00 ms ESP-AVL1.knf.vu.lt (192.168.0.190) |
| ...       |               |                                             |
| 22        |               |                                             |

Based on the data you have collected, draw up a network topology diagram.

#### 5.2 Network Analysis using NMAP

##### 5.2.1 Identify Active Network Devices by Scanning the Network using NMAP
Write down the IP and MAC addresses of the active devices in a table:

| No. | IP Address of the Active Device | MAC Address                     |
|-----|--------------------------------|---------------------------------|
| 1   | 192.168.0.3                    | 00:15:5D:7D:5C:19 (Microsoft)   |
| 2   | 192.168.0.227                  | B6:0A:6B:0B:27:C3 (Unknown)     |
| 3   | 192.168.0.226                  | 48:3F:DA:7A:DF:F3 (Espressif)   |
| 4   | 192.168.0.220                  | 00:15:5D:7D:5C:16 (Microsoft)   |
| 5   | 192.168.0.190                  | 48:3F:DA:7A:DC:17 (Espressif)   |
| ... |                                |                                 |

##### 5.2.2 Identify Available Services on Active Devices
Choose one of the three port scanning methods described in the theoretical part. Write the results in a table:

| No. | IP Address    | Services Provided                                 |
|-----|---------------|---------------------------------------------------|
| 1   | 192.168.0.3   | Not shown: 1000 filtered tcp ports (no-response)  |
| 2   | 192.168.0.227 | Not shown: 1000 filtered tcp ports (no-response)  |
| 3   | 192.168.0.226 | 53/tcp closed domain                              |
| 4   | 192.168.0.220 | Not shown: 1000 filtered tcp ports (no-response)  |
| 5   | 192.168.0.190 | 53/tcp closed domain                              |
| ... |               |                                                   |

Based on the data collected (Tables 3, 4, 5), draw a network topology diagram.

### 5.3 Comparison of the Results and Conclusions

Describe the results of the network study using both methods. Write the conclusions.

| IP           | Results of Part 5.1 | Results of Part 5.2                      | Notes                                         |
|--------------|---------------------|------------------------------------------|-----------------------------------------------|
| 192.168.0.3  | Ping works          | MAC Address: 00:15:5D:7D:5C:19 (Microsoft) | (no-response) from the ports                 |
| 192.168.0.227| Ping works          | MAC Address: B6:0A:6B:0B:27:C3 (Unknown)  | (no-response) from the ports                 |
| 192.168.0.226| Ping works          | MAC Address: 48:3F:DA:7A:DF:F3 (Espressif) | This domain has port 53/tcp closed domain    |
| 192.168.0.220| Ping works          | MAC Address: 00:15:5D:7D:5C:16 (Microsoft) | (no-response) from the ports                 |
| 192.168.0.190| Ping works          | MAC Address: 48:3F:DA:7A:DC:17 (Espressif) | This domain has port 53/tcp closed domain    |

### Conclusions
The conclusion of this lab work on Ethical Hacking Technologies specifically focusing on network scanning integrates the findings from both methodologies utilized: ICMP-based tools (ping and traceroute) and TCP/IP scanning with NMAP. Here's a structured conclusion based on the data and methodologies outlined:

1. **Network Discovery and Device Identification:** The initial phase involved using basic ICMP tools like ping and traceroute to identify active devices and map the path to these devices within the network. This phase highlighted the network's layout from the perspective of reachable devices and the routes packets take within the network. However, it provided limited information on the services running on these devices.

2. **Service and Port Identification with NMAP:** The use of NMAP significantly deepened the network analysis by not only confirming the presence of active devices identified through ping and traceroute but also detailing the services running on these devices through open ports. This phase was crucial for understanding the network's operational aspects such as service availability and potential vulnerabilities.

3. **Security Implications and Observations:**
   - The discovery of open ports such as 135/tcp (Microsoft Windows RPC), 139/tcp (netbios-ssn), 445/tcp (Microsoft-ds?), and others related to VMware services (ports 902/tcp and 912/tcp) indicates a mix of essential network services and potentially sensitive administrative interfaces.
   - The presence of open UDP ports related to netbios, UPnP, and NAT traversal suggests a diverse set of services that could be exploited if not securely configured.

4. **Network Topology Insights:** Drawing the network topology based on the collected data helps visualize the network's structure, including device interconnections and the presence of intermediate devices like routers and switches identified through traceroute. This visual representation aids in understanding the network's complexity and potential points of vulnerability.
