
# Cryptic COBOL — Source Code Analysis

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Reverse Engineering  
**Points:** 300/300  
**Status:** Solved

## Scenario

The challenge provided a COBOL program
containing intentional syntax errors.

The objective was to determine what
the program would print if its syntax
errors were corrected.

Executing the original program was
not a viable solution.

## Reconstructed Solution Approach

### Step 1: Inspect the Source Code

I would begin by identifying the
main sections of the COBOL program.

A typical COBOL program includes:

- IDENTIFICATION DIVISION
- DATA DIVISION
- PROCEDURE DIVISION

The PROCEDURE DIVISION contains the
executable logic.

### Step 2: Identify Output Statements

I would search for DISPLAY statements,
which are commonly used to print output.

For example:

```cobol
DISPLAY "HELLO WORLD".
```

This statement prints the specified text.

### Step 3: Trace Variables and Operations

Next, I would examine:

- Variable declarations
- Initial values
- MOVE statements
- STRING operations
- Conditional branches
- Arithmetic operations

The goal would be to determine the
final values displayed by the program.

### Step 4: Simulate Execution

Since the source contains intentional
syntax errors, I would trace the
intended execution manually.

For each statement, I would record
how the program state changes.

### Step 5: Recover the Output

Finally, I would reconstruct the
exact output that a corrected
version of the program would print.

The challenge was successfully
completed, earning 300 points.

The original source code is needed
to reproduce the exact output.

## Skills Demonstrated

- Source code analysis
- Reverse engineering
- Control flow tracing
- Program logic interpretation
- Debugging fundamentals

## Key Takeaways

Reverse engineering does not always
require executing a program.

Static source analysis can reveal
the intended behavior of software,
even when the code cannot compile.
