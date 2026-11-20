
# 64 Types of Candy Base64 Decoding

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Cryptography  
**Points:** 100/100  
**Status:** Solved

## Scenario

A friend refused to reveal their
favorite Halloween candy without
encoding the answer.

The challenge provided the following
encoded string:

```
TWV0YUNURntsMzdzX2cwX3cxdGhfZDRya19jaDBjMGw0dDN9
```

The objective was to decode the
message and recover the flag.

## Investigation

### 1. Identify the Encoding

The challenge title referenced
the number 64.

The supplied string contained
characters consistent with Base64
encoding.

Base64 represents binary data
using a set of 64 characters.

### 2. Decode the Message

Python can be used to decode
the supplied string:

```python
import base64

encoded = (
    "TWV0YUNURntsMzdzX2cwX3cxdGhf"
    "ZDRya19jaDBjMGw0dDN9"
)

decoded = base64.b64decode(encoded)

print(decoded.decode("utf-8"))
```

### 3. Result

The decoded message revealed
the challenge flag.

The challenge was successfully
completed, earning 100 points.

## Security Lessons

Base64 is an encoding scheme,
not an encryption algorithm.

Encoded data can be decoded
without a secret key.

## Skills Demonstrated

- Encoding identification
- Base64 decoding
- Python scripting
- Data interpretation
