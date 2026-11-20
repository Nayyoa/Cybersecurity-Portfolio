
# Baby Something HTTP Traffic Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Forensics  
**Points:** 50/50  
**Status:** Solved

## Challenge Description

The challenge provided the clue:

"How does the song go again?
Baby something do do do do do do..."

A packet capture was supplied
for analysis.

**Artifact:** `babysomething.pcap`

The objective was to inspect
the network traffic and
recover the hidden flag.

## Investigation Methodology

### Step 1: Open the PCAP

The investigation began by
examining the packet capture
in Wireshark.

The goal was to identify
relevant protocols and
application-layer communications.

### Step 2: Filter HTTP Traffic

The following Wireshark
display filter isolates
HTTP traffic:

```text
http
```

This makes it easier to
identify web requests
and server responses.

### Step 3: Identify the HTTP Exchange

The investigation identified
the following packets:

**Packet 4:**

```http
GET / HTTP/1.1
```

**Packet 6:**

```http
HTTP/1.1 200 OK
```

The HTTP communication
involved the host:

```text
babyshark.local
```

The successful response
indicated that the server
returned the requested
web resource.

### Step 4: Follow the TCP Stream

To inspect the complete
HTTP communication:

1. Select the relevant
   HTTP packet.
2. Right-click the packet.
3. Select Follow.
4. Choose TCP Stream.

Wireshark reconstructs
the communication between
the client and server.

### Step 5: Examine the Response

The HTTP response contained
HTML content.

Inspecting the reconstructed
TCP stream revealed the
information needed to
identify the flag.

### Step 6: Submit the Flag

The recovered flag was
submitted successfully.

**Points earned:** 50/50

## Security Implications

Unencrypted HTTP traffic
can expose application data
to network observers.

Network forensic tools
can reconstruct HTTP
communications and reveal
transmitted content.

HTTPS protects this content
through transport encryption.

## Skills Demonstrated

- Wireshark
- Network packet analysis
- HTTP protocol investigation
- TCP stream reconstruction
- Digital forensics

## Key Takeaways

Following TCP streams is
an effective technique for
investigating application-layer
traffic.

Even simple HTTP exchanges
can contain valuable
forensic evidence.
