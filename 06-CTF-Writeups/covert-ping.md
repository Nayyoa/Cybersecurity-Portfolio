
# Covert Ping — ICMP Exfiltration Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Forensics  
**Difficulty:** Pro  
**Points:** 100/100  
**Status:** Solved

## Scenario

A critical database server was observed
sending repeated ICMP Echo Requests to an
external host.

The traffic exhibited unusual characteristics:

- Repeated requests to the same destination
- Consistent packet sizes
- Regular communication patterns
- Activity unrelated to normal troubleshooting

The objective was to investigate the traffic
and identify information transmitted through
the suspected covert channel.

**Provided artifact:** `icmp-exfil.pcap`

---

## Investigation Methodology

### 1. Examine ICMP Traffic

The investigation focused on ICMP packets
contained in the supplied PCAP file.

Wireshark can isolate this traffic using
the following display filter:

`icmp`

The goal was to distinguish ordinary
diagnostic traffic from potentially
suspicious communications.

### 2. Identify Suspicious Communication

The investigation identified ICMP Echo
Requests between:

- Source: `10.10.10.50`
- Destination: `198.51.100.66`

The repeated requests contained identical
encoded application data.

This suggested that ICMP was being used
to carry information rather than solely
to test network connectivity.

### 3. Examine ICMP Payloads

Inspection of the ICMP payloads revealed
Base64-encoded content.

Six requests carried the same encoded data.

The repeated payloads were consistent with
the challenge's suspected covert channel.

### 4. Decode the Data

The encoded content was decoded using
Base64 decoding.

The decoded information followed the
credential format requested by the challenge:

`username:password`

The recovered credential was successfully
identified and submitted.

The credential itself is intentionally
omitted from this public writeup.

---

## Findings

The analysis confirmed that the ICMP
traffic contained encoded credential data.

Key observations:

- ICMP Echo Requests carried application data.
- The same encoded payload appeared repeatedly.
- Base64 decoding revealed credential information.
- The traffic demonstrated a potential
  data-exfiltration technique.

---

## Security Implications

ICMP is commonly used for network
diagnostics, but its payload fields can
also carry unauthorized information.

Security teams should consider:

- Monitoring unusual ICMP traffic patterns
- Inspecting unexpected payload content
- Detecting repeated external communications
- Investigating suspected covert channels

---

## Skills Demonstrated

- Network traffic investigation
- ICMP protocol analysis
- Payload inspection
- Base64 decoding
- Data exfiltration detection
- Digital forensics

---

## Key Takeaways

This challenge demonstrated how a common
network protocol can be misused to transfer
sensitive information.

It reinforced the importance of inspecting
packet contents and identifying abnormal
network behavior during security
investigations.
