
# Cryptic COBOL Pascal's Triangle Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Reverse Engineering  
**Points:** 300/300  
**Status:** Solved

## Challenge Description

The challenge provided a COBOL program
containing intentional syntax errors.

The objective was to determine what
the program would print if it were
corrected and executed.

## Solution Approach

### Step 1: Analyze the Program Logic

The first step was to understand the
intended behavior of the COBOL program.

The program's logic was related to
Pascal's triangle, a mathematical
structure in which each interior
element is the sum of the two
elements directly above it.

The task was to determine the
numerical result produced by the
program.

### Step 2: Identify the Mathematical Pattern

Pascal's triangle begins as follows:

```text
         1
        1 1
       1 2 1
      1 3 3 1
     1 4 6 4 1
```

The sum of the elements in each
row follows a power-of-two pattern.

Using one-based row numbering:

- Row 1: 1
- Row 2: 2
- Row 3: 4
- Row 4: 8
- Row 5: 16

The sum of row n is:

```text
2^(n-1)
```

### Step 3: Calculate the Required Result

The program required the sum
of the 20th row.

Using the formula:

```text
2^(20-1) = 2^19 = 524288
```

### Step 4: Verify with Python

The calculation can be reproduced
using Python:

```python
row = 20

result = 2 ** (row - 1)

print(result)
```

Output:

```text
524288
```

### Step 5: Match the Program's Output

The expected output included
a leading zero.

The final answer was:

```text
0524288
```

This corresponds to the numerical
result formatted as a seven-digit
value.

## Result

**Recovered answer:** `0524288`

**Challenge successfully solved.**

## Skills Demonstrated

- Source code analysis
- Reverse engineering
- Mathematical pattern recognition
- Python scripting
- Program output reconstruction

## Key Takeaways

Understanding the mathematical
logic of a program can eliminate
the need to execute or compile it.

This challenge demonstrated how
static analysis and mathematical
reasoning can be combined to
recover a program's intended output.
