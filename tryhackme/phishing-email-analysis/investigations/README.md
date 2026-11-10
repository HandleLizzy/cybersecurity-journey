# Phishing Email Investigation

## 1. Investigation Overview

This investigation examines an ADT-themed promotional email received on 21 June 2021.

The objective was to assess the email's authenticity and identify potential indicators of phishing through email header analysis, authentication checks, threat intelligence and available security evidence.

## 2. Email Details

| Field | Value |
|---|---|
| Sender display name | ADT Security Services |
| Sender domain | ant.anki-tech.com |
| Recipient | alexa@yahoo.com |
| Subject | Help protect your budget by protecting your home |
| Date received | 21 June 2021 |
| Time received | 15:36 UTC |
| Originating IP | 43.255.56.161 |

## 3. Email Header Analysis

The email headers were examined to identify the sending infrastructure and authentication results.

The following authentication results were observed:

- SPF: Pass
- DKIM: Pass
- DMARC: Pass

These results indicate that the email passed the recorded authentication checks. However, successful authentication does not independently establish
