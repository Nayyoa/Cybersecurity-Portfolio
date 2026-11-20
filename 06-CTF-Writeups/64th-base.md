
# 64th Base Base64 Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Cryptography  
**Points:** 100/100  
**Status:** Solved

## Scenario

The challenge described a fictional
baseball game involving 64 bases.

Players were exchanging encoded
messages instead of communicating
normally.

The following string was provided:

```
TWV0YUNURntoMHAzX3kwdV9nM3RfNF9oMG0zX3J1bn0=
```

The objective was to recover
the hidden message.

## Investigation

### 1. Recognize Base64

The challenge title suggested
a connection with Base64.

The supplied string also
contained a trailing equals
sign, commonly used as padding
in Base64 encoding.

### 2. Decode the String

Python provides a built-in
Base64 decoding module:

```python
import base64

encoded = (
    "TWV0YUNURntoMHAzX3kwdV9nM3Rf"
    "NF9oMG0zX3J1bn0="
)

decoded = base64.b64decode(encoded)

print(decoded.decode("utf-8"))
```

### 3. Result

Decoding the string revealed
the expected flag.

The challenge was successfully
completed, earning 100 points.

## Security Lessons

Encoding and encryption serve
different purposes.

Base64 does not provide
confidentiality because anyone
can reverse the encoding.

## Skills Demonstrated

- Base64 recognition
- Encoded data analysis
- Python scripting
- Cryptography fundamentals
