# URL Analysis

## Overview

URLs are one of the most common elements used in phishing attacks.

Attackers use malicious links to:

- Steal credentials
- Redirect users to fake websites
- Deliver malware
- Track victims

SOC analysts analyze URLs to determine if they are malicious.

---

# URL Structure

Example: https://login.example.com/account

A URL contains:

## Protocol

Defines how the connection is made.

Examples:
- http://
- https://

HTTPS uses encryption, but it does not guarantee that a website is safe.

---

## Domain

The main website address.

Example: example.com

Analysts check:

- Domain age
- Reputation
- Ownership
- Similarity to legitimate domains

---

## Subdomain

Part before the main domain.

Example: login.example.com

Attackers may use subdomains to appear legitimate.

Example: microsoft.fake-domain.com

The real domain is: fake-domain.com

---

# Common Malicious URL Techniques

## Domain Spoofing

Attackers create domains similar to legitimate websites.

Examples:

Real: paypal.com

Fake: paypa1.com

Common changes:

- Replacing letters with numbers
- Adding extra words
- Misspellings

---

## URL Shortening

Attackers use shortened URLs to hide destinations.

Examples:

- bit.ly
- tinyurl

Problems:

- Hides the real domain
- Makes analysis harder
- Can redirect multiple times

Always expand shortened URLs before visiting.

---

## Redirect Chains

Attackers use multiple redirects.

Example:
Email link
↓
Short URL
↓
Fake website
↓
Credential harvesting page

Purpose:

- Hide final destination
- Avoid security filters
- Make investigation harder

---

## Fake Login Pages

A common phishing technique.

Attackers create pages that imitate:

- Microsoft
- Google
- Apple
- Banking websites

Goal:

Steal:

- Usernames
- Passwords
- Session tokens

---

# URL Investigation Process

## Step 1 - Extract URL

Collect URLs from:

- Email body
- HTML source
- Attachments
- Buttons

Do not click suspicious links.

---

## Step 2 - Defang URL

Defanging prevents accidental clicks.

Example:

Original: http://malicious.com/login

Defanged: hxxp[://]malicious[.]com/login

Common changes:
. → [.]
http:// → hxxp://

---

## Step 3 - Analyze Domain

Check:

- Domain reputation
- Registration date
- Ownership
- Previous malicious activity

Questions:

- Is the domain new?
- Does it match the company?
- Has it been reported before?

---

## Step 4 - Check Redirects

Look for:

- Hidden destinations
- Multiple redirects
- Suspicious domains

Tools can reveal the complete redirect chain.

---

# URL Analysis Tools

## URLScan.io

Used for safe website analysis.

Provides:

- Screenshots
- Network requests
- Redirect information
- Domain information

---

## VirusTotal

Can analyze:

- URLs
- Domains
- IP addresses

Provides:

- Security vendor detections
- Reputation information
- Previous reports

---

## Cisco Talos

Used for reputation checks.

Analyzes:

- Domains
- IP addresses
- Threat intelligence data

---

# URL Red Flags

Suspicious indicators:

## Long URLs

May contain:

- Tracking data
- Encoded information
- Redirect parameters

---

## Unknown Domains

Be careful with:

- Newly created domains
- Random names
- Free hosting domains

---

## Brand Names in Wrong Domains

Example: microsoft-login.security-check.com

The domain is: security-check.com

not Microsoft.

---

## No HTTPS

HTTP does not encrypt communication.

However:

HTTPS ≠ Safe

Malicious websites can also use HTTPS.

---

# SOC Analyst Checklist

When analyzing a suspicious URL:

- Extract the URL
- Defang it
- Identify the real domain
- Check reputation
- Analyze redirects
- Search threat intelligence
- Document findings

---

# Key Takeaways

- Never open suspicious URLs directly
- Check the real domain, not only the visible text
- Attackers use redirects to hide malicious destinations
- URL analysis helps identify phishing infrastructure
- Always collect URLs as IOCs
