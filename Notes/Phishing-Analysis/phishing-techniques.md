# Phishing Techniques

## Overview

Phishing is a social engineering attack where attackers impersonate trusted entities to trick users into performing actions such as:

- Clicking malicious links
- Opening attachments
- Sharing sensitive information
- Entering credentials on fake websites

The main goal of phishing is usually:

- Credential theft
- Malware delivery
- Financial fraud
- Unauthorized access

---

# Common Phishing Types

## Phishing

General phishing attacks sent to many users.

Attackers usually pretend to be:

- Banks
- Technology companies
- Delivery services
- Online platforms

Example:

A fake Microsoft email asking users to verify their account.

---

## Spear Phishing

A targeted phishing attack against a specific person or organization.

Attackers often collect information about the victim before creating the email.

Used information can include:

- Name
- Job position
- Company details
- Public information

Goal:

Make the email appear more realistic.

---

## Whaling

A type of spear phishing targeting high-level employees.

Common targets:

- CEO
- CFO
- Managers
- Executives

Goals:

- Steal sensitive information
- Perform financial fraud
- Gain access to company systems

---

## Smishing

Phishing performed through SMS messages.

Common examples:

- Fake delivery notifications
- Fake banking alerts
- Account verification messages

---

## Vishing

Phishing performed through voice calls.

Attackers use social engineering techniques to:

- Gain trust
- Collect information
- Trick users into performing actions

---

# Common Phishing Techniques

## Spoofed Email Address

Attackers modify sender information to appear as a trusted organization.

Example: support@microsoft-security.com

Red flags:

- Domain does not match the official company
- Misspelled domains
- Suspicious email addresses

Always check the real sender address.

---

## Brand Impersonation

Attackers copy legitimate companies to make emails look trustworthy.

They may use:

- Company logos
- Colors
- Email templates
- Similar formatting

Common impersonated brands:

- Microsoft
- PayPal
- Netflix
- Apple
- Delivery companies

---

## Sense of Urgency

Attackers create pressure to make users act quickly.

Examples:

- "Your account will be locked"
- "Payment required immediately"
- "Suspicious login detected"

Purpose:

Prevent users from carefully checking the message.

---

## Credential Harvesting

Attackers create fake login pages to steal credentials.

The fake website may imitate:

- Microsoft login
- Google login
- Banking portals

Collected information:

- Username
- Password
- Session information

---

## Malicious Links

Phishing emails often contain links leading to malicious websites.

Common techniques:

- URL shortening
- Hidden links
- Redirect chains
- Similar-looking domains

Example:

Fake: micros0ft-login.com

Real: microsoft.com

---

## Malicious Attachments

Attackers use files to deliver malware.

Common file types:

- PDF
- Office documents
- ZIP archives
- Executable files

Examples:
- invoice.pdf.exe
- update.docm
- payment.xlsx
- 
Possible results:

- Malware infection
- Credential theft
- Remote access

---

## HTML Email Abuse

Attackers use HTML emails to create realistic-looking messages.

Can include:

- Fake buttons
- Hidden URLs
- Images
- Tracking pixels

HTML source analysis can reveal hidden malicious content.

---

# Social Engineering Indicators

Common warning signs:

## Unexpected Emails

Be careful with emails you did not expect.

Examples:

- Unknown invoices
- Password reset messages
- Delivery notifications

---

## Generic Greetings

Example: Dear Customer

instead of using a real name.

---

## Suspicious Language

Indicators:

- Grammar mistakes
- Strange wording
- Unusual requests

Note:

Modern attackers can use AI to create realistic emails, so grammar alone is not enough.

---

# Phishing Attack Flow

Typical phishing attack:
Email received
↓
User clicks link
↓
Fake website opens
↓
Credentials entered
↓
Credentials sent to attacker
↓
Account compromise

---

# SOC Analyst Detection

During phishing analysis check:

## Sender

- Email address
- Domain reputation
- Reply-To address

## Message

- Urgency
- Branding
- Language
- Social engineering techniques

## Links

- Destination URL
- Domain reputation
- Redirects

## Attachments

- File type
- Hash
- Suspicious behavior

---

# Key Takeaways

- Phishing relies on social engineering
- Attackers impersonate trusted organizations
- Always verify senders and links
- Do not trust unexpected attachments
- Collect indicators for further investigation
- Understanding phishing techniques helps SOC analysts detect attacks
