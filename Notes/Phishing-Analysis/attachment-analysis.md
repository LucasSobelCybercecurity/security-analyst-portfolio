# Attachment Analysis

## Overview

Email attachments are one of the most common methods attackers use to deliver malicious content.

Attackers use attachments to:

- Deliver malware
- Steal credentials
- Execute malicious code
- Redirect users to phishing websites

SOC analysts must analyze attachments safely before opening them.

---

# Common Malicious Attachment Types

## PDF Files

Attackers use PDFs because they look trustworthy.

Possible threats:

- Hidden links
- Fake login pages
- Embedded content

Example: invoice.pdf

A PDF file is not automatically safe.

---

## Microsoft Office Files

Common examples:
.docm
.xlsm
.doc
.xlsx

Risks:

- Macros
- Embedded links
- Malicious scripts

Attackers often use documents pretending to be:

- Invoices
- Reports
- Shipping documents

---

## Archive Files

Examples:
.zip
.rar
.7z

Used to:

- Hide malware
- Bypass email filters
- Compress malicious files

Example:
invoice.zip
└── invoice.exe

---

## Executable Files

Examples:
.exe
.bat
.scr

These files can directly execute code.

High risk indicators:

- Unexpected executable files
- Unknown sources
- Fake file extensions

Example: document.pdf.exe

---

# Attachment Analysis Process

## Step 1 - Do Not Open the File

Never open suspicious attachments on a normal machine.

Use:

- Virtual machine
- Sandbox
- Malware analysis environment

Purpose:

- Prevent infection
- Protect analyst systems

---

# Step 2 - Check File Information

Analyze:

- File name
- File extension
- File size
- File type

Questions:

- Does the file match the email purpose?
- Is the extension suspicious?
- Was the attachment expected?

Example:

Email: Netflix billing problem

Attachment: invoice.exe

Possible phishing indicator.

---

# Step 3 - Generate File Hash

A hash creates a unique identifier for a file.

Common algorithms:

- MD5
- SHA-1
- SHA-256

Example: sha256sum suspicious_file.pdf

Hash example: 025ba9ce4a2118a9ca7b115c8869ff73bc16bad3732ba359cef1e60ad8f961f9

Hashes are used for:

- Malware identification
- Threat intelligence searches
- Comparing files

---

# Step 4 - Analyze Embedded Content

Files can contain hidden content.

Look for:

- Embedded links
- Macros
- Scripts
- External resources

Examples:

Office documents:

- VBA macros
- External URLs

PDF files:

- Embedded links
- JavaScript

---

# Step 5 - Check Reputation

Upload hashes or files to security platforms.

Useful tools:

## VirusTotal

Used for:

- File reputation
- Hash searches
- Antivirus detections

---

## Cisco Talos

Provides:

- Threat intelligence
- Malware reputation
- File analysis

---

# Malware Sandbox Analysis

A sandbox is a controlled environment used to safely execute suspicious files.

It allows analysts to observe:

- Processes
- Network connections
- File changes
- System modifications
- Malware behavior

---

# Sandbox Tools

## ANY.RUN

Features:

- Interactive malware analysis
- Process monitoring
- Network analysis
- IOC collection

---

## Hybrid Analysis

Provides:

- Malware behavior reports
- Network activity
- System changes
- Threat indicators

---

## Joe Sandbox

Supports:

- Static analysis
- Dynamic analysis

Static analysis:

- Examines files without execution

Dynamic analysis:

- Observes behavior during execution

---

# Common Attachment Red Flags

## Unexpected Files

Example:
You did not request an invoice
but received one

---

## Suspicious Extensions

Examples:
.pdf.exe
.docm
.xlsm
.scr

---

## Fake Documents

Attackers create:

- Fake invoices
- Fake shipping documents
- Fake payment requests

---

## Password Protected Archives

Attackers may use passwords to:

- Avoid email scanning
- Hide malware

---

# SOC Analyst Workflow

When analyzing an attachment:

1. Collect the file
2. Do not open it directly
3. Identify file type
4. Generate hash
5. Search reputation databases
6. Analyze safely in sandbox
7. Collect IOCs
8. Document findings

---

# Key Takeaways

- Attachments are common phishing attack vectors
- Never open suspicious files directly
- File hashes help identify known threats
- Sandboxes allow safe malware analysis
- Always collect and document attachment indicators
