# Email Basics

## Overview

Email is one of the most common communication methods and one of the most used attack vectors in cybersecurity.

SOC analysts need to understand how emails work in order to investigate phishing attempts and identify malicious activity.

---

# Email Address Structure

Example: david@tryhackme.com

An email address contains three main parts:

## Username

Identifies the user's mailbox.

Example: david

## @ Symbol

Separates the username from the domain.

## Domain

Identifies the mail server or organization.

Example: tryhackme.com

---

# Email Communication

When an email is sent, it travels through multiple systems before reaching the recipient.

Basic flow:
Sender
↓
SMTP Server
↓
Internet
↓
Recipient Mail Server
↓
Recipient

---

# Email Protocols

## SMTP (Simple Mail Transfer Protocol)

Used for sending emails.

Commonly responsible for:

- Sending messages between mail servers
- Delivering outgoing emails

---

## POP3 (Post Office Protocol)

Used to download emails from a server.

Characteristics:

- Downloads messages to one device
- Emails may be removed from the server
- Mainly used for offline access

---

## IMAP (Internet Message Access Protocol)

Used to synchronize emails between devices.

Characteristics:

- Emails remain stored on the server
- Multiple devices can access the same mailbox
- Changes are synchronized

---

# Email Components

An email consists of two main parts:

## Email Header

Contains technical information about the message.

Important fields:

- From
- To
- Reply-To
- Subject
- Date
- Sender IP
- Mail server information

Headers are important during phishing investigations because they can reveal:

- Fake sender addresses
- Suspicious domains
- Email origin

---

## Email Body

Contains the actual message.

Can include:

- Plain text
- HTML content
- Images
- Links
- Attachments

Attackers often use the email body to:

- Create fake messages
- Add malicious links
- Deliver malware

---

# HTML Emails

Modern emails often use HTML formatting.

HTML emails can contain:

- Images
- Buttons
- Links
- Embedded content

During investigations analysts check HTML code for:

- Hidden links
- Suspicious redirects
- Tracking pixels
- Malicious content

---

# Message Source

Message source shows the raw content of an email.

It can reveal:

- Full headers
- HTML code
- Hidden URLs
- Technical information

Useful shortcut: Ctrl + U

Message source analysis is commonly used during phishing investigations.

---

# Security Relevance

Understanding email basics helps SOC analysts:

- Investigate phishing emails
- Identify malicious senders
- Extract Indicators of Compromise (IOCs)
- Analyze suspicious links and attachments
- Understand attack techniques

---

# Key Takeaways

- Emails contain headers and body content
- SMTP is used for sending emails
- POP3 downloads emails locally
- IMAP synchronizes emails
- Headers provide important investigation data
- Email analysis is a key SOC analyst skill
