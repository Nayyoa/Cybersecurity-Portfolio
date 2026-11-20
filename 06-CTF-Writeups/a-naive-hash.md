
# A Naive Hash MD5 Hash Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026
**Platform:** MetaCTF
**Category:** Cryptography
**Points:** 100/100
**Status:** Solved

## Scenario

The challenge provided the following
MD5 hash:

`5c2981b42e5bc96ad70cf064290b70b4`

The objective was to determine the
original plaintext corresponding
to the hash.

## Investigation Methodology

### 1. Identify the Hash Format

The supplied value contains 32
hexadecimal characters.

This is consistent with the format
of an MD5 hash, which produces a
128-bit digest.

### 2. Understand Hash Verification

MD5 is a one-way hash function.

Unlike encryption, hashing does
not provide a decryption operation.

Recovering the original plaintext
generally involves testing candidate
values and comparing their hashes.

### 3. Recover the Plaintext

The challenge was solved by identifying
a plaintext candidate whose MD5
digest matched the supplied hash.

The recovered plaintext was:

`wildc@ts`

### 4. Verify the Result

The candidate can be verified locally
using Python:

```python
import hashlib

candidate = "wildc@ts"

digest = hashlib.md5(
    candidate.encode()
).hexdigest()

print(digest)
```

The computed digest can then be
compared with the challenge hash.

## Security Lessons

- Hashing is not encryption.
- MD5 is unsuitable for secure
  password storage.
- Predictable passwords are
  vulnerable to guessing attacks.
- Password storage should use
  modern password-hashing algorithms
  such as Argon2id.

## Skills Demonstrated

- Cryptographic hash identification
- MD5 analysis
- Hash verification
- Python scripting
- Password security fundamentals
