# Phishing Email Analysis

## Project Overview

This project documents an investigation of an ADT-themed promotional email received on 21 June 2021.

The investigation involved examining email headers, authentication results, sender information, URLs, associated domains and threat intelligence findings.

The objective was to apply practical SOC investigation techniques and document findings in a structured report.

## Investigation Summary

| Item | Finding |
|---|---|
| Display Name | ADT Security Services |
| Sender Domain | ant.anki-tech.com |
| Originating IP | 43.255.56.161 |
| SPF | PASS |
| DKIM | PASS |
| DMARC | PASS |
| Overall Assessment | Inconclusive |

## Skills Demonstrated

- Phishing email analysis
- Email header investigation
- SPF, DKIM and DMARC interpretation
- Indicator extraction
- Domain and URL reputation checks
- VirusTotal analysis
- Evidence documentation
- Security investigation reporting

## Tools Used

- Mozilla Thunderbird
- VirusTotal
- TryHackMe
- GitHub

## Project Structure

| Folder | Description |
|---|---|
| `investigations/` | Investigation overview and findings |
| `IOCs/` | Extracted indicators |
| `reports/
