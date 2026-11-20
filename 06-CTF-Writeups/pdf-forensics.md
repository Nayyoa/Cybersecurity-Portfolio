
# PDF Forensics Document Redaction Investigation

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026  
**Platform:** MetaCTF  
**Category:** Forensics  
**Points:** 125/125  
**Status:** Solved

## Challenge Description

The challenge presented a
government document release
concerning an investigation
into VegetableCTF, Inc.

The document was described as
complying with applicable
transparency requirements.

**Provided artifact:**

`EDVA00004271.pdf`

The objective was to examine
the document and recover
the hidden information.

## Solution Approach

### Step 1: Inspect the PDF

The investigation begins with
a visual examination of the
document.

I looked for:

- Redacted passages
- Unusual formatting
- Hidden or overlapping content
- Suspicious document elements

### Step 2: Examine PDF Metadata

The following command can
display document metadata:

```bash
pdfinfo EDVA00004271.pdf
```

This reveals:

- PDF version
- Creation and modification dates
- Producing software
- Document properties

### Step 3: Extract Text

I attempted to extract
the document's text:

```bash
pdftotext -layout EDVA00004271.pdf extracted.txt
```

Then examined the output:

```bash
cat extracted.txt
```

This is useful because some
PDF documents contain text
that is not immediately
visible in the rendered page.

### Step 4: Investigate Redactions

The document contains
redacted information, I
checked whether the underlying
text was actually removed.

A common PDF security mistake
is placing an opaque shape
over sensitive text without
removing the original content.

Text extraction revealed information 
hidden beneath such overlays.


### Step 5: Recover the Flag

```text
MetaCTF{sh0uldnt_h4v3_c4nc3l13d_4cr0bat}
```

The flag references Acrobat,
which is consistent with the
challenge's PDF-related theme.



## Result

**Flag recovered successfully.**

**Points earned:** 125/125

## Skills Demonstrated

- PDF forensic investigation
- Document metadata analysis
- Text extraction
- Document security assessment
- Digital forensics

## Key Takeaways

PDF documents can contain
information beyond what is
visible on the page.

Proper redaction requires
removing sensitive information
from the underlying document,
not simply hiding it visually.
