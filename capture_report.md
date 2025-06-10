# Network Traffic Analysis Report

**Capture File:** `network_capture.pcap`  
**Date of Analysis:** Monday, June 2  
**Analyst Name:** Mahenaz  
**Purpose:** Protocol breakdown, communication pattern identification, and network behavior summary

---

## 1. Executive Summary

This report presents the findings from the analysis of a packet capture (`network_capture.pcap`). The traffic is characterized by a heavy reliance on IPv6 addressing, widespread use of modern encrypted protocols (TLSv1.3, QUIC), and minimal legacy protocol activity. The observed behavior aligns with typical end-user activities such as secure web browsing, video streaming, and background network operations.

---

## 2. Methodology

- **Tool Used:** TShark (Wireshark CLI)
- **Analysis Focus:**
  - Protocol distribution
  - Communication patterns
  - Service identification
  - Security and protocol trends

---

## 3. Protocol Breakdown

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

---

## 4. Key Observations

### IPv6 Dominance

- IPv6 frames total: **11,874**
- Significantly more IPv6 traffic compared to IPv4, indicating a mature IPv6-enabled environment.

### Encrypted Communications

- **TLSv1.3** is widely used, reflecting strong adoption of secure HTTPS and encrypted service traffic.
- High volume of **QUIC packets** suggests usage of next-generation transport protocols, commonly seen in services like YouTube, Google Search, and other web-based applications using HTTP/3.

### Limited Legacy Protocols

- Only **4 HTTP packets** were identified, showing minimal use of unencrypted communication.
- Minimal **DNS traffic** (186 queries), primarily resolving domains such as `google.com`.

### Local Network Discovery

- Presence of **ARP** and **ICMPv6 Neighbor Discovery** frames indicates normal local network operation and device discovery.

---

## 5. Identified Services

| Service                  | Protocol(s) Used             | Description                                               |
|--------------------------|------------------------------|-----------------------------------------------------------|
| Encrypted Web Browsing   | HTTPS, TLSv1.3               | Secure access to websites and online services             |
| Video Streaming          | QUIC                         | Likely associated with platforms like YouTube              |
| Domain Resolution        | DNS over UDP                 | Standard DNS queries for domain name resolution            |
| Certificate Validation   | OCSP                         | Online validation of SSL/TLS certificates                  |
| Local Network Discovery  | ARP, ICMPv6                  | Layer 2 and IPv6 neighbor discovery mechanisms             |

---

## 6. Notable Insights

- No signs of malicious or anomalous network activity detected.
- Traffic patterns reflect standard user behavior including:
  - Web browsing
  - Media streaming
  - Background certificate checks
  - Network maintenance tasks
- Strong presence of **QUIC** highlights the increasing adoption of high-performance, low-latency transport protocols for better user experience.

---

## 7. Conclusion

The captured traffic represents a typical modern network environment with a focus on:

- **Security** (via TLSv1.3 and QUIC encryption)
- **Performance optimization** (QUIC usage)
- **IPv6 adoption**

This dataset can serve as a valuable reference for:

- Educational purposes
- Protocol study
- Baseline profiling for future anomaly detection initiatives

---

**End of Report**
