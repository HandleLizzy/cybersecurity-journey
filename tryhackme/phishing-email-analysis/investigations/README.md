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

Email headers contain technical information about how an email was sent and delivered.

Important header fields include:

- **From:** Sender address displayed in the email.
- **To:** Intended recipient.
- **Subject:** Email subject line.
- **Date:** Time the email was sent.
- **Return-Path:** Address used for handling email delivery failures.
- **Received:** Records showing the email's routing through mail servers.
- **Message-ID:** Unique identifier assigned to an email message.

Analysing these fields can help identify suspicious sending infrastructure and possible sender spoofing.

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
