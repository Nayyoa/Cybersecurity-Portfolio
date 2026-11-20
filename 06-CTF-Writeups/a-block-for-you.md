
# A Block for You, A Block For ??? Custom Cryptography

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Cryptography  
**Points:** 400/400  
**Status:** Solved

## Challenge Description

The challenge introduced a fictional
attacker who developed a custom
encryption system.

A hexadecimal ciphertext was provided.

The objective was to investigate
the cryptographic construction
and recover the original message.

## Solution Approach

### Step 1: Decode the Hexadecimal Data

The ciphertext was provided as
a hexadecimal string.

Python can convert it into
raw bytes:

```python
ciphertext_hex = (
    "3d025bb30453680a77bba03d061017c0"
    "752cec10bdfc02346956e13d56814956"
    "bc4eb1c269896c8748d9e0e6631a1a"
    "180476e2b4c2ae514a212ced02de0ba3d5"
)

ciphertext = bytes.fromhex(ciphertext_hex)

print("Length:", len(ciphertext))
print("Hex:", ciphertext.hex())
```

### Step 2: Examine the Ciphertext Structure

The next step was to
investigate whether the data
follows a block-oriented structure.

Useful observations include:

- Total ciphertext length
- Repeated byte sequences
- Potential block boundaries
- Padding patterns
- Available encryption parameters

The challenge title suggests
a connection with block-based
cryptography.


### Step 3: Investigate the Encryption Algorithm

The challenge description
indicates that the attacker
implemented a custom
cryptographic construction.

I examined the source code
to determine:

1. How plaintext is divided
   into blocks
2. How each block is transformed
3. Whether blocks depend on
   previous blocks
4. How encryption keys are used
5. Whether the transformations
   can be reversed

### Step 4: Develop a Decryption Strategy

After identifying the encryption
mechanism, the next step was
to implement its inverse.

The decryption algorithm must
match the actual cryptographic
construction.


### Step 5: Validate the Plaintext


## Result

**Challenge successfully solved.**

**Points earned:** 400/400

## Skills Demonstrated

- Cryptanalysis
- Hexadecimal data processing
- Python scripting
- Block cipher concepts
- Algorithm investigation

## Key Takeaways

Custom encryption algorithms
may contain weaknesses that
are difficult to identify
without understanding their
internal operations.

Secure cryptographic design
requires more than simply
making an algorithm complicated.
