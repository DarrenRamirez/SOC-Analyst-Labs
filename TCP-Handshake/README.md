# TCP 3-Way Handshake Lab

## Objective
Capture and analyze a TCP 3-way handshake using Wireshark to demonstrate how reliable connections are established at OSI Layer 4 (Transport).

---

##  Tools Used
- **Wireshark** – packet capture and analysis
- **Windows/Linux Terminal** – generated traffic (ping, curl, nslookup)

---

## Process
1. Started Wireshark capture on active network interface (Wi-Fi).
2. Generated new TCP traffic using:
   - `ping google.com`
   - `curl http://example.com`
   - Opened websites in browser (new tab/private mode).
3. Applied Wireshark display filter:
   ```wireshark
   tcp.flags.syn == 1 || tcp.flags.ack == 1
