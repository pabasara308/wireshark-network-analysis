# Investigation 001 – DNS Traffic Analysis

## Objective
Capture and analyze DNS traffic using Wireshark to understand how domain names are resolved into IP addresses.

## Lab Environment
- Operating System: Windows 11
- Tool: Wireshark 4.6.10
- Network Interface: Wi-Fi
- Test Domain: example.com
- Display Filter: `dns.qry.name == "example.com"`

## Investigation Steps
1. Started packet capture on the Wi-Fi interface.
2. Opened `https://example.com` in a web browser.
3. Stopped packet capture and applied a DNS display filter.
4. Identified DNS queries for A, AAAA, and HTTPS records.
5. Matched DNS request packet 580 with response packet 590.
6. Expanded the DNS response details and inspected the returned IPv4 addresses.

## Findings
- DNS Client: 192.168.8.82
- DNS Server: 192.168.8.1
- Domain: example.com
- Query Type: A (IPv4)
- Request Packet: 580
- Response Packet: 590
- Transaction ID: 0x141d
- Response Code: No error
- Answer Records: 2
- Resolved IPv4 Addresses:
  - 104.20.23.154
  - 172.66.147.243
- DNS Response Time: 31.7206 ms

## Conclusion
The DNS query for example.com completed successfully and returned two IPv4 addresses. This exercise demonstrated packet capture, DNS filtering, request-response correlation, and basic DNS response analysis.

No malicious activity was identified from this DNS exchange alone.

## Skills Practiced
- Wireshark packet capture
- DNS protocol analysis
- Network traffic filtering
- DNS transaction identification
- Security investigation documentation
