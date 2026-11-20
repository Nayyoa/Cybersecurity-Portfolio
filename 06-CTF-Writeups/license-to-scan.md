
# 007: License to Scan — Custom Protocol Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026
**Platform:** MetaCTF
**Category:** Forensics
**Points:** 250/250
**Status:** Solved

## Scenario

A transport department acquired used
license plate cameras.

The camera console was not functioning,
so the challenge provided a network
packet capture and documentation
describing the camera protocol.

The objective was to analyze the
captured communications and recover
the required information.

## Investigation

### 1. Packet Capture Analysis

The investigation involved a PCAPNG
file containing communications from
the camera system.

The provided protocol documentation
was essential for interpreting the
captured traffic.

### 2. Custom Protocol Interpretation

Unlike standard HTTP or DNS traffic,
custom protocols may require manual
interpretation of packet fields.

The investigation involved examining
the protocol structure and determining
how its data was represented.

### 3. Encoded Data

Our earlier investigation included
analysis of a custom protocol referred
to as MALD and XOR-based decoding.

The original packet offsets and
complete decoding sequence are not
included here because they have not
been verified against the capture.

### 4. Result

The challenge was successfully solved,
earning 250 points.

## Security Lessons

- Proprietary protocols may require
  manual packet interpretation.
- Protocol documentation can be
  critical to forensic analysis.
- Encoded traffic is not necessarily
  encrypted securely.
- Packet captures can reveal
  application-specific information.

## Skills Demonstrated

- Network forensics
- Custom protocol analysis
- Packet structure interpretation
- Data encoding analysis
- Technical documentation analysis
