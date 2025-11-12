# Experiment 03 — Wireshark

**Aim:**  
To capture and analyze live network packets using Wireshark and identify communication protocols, IP addresses, and potential anomalies.

---

## Tools Used
- **Tool Name:** Wireshark  
- **Version:** 4.2.3  
- **Operating System:** Windows 10 (64-bit)  
- **File Type:** `.pcapng` (Packet Capture File)  
- **Protocols Observed:** TCP, UDP, HTTP, ICMP, DNS

---

## Procedure (Step-by-Step)
1. Launched **Wireshark** on the system.  
2. From the list of network interfaces, selected the **active adapter** 
3. Clicked the **Start Capturing Packets** button.  
4. Performed normal network activities — e.g., opened a website, searched Google, or pinged an IP.  
5. Stopped packet capture after 1–2 minutes using the **Red Stop** button.  
6. Saved the capture as:  
7. Applied filters to analyze specific traffic:
- `http` → view web traffic  
- `dns` → view domain name resolution  
- `icmp` → view ping requests/replies  
- `ip.src == 192.168.1.X` → filter packets from your system  
8. Selected individual packets to inspect **Frame details**, **Ethernet header**, **IP header**, and **TCP/UDP layers**.  
9. Expanded the packet details to view **source & destination IP addresses**, ports, and payload data.  
10. Used the **Statistics → Protocol Hierarchy** and **Conversations** windows to summarize captured traffic.  
11. Noted down suspicious packets or high-traffic connections for analysis.

---

## Result / Observation
Wireshark successfully captured and analyzed live network traffic from the system’s active network adapter.  
Packets were filtered and examined for protocol types, IP addresses, and packet-level details, providing insight into real-time communication between hosts.

---

## Conclusion
The experiment demonstrates how **Wireshark** can be used for network forensic analysis.  
It allows investigators to capture live packets, identify protocols, inspect headers, and detect suspicious or malicious activity.  
Wireshark is an essential tool for network monitoring, intrusion detection, and cybersecurity investigations.

---

## Viva / Important Questions

1. **What is Wireshark used for?**  
→ Wireshark is used to capture, analyze, and visualize network packets in real-time for troubleshooting and forensic analysis.

2. **What file format does Wireshark use to save captures?**  
→ `.pcap` or `.pcapng` (Packet Capture formats).

3. **What is a packet filter?**  
→ A filter helps isolate specific packets (e.g., only HTTP or DNS traffic) for focused analysis.

4. **Explain the difference between TCP and UDP.**  
→ TCP is connection-oriented and reliable; UDP is connectionless and faster, but less reliable.

5. **How can Wireshark help in digital forensics?**  
→ It helps trace communication between devices, identify data exfiltration, and verify timestamps of network events.
