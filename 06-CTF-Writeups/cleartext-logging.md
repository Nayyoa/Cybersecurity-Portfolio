
# Cleartext Logging Windows Event Log Forensics

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026
**Platform:** MetaCTF
**Category:** Forensics
**Points:** 275/275
**Status:** Solved

## Scenario

An attacker was suspected of encrypting
files from the command line before
exfiltrating them.

Windows command-line logging had been
enabled, and an exported Windows Event
Log (.evtx) file was provided.

The objective was to recover information
that could help decrypt a RAR archive.

## Investigation

### 1. Windows Event Logs

The investigation focused on process
execution records within the provided
Windows Security event log.

Windows Event ID 4688 is associated
with process creation.

When command-line auditing is enabled,
these events can include arguments
passed to executed programs.

### 2. Command-Line Evidence

The relevant investigation involved
examining command-line activity for
evidence of archive creation or encryption.

Such records may expose information
about how an archive was generated.

### 3. Challenge Resolution

The challenge was successfully solved,
earning 275 points.

The exact recovered command line and
archive password are omitted because
they have not been independently
reconstructed for this writeup.

## Security Lessons

- Process creation logs can provide
  valuable forensic evidence.
- Command-line arguments may reveal
  sensitive information.
- Windows event logs can help
  reconstruct attacker activity.
- Logging configuration affects
  investigation visibility.

## Skills Demonstrated

- Windows event log analysis
- Process execution investigation
- Digital forensics
- Incident investigation
