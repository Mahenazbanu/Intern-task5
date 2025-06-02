# Intern-task5
Capture and Analyze Network Traffic Using Wireshark.



# Network Traffic Capture & Analysis with Wireshark

This project demonstrates how to capture and analyze live network traffic using **Wireshark**, focusing on identifying common protocols and understanding communication patterns in a modern network environment.

## 🎯 Objective
The goal of this task is to:
- Gain hands-on experience capturing live network traffic.
- Identify and understand different network protocols in use.
- Analyze packet data to recognize typical communication behaviors.

## 🛠️ Tools Used
- **Wireshark** (Free and open-source network protocol analyzer)

## 📁 Deliverables
1. A packet capture file: `network_capture.pcap`
2. A summary report detailing observed protocols and network behavior

---

## 🧪 Task Steps Performed

1. Installed **Wireshark** on the analysis machine.
2. Started packet capture on the active network interface.
3. Generated traffic by browsing websites and streaming media.
4. Stopped capture after approximately one minute.
5. Applied display filters to isolate specific protocols (e.g., TCP, DNS, QUIC).
6. Identified at least 3 distinct protocols in the captured data.
7. Exported the full capture as `network_capture.pcap`.
8. Summarized findings based on the observed packet details.

---

## 📊 Summary of Findings

> **Analysis Date:** Monday, June 2  
> **Analyst Name:** Mahenaz  
> **Capture File:** `network_capture.pcap`

### 🔍 Protocol Breakdown

| Protocol   | Packet Count |
|------------|--------------|
| TCP        | 4,982        |
| QUIC       | 3,796        |
| TLSv1.3    | 2,715        |
| ICMPv6     | 224          |
| DNS        | 186          |
| OCSP       | 98           |
| ARP        | 14           |
| HTTP       | 4            |

### 🌐 Key Observations

- **IPv6 Dominance:** Over 11,000 IPv6 frames were observed, indicating a mature IPv6-enabled network environment.
- **Encrypted Communication:** Widespread use of **TLSv1.3** and **QUIC**, showing strong preference for secure and efficient transport protocols.
- **Minimal Legacy Protocols:** Only 4 unencrypted HTTP packets detected, reflecting modern security practices.
- **Local Discovery:** Normal local network operations were seen via **ARP** and **ICMPv6 Neighbor Discovery**.

### 🚦 Identified Services

| Service                  | Protocol(s) Used             | Description                                               |
|--------------------------|------------------------------|-----------------------------------------------------------|
| Encrypted Web Browsing   | HTTPS, TLSv1.3               | Secure access to websites                                 |
| Video Streaming          | QUIC                         | Likely YouTube or Google services over HTTP/3              |
| Domain Resolution        | DNS over UDP                 | Standard domain name lookups                              |
| Certificate Validation   | OCSP                         | SSL/TLS certificate status checks                         |
| Local Network Discovery  | ARP, ICMPv6                  | Layer 2 and IPv6 neighbor discovery                       |

---

## 🧠 Notable Insights

- No malicious or suspicious activity was identified.
- Traffic reflects standard end-user behavior such as web browsing, video streaming, and background system tasks.
- Strong presence of **QUIC** highlights growing adoption of next-generation transport protocols for performance optimization.

---

## 📝 Conclusion

This packet capture serves as an excellent example of modern network behavior — secure, encrypted, and optimized for performance. It can be used for:
- Educational purposes
- Protocol study
- Baseline profiling for future anomaly detection

---

## 📂 Files Included in Repository

- `network_capture.pcap` – The raw packet capture file
- `README.md` – This document explaining the task, methodology, and findings

---

## 📚 How to Use This Repository

To explore the packet capture:
1. Download and install [Wireshark](https://www.wireshark.org/) 
2. Open `network_capture.pcap` in Wireshark
3. Apply filters like `tcp`, `quic`, `tls`, or `dns` to examine specific protocols

---

## 🙌 Outcome

By completing this task, you gain:
- Practical experience in packet capture and analysis
- Awareness of common network protocols and their usage
- Insight into secure and modern communication trends
