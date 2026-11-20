# TLS 1.3 Traffic Analysis Using Wireshark

## Objective
Analyze a TLS 1.3 connection using Wireshark to understand the TLS handshake, negotiated cryptographic parameters, and encrypted traffic.

## Tools
- Wireshark
- Windows 11
- Network packet capture (PCAPNG)

## Investigation

### 1. TCP Connection Establishment
The TCP three-way handshake was observed in packets 417, 418, and 419.

- Packet 417: SYN
- Packet 418: SYN, ACK
- Packet 419: ACK

The connection used TCP port 443 for HTTPS communication.

### 2. TLS Client Hello
Packet 420 contained the TLS Client Hello message.

Observations:
- SNI hostname: safebrowsing.google.com
- Supported versions: TLS 1.3 and TLS 1.2
- Offered cipher suites: 16

The client advertised supported TLS parameters to the server.

### 3. TLS Server Hello
Packet 422 contained the TLS Server Hello message.

Observations:
- Negotiated TLS version: TLS 1.3
- Selected cipher suite: TLS_AES_128_GCM_SHA256
- Key share group: X25519MLKEM768

The Server Hello confirmed the negotiated TLS parameters.

### 4. Encrypted TLS Traffic
Packet 426 contained a TLS Application Data record.

Observations:
- TLS record type: Application Data (23)
- Source TCP port: 443
- Destination TCP port: 53989
- Encrypted application data was present.
- Wireshark reassembled four TCP segments.

The application content was not readable without the required decryption keys.

## Conclusion
This investigation demonstrated how Wireshark can be used to identify a TCP handshake, inspect TLS 1.3 negotiation, and observe encrypted TLS records.

## Skills Practiced
- Network packet analysis
- TCP handshake analysis
- TLS 1.3 protocol analysis
- Cipher suite identification
- Encrypted traffic investigation
- Wireshark filtering
