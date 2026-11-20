
# Architecture Astronaut Binary Identification

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026
**Platform:** MetaCTF
**Category:** Reverse Engineering
**Points:** 100/100
**Status:** Solved

## Scenario

An executable was recovered from an
unknown device.

The program could not be executed on
the available system, suggesting that
it had been compiled for a different
CPU architecture.

The objective was to identify the
target architecture without running
or disassembling the executable.

## Investigation Methodology

### 1. Examine the Executable

The investigation focused on
identifying the binary's architecture
through its file format and metadata.

On Linux, the following command can
be used for this purpose:

```bash
file executable
```

This command can identify executable
formats and supported architectures.

### 2. Identify the Architecture

The executable was identified as
targeting the Xtensa architecture.

Xtensa is a configurable processor
architecture commonly associated
with embedded systems.

### 3. Result

**Recovered answer:** `xtensa`

The correct architecture was
submitted successfully.

## Security Lessons

- Executable files contain useful
  architectural metadata.
- Binary identification does not
  always require code execution.
- CPU architecture affects binary
  compatibility.
- File inspection is an important
  first step in malware analysis.

## Skills Demonstrated

- Binary file identification
- Executable format analysis
- CPU architecture recognition
- Reverse engineering fundamentals
