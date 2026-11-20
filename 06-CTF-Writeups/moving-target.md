
# Moving Target — DNS Fast Flux Investigation

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Network Forensics  
**Difficulty:** Pro  
**Points:** 100/100  
**Status:** Solved

## Scenario

A network capture contained DNS traffic
from several office workstations.

One domain exhibited suspicious behavior:
its DNS responses repeatedly returned
different IP addresses with unusually
short Time-to-Live (TTL) values.

The objective was to identify the domain
using this behavior.

**Provided artifact:** `suspicious-dns.pcap`

---

## Investigation Methodology

### 1. Examine DNS Traffic

The investigation focused on DNS
communications in the provided PCAP.

Wireshark display filter:

`dns`

This allows DNS queries and responses
to be examined separately from other
network traffic.

### 2. Analyze DNS Responses

The key indicators to investigate were:

- Repeated queries for the same domain
- Frequently changing resolved IP addresses
- Unusually short DNS TTL values
- Differences from normal DNS activity

### 3. Identify Fast Flux Behavior

Fast flux is a technique in which a
domain name rapidly resolves to different
IP addresses.

This can make malicious infrastructure
more difficult to identify and block
using individual IP addresses.

By comparing DNS responses for the same
domain, the suspicious resolution pattern
can be distinguished from ordinary
browsing activity.

### 4. Determine the Suspicious Domain

The challenge required identifying the
single domain exhibiting fast flux behavior.

The correct domain was identified and
submitted successfully.

The exact domain is not reproduced here.

---

## Findings

The challenge demonstrated how DNS
resolution patterns can reveal suspicious
network infrastructure.

Important indicators included:

- Rapid IP address changes
- Very short TTL values
- Repeated DNS resolution activity

These indicators can support threat
detection when evaluated alongside
other network and security telemetry.

---

## Security Implications

Fast flux techniques may be associated
with malicious infrastructure designed
to remain available despite IP-based
blocking.

Security analysts can investigate
such activity through:

- DNS log monitoring
- Historical DNS analysis
- Network traffic inspection
- Correlation with threat intelligence

---

## Skills Demonstrated

- DNS protocol analysis
- Network traffic investigation
- Suspicious infrastructure detection
- Fast flux identification
- Digital forensics
- Threat analysis

---

## Key Takeaways

This challenge highlighted the value
of DNS traffic analysis in identifying
potentially malicious infrastructure.

It demonstrated how changes in DNS
responses and TTL values can provide
useful indicators during security
investigations.
