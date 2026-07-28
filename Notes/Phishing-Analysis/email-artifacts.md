# Email Artifacts

## Overview

Email artifacts are pieces of information collected during an email investigation.

They help analysts:

- Identify phishing attempts
- Find Indicators of Compromise (IOCs)
- Investigate attacker infrastructure
- Perform threat intelligence checks
- Document security incidents

---

# Email Header Artifacts

Email headers contain technical information about the message.

They are one of the most important sources of information during phishing investigations.

---

## Sender Email Address

Shows who sent the email.

Analysts check:

- Username
- Domain
- Organization match

Red flags:

- Misspelled domains
- Free email providers pretending to be companies
- Suspicious domains

Example: support@micros0ft.com

The domain uses a zero instead of the letter "o".

---

## Sender IP Address

Shows the origin of the email.

Can be used for:

- IP reputation checks
- Geolocation
- Identifying mail servers
- Threat intelligence searches

Suspicious IP addresses may indicate:

- Spam infrastructure
- Compromised servers
- Malicious campaigns

---

## Subject

The subject line can reveal social engineering techniques.

Common phishing subjects:

- Account suspended
- Payment failed
- Security alert
- Action required
- Invoice attached

Attackers use subjects to create urgency.

---

## Recipient Information

Check:

- To
- CC
- BCC

Questions:

- Was the email sent directly?
- Was it sent to many users?
- Is the recipient expected?

Suspicious signs:

- Hidden recipients using BCC
- Large recipient lists
- Unknown recipients

---

## Reply-To Address

The Reply-To field shows where responses are sent.

Attackers may use:

- Fake From address
- Different Reply-To address

Example:
From:
support@company.com

Reply-To:
attacker@gmail.com

Purpose:

Redirect replies to the attacker.

---

## Date and Time

Check:

- Sending time
- Date
- Time zone

Possible indicators:

- Unusual sending hours
- Date mismatch
- Inconsistent information

---

# Email Body Artifacts

The email body contains information used to identify malicious activity.

---

## URLs and Hyperlinks

Extract all links from the email.

Check:

- Real destination
- Domain reputation
- Redirect chains
- Shortened URLs

Never trust:

- Displayed text
- Buttons
- Embedded links

Displayed: Click here to verify account

Actual link:
http://malicious-site.com/login

---

## Attachments

Analyze:

- File name
- File extension
- File type
- Hash value

Suspicious examples:
- invoice.pdf.exe
- payment.docm
- update.zip
  
Red flags:

- Unexpected attachments
- Executable files
- Macro-enabled documents

---

## File Hashes

A hash is a unique identifier for a file.

Common algorithms:

- MD5
- SHA-1
- SHA-256

Example: sha256sum suspicious_file.pdf

Hashes are used to:

- Search threat intelligence databases
- Identify known malware
- Compare files

---

# HTML Artifacts

HTML emails may contain hidden information.

Analysts look for:

- Hidden URLs
- External resources
- Tracking pixels
- Suspicious scripts

---

## Tracking Pixels

Small invisible images used to track users.

Attackers can learn:

- When an email was opened
- User activity
- Email client information

---

# IOC Collection

During investigation collect:

## Email Indicators

- Sender address
- Reply-To address
- Domains

## Network Indicators

- IP addresses
- URLs
- Domains

## File Indicators

- File names
- File hashes
- Attachment types

---

# Investigation Workflow

Basic email artifact collection:

1. Extract email headers
2. Check sender information
3. Analyze subject
4. Review recipients
5. Compare Reply-To address
6. Extract URLs
7. Analyze attachments
8. Generate hashes
9. Search IOCs
10. Document findings

---

# Useful Tools

## Email Header Analysis

- Google Messageheader
- Message Header Analyzer
- PhishTool

## URL Analysis

- URLScan.io
- VirusTotal
- Cisco Talos

## File Analysis

- VirusTotal
- ANY.RUN
- Hybrid Analysis

---

# Key Takeaways

- Email artifacts provide evidence during investigations
- Headers reveal technical information
- URLs and attachments are common attack vectors
- IOCs help identify malicious activity
- Proper documentation is important in SOC workflows
