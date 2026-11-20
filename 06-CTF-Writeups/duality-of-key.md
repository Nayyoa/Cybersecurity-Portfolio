
# Duality of Key Cryptographic Investigation

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Cryptography  
**Points:** 300/300  
**Status:** Solved

## Challenge Description

The challenge provided the clue:

"If one key is good, two must be great!"

A downloadable challenge artifact
was also provided.

The objective was to investigate
the cryptographic mechanism and
recover the hidden flag.

## Solution Approach

### Step 1: Identify the Artifact

The first step is to
determine the file format.

On Linux:

```bash
file challenge_file
```

The file contents could then
be examined using:

```bash
xxd challenge_file | head
```

For a text-based artifact:

```bash
cat challenge_file
```

These checks help determine
whether the file contains
source code, encoded data,
ciphertext, or cryptographic
parameters.

### Step 2: Identify the Key Structure

The challenge title suggests
that two keys play a role
in the cryptographic process.

The investigation focuses on:

- The encryption algorithm
- The purpose of each key
- Whether the keys are independent
- The relationship between the keys
- The order of cryptographic operations


### Step 3: Analyze the Cryptographic Operations

The next step is to
identify the operations
performed on the plaintext.

```python
def xor_encrypt(data, key1, key2):
    result = bytearray()

    for i, value in enumerate(data):
        result.append(
            value
            ^ key1[i % len(key1)]
            ^ key2[i % len(key2)]
        )

    return bytes(result)
```

In such a construction,
XOR is reversible.

### Step 4: Reconstruct the Decryption

Once the algorithm
and key relationships are
identified, the inverse
operations can be implemented.

The recovered plaintext
is then checked
against the expected
MetaCTF flag format.

## Result

**Challenge successfully solved.**

The original artifact is required
to reproduce the exact key analysis
and decryption sequence.

## Skills Demonstrated

- Cryptographic analysis
- Binary and file inspection
- Python scripting
- Key management concepts
- Algorithm analysis

## Key Takeaways

Cryptographic security depends
on how algorithms and keys
are combined.

Multiple keys do not
automatically guarantee
stronger encryption.
