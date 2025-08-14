# Networking Reference

## OSI Model

| Layer Number | Layer Name         | Main Function                                 | Example Protocols and Standards           |
|--------------|------------------|-----------------------------------------------|------------------------------------------|
| Layer 7      | Application       | Provides services and interfaces to apps    | HTTP, FTP, DNS, POP3, SMTP, IMAP        |
| Layer 6      | Presentation      | Data encoding, encryption, compression       | Unicode, MIME, JPEG, PNG, MPEG           |
| Layer 5      | Session           | Manage and synchronize sessions              | NFS, RPC                                 |
| Layer 4      | Transport         | End-to-end communication, segmentation      | UDP, TCP                                 |
| Layer 3      | Network           | Logical addressing, routing between networks| IP, ICMP, IPSec                          |
| Layer 2      | Data Link         | Reliable data transfer between adjacent nodes| Ethernet (802.3), WiFi (802.11)         |
| Layer 1      | Physical          | Physical transmission of data                | Electrical, optical, wireless signals   |

---

## IP Addressing
- Each octet must be `0 ≤ octet ≤ 255`.  
- Private IP ranges (RFC 1918):
  - `10.0.0.0 - 10.255.255.255` (10/8)  
  - `172.16.0.0 - 172.31.255.255` (172.16/12)  
  - `192.168.0.0 - 192.168.255.255` (192.168/16)  
- Port numbers: `1–65535`

| Protocol | Transport | Default Port |
|----------|-----------|--------------|
| TELNET   | TCP       | 23           |
| DNS      | UDP/TCP   | 53           |
| HTTP     | TCP       | 80           |
| HTTPS    | TCP       | 443          |
| FTP      | TCP       | 21           |
| SMTP     | TCP       | 25           |
| POP3     | TCP       | 110          |
| IMAP     | TCP       | 143          |

---

## TCPDump

### Basic Commands
| Command                     | Explanation                                        |
|------------------------------|---------------------------------------------------|
| `tcpdump -i INTERFACE`       | Capture packets on a network interface           |
| `tcpdump -w FILE`            | Write captured packets to a file                 |
| `tcpdump -r FILE`            | Read packets from a file                          |
| `tcpdump -c COUNT`           | Capture a set number of packets                  |
| `tcpdump -n`                 | Do not resolve IP addresses                       |
| `tcpdump -nn`                | Do not resolve IP addresses or protocols         |
| `tcpdump -v`                 | Verbose output (`-vv`, `-vvv` for more detail)  |

**Examples**
```bash
tcpdump -i eth0 -c 50 -v          # Capture 50 packets on eth0 verbosely
tcpdump -i wlo1 -w data.pcap      # Capture WiFi packets to a file
tcpdump -i any -nn                # Capture packets on all interfaces without resolving names


Filtering
Command	Explanation
tcpdump host IP	Filter by IP or hostname
tcpdump src host IP	Filter by source IP
tcpdump dst host IP	Filter by destination IP
tcpdump port PORT_NUMBER	Filter by port
tcpdump src port PORT_NUMBER	Filter by source port
tcpdump dst port PORT_NUMBER	Filter by destination port
tcpdump PROTOCOL	Filter by protocol (e.g., ip, ip6, icmp)

Examples

tcpdump -i any tcp port 22                         # Capture SSH traffic
tcpdump -i wlo1 udp port 123                       # Capture NTP traffic
tcpdump -i eth0 host example.com and tcp port 443  # Capture HTTPS traffic for example.com

Display Options
Command	Explanation
tcpdump -q	Brief output
tcpdump -e	Include MAC addresses
tcpdump -A	Print packets as ASCII
tcpdump -xx	Display packets in hexadecimal
tcpdump -X	Show packets in both hexadecimal and ASCII
