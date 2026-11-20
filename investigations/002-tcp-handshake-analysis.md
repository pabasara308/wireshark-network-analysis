# TCP Three-Way Handshake Analysis

## Objective
Analyze and verify the TCP three-way handshake using Wireshark.

## Lab Environment
- Operating system: Windows 11
- Tool: Wireshark
- Protocols: TCP, IPv6, TLS 1.3

## Wireshark Filter
`tcp.stream eq 17`

## Packet Analysis
| Packet | Source Port | Destination Port | TCP Flags | Observation |
|---|---|---|---|---|
| 417 | 53989 | 443 | SYN | Client initiates a TCP connection |
| 418 | 443 | 53989 | SYN, ACK | Server acknowledges the connection request |
| 419 | 53989 | 443 | ACK | Client completes the TCP handshake |

## Findings
1. Identified all three TCP handshake packets.
2. Verified SYN, SYN-ACK, and ACK flags in Wireshark.
3. Observed a TLS 1.3 Client Hello after the TCP handshake.
4. Confirmed that the analyzed connection used IPv6.

## Conclusion
The capture demonstrates a successful TCP three-way handshake followed by the beginning of TLS communication. No malicious activity was established from these packets alone.

## Evidence
See the screenshots folder for packet-analysis evidence.
