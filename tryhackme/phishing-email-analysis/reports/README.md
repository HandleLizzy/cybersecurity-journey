# Phishing Email Investigation Report

## 1. Incident Overview

This investigation examines an email presented as a promotional message from **ADT Security Services**.

The email was received on **21 June 2021 at 15:36 UTC** by `alexa@yahoo.com`. Its subject line was:

**Help protect your budget by protecting your home**

The investigation focused on examining the email headers, reviewing the sender and associated domains, analysing the promotional tracking URL, and checking available threat intelligence results using VirusTotal.

### Investigation Objective

To assess whether the email contains indicators of phishing or other suspicious activity and document the findings using evidence from the email source and security analysis tools.


## 2. Email Details

| Field | Value |
|---|---|
| Display Name | ADT Security Services |
| Sender Address | newsletters@ant.anki-tech.com |
| Reply-To Address | reply@ant.anki-tech.com |
| Recipient | alexa@yahoo.com |
| Subject | Help protect your budget by protecting your home |
| Date Received | 21 June 2021, 15:36:02 UTC |
| Sender Domain | ant.anki-tech.com |
| Originating IP | 43.255.56.161 |

### Initial Observations

- The display name identifies the sender as ADT Security Services.
- The sender and Reply-To addresses use the `ant.anki-tech.com` domain.
- The email contains promotional content and tracking links.
- The email's HTML source references images hosted on `blueoceanfresh.com`, a separate domain.

**Note:** These observations identify items for further investigation; they do not independently establish that the email is malicious.
