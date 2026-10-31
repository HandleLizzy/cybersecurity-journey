# Phishing Email Investigations

## 1. Introduction

Phishing is a social engineering attack in which cybercriminals impersonate trusted individuals or organisations to trick victims into revealing sensitive information, clicking malicious links or downloading harmful attachments.

As a SOC Analyst, understanding how to identify and investigate phishing emails is an important skill.

## 2. Common Types of Phishing

- **Email Phishing:** Fraudulent emails designed to steal information or deliver malware.
- **Spear Phishing:** Targeted attacks against specific individuals or organisations.
- **Whaling:** Phishing attacks targeting senior executives.
- **Smishing:** Phishing conducted through SMS messages.
- **Vishing:** Phishing conducted through voice calls.
- **Business Email Compromise (BEC):** Attackers impersonate or compromise business email accounts to deceive employees.


## 3. Identifying Suspicious Emails

Common phishing indicators include:

- Unfamiliar or spoofed sender addresses.
- Urgent or threatening language.
- Unexpected attachments.
- Suspicious hyperlinks.
- Requests for passwords or financial information.
- Spelling and grammatical mistakes.
- Mismatched sender names and email addresses.

One indicator alone does not prove an email is malicious. Analysts must examine the available evidence.

## 4. Email Header Analysis

### Practical Learning: Email Headers

An email consists of two main components:

- **Email Header:** Contains metadata about the email, including sender, recipient, subject and delivery information.
- **Email Body:** Contains the actual message, which may include text, HTML, links and attachments.

#### Important Email Header Fields

| Header Field | Purpose |
|---|---|
| From | Displays the sender's email address |
| To | Identifies the recipient |
| Reply-To | Specifies where replies are directed |
| Subject | Displays the email subject |
| Date | Indicates when the email was sent |
| Received | Records the email's delivery route |
| Return-Path | Identifies the envelope sender |
| Message-ID | Provides a unique email identifier |

#### Viewing Raw Email Source

In Thunderbird, the raw email source can be accessed through:

**View → Message Source**

Keyboard shortcut: `Ctrl + U`

Viewing the raw source allows analysts to inspect additional technical information that may not be visible in the normal inbox.

#### SOC Analyst Relevance

Email header analysis helps security analysts:
- Investigate suspicious sender information.
- Examine email delivery routes.
- Identify possible sender spoofing.
- Review email authentication results.
- Gather evidence during phishing investigations.

**Practical Exercise:** TryHackMe – Phishing Analysis Fundamentals, Task 4: Email Headers.


## 5. Email Authentication

Three important email authentication mechanisms are:

- **SPF:** Identifies authorised mail servers for a domain.
- **DKIM:** Uses digital signatures to help verify email authenticity and integrity.
- **DMARC:** Defines how receiving servers should handle messages that fail SPF and DKIM alignment checks.

These mechanisms help organisations reduce email spoofing.

## 6. Phishing Investigation Process

A typical phishing investigation involves:

1. Reviewing the suspicious email.
2. Examining sender information and email headers.
3. Identifying suspicious links and attachments.
4. Investigating domains and URLs using appropriate tools.
5. Extracting Indicators of Compromise (IOCs).
6. Assessing the evidence and determining the threat.
7. Documenting findings and recommending mitigation.

## 7. Investigation Tools

Tools that can assist with phishing investigations include:

- VirusTotal – URL, domain and file reputation analysis.
- urlscan.io – Website and URL analysis.
- MXToolbox – Email and DNS diagnostics.
- CyberChef – Data decoding and analysis.
- Google Admin Toolbox Messageheader – Email header analysis.

## 8. Indicators of Compromise (IOCs)

IOCs are observable indicators that may suggest malicious activity.

Examples include:

- Suspicious email addresses.
- Malicious URLs.
- Suspicious domains.
- Malicious attachment hashes.
- IP addresses associated with malicious infrastructure.

## 9. Investigation Findings

Practical investigation findings will be documented here as I complete the TryHackMe Phishing Analysis exercises.

## 10. Defensive Recommendations

- Implement email security filtering.
- Configure SPF, DKIM and DMARC.
- Enable multi-factor authentication.
- Train employees to recognise phishing.
- Establish procedures for reporting suspicious emails.
- Investigate and contain confirmed phishing incidents.

## 11. Project Status

**Status:** In Progress

**Learning Platform:** TryHackMe

**Focus:** Phishing Detection, Email Analysis and SOC Investigation.v &#x20;


## Practical Investigation 01: Email Header Analysis

**Platform:** TryHackMe  
**Task:** Email Headers  
**Email subject:** Help protect your budget by protecting your home  
**Date in email:** 21 June 2021

### Objective
Examine a raw email source to identify sender information, email routing details, authentication results and potentially suspicious indicators.

### Evidence Collected

| Field | Observed Value |
|---|---|
| From | newsletters@ant.anki-tech.com |
| Display Name | ADT Security Services |
| Recipient | alexa@yahoo.com |
| Reply-To | reply@ant.anki-tech.com |
| Originating IP | 43.255.56.161 |
| Sending Host | smtp3-160.piican.com |
| SPF | Pass |
| DKIM | Pass |
| DMARC | Pass |

### Observations

1. The display name claims to represent ADT Security Services, while the sender uses the domain ant.anki-tech.com.
2. The originating IP address identified in the email is 43.255.56.161.
3. SPF, DKIM and DMARC authentication checks all passed for the sending domain.
4. The HTML email contains image references to blueoceanfresh.com.
5. The message includes marketing click-tracking and unsubscribe links.

### Preliminary Assessment

The email contains domain inconsistencies that warrant further investigation. However, successful authentication indicates that the sending domain passed its configured email authentication checks.

Authentication success does not establish that the message is legitimate or that the sender is authorised to represent ADT.

The email cannot be conclusively classified as phishing based on the available evidence.

### Next Steps

- Investigate the originating IP address.
- Examine the reputation of the sending and image-hosting domains.
- Investigate the destinations of the tracking URLs.
- Establish whether the sender is an authorised marketing provider for ADT.

### Skills Practised

- Raw email source inspection.
- Email header analysis.
- Sender and domain investigation.
- SPF, DKIM and DMARC interpretation.
- IOC identification.
- Preliminary threat assessment.
