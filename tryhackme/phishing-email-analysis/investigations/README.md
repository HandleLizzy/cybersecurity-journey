# Phishing Email Investigation Report

## 1. Incident Overview

This investigation examines an email displaying the name **ADT Security Services** and containing promotional content.

The email was received by `alexa@yahoo.com` on **21 June 2021 at 15:36:02 UTC**.

**Subject:** Help protect your budget by protecting your home

The investigation involved reviewing the email source and headers, examining authentication results, extracting relevant indicators, and checking available VirusTotal reports.

### Investigation Objective

To assess whether the email contains indicators of phishing or other suspicious activity and document an evidence-based assessment.

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
- The HTML source references images hosted on `blueoceanfresh.com`, a domain separate from the sender domain.
- Thunderbird blocked remote content when the email was viewed.

These observations identify items for investigation but do not independently prove that the email is malicious.

## 3. Email Header Analysis

The original email headers were reviewed to examine the sending infrastructure and authentication results.

### Authentication Results

| Authentication Check | Result |
|---|---|
| SPF | PASS |
| DKIM | PASS |
| DMARC | PASS |

### Header Findings

- The originating IP recorded in the email headers was `43.255.56.161`.
- SPF passed, indicating that the sending IP was authorised by the sender domain's SPF configuration.
- DKIM authentication passed for `ant.anki-tech.com`.
- DMARC passed. The recorded DMARC policy was `p=NONE`.

### Assessment

The email passed all three recorded authentication checks. This indicates that the message passed the configured authentication checks for the sender domain. However, successful email authentication does not establish that the sender's displayed identity or the email content is legitimate.

## 4. Threat Intelligence Analysis

VirusTotal was used to review the sender domain, the main promotional tracking URL, and the domain hosting images referenced in the email.

### 4.1 Sender Domain

- **Indicator:** `ant.anki-tech.com`
- **VirusTotal result:** 0/92 security vendors flagged the domain as malicious.
- **Last analysis shown:** 11 days ago.

### 4.2 Promotional Tracking URL

The main promotional call-to-action URL extracted from the email source was:

`https://ant.anki-tech.com/ga/click/2-952622232-3970-423304-838253-590962-350694bcf9-17b3b9c21a`

- **VirusTotal result:** 0/91 security vendors flagged the URL as malicious.
- **Report timestamp shown:** 15 September 2026, 09:27:19 UTC.
- **Last analysis shown:** 1 month ago.
- The VirusTotal URL report also displayed `43.255.56.3` as a related IP address. This is separate from the email's originating IP, `43.255.56.161`, and was not independently assessed in this investigation.

### 4.3 Image-Hosting Domain

- **Indicator:** `blueoceanfresh.com`
- **VirusTotal result:** 0/92 security vendors flagged the domain as malicious.
- **Last analysis shown:** 5 months ago.
- The domain appears in image URLs within the email's HTML source.

### Threat Intelligence Assessment

None of the three reviewed domain and URL indicators received malicious detections in the VirusTotal results provided.

These results do not guarantee that the indicators are safe. The analyses were performed at different times, and a zero-detection result is not proof of legitimacy.

## 5. Suspicious Observations and Limitations

The following points warrant attention:

1. **Displayed sender identity:** The email displays the name ADT Security Services, while the sender address uses `ant.anki-tech.com`. This difference warrants verification but does not, by itself, prove impersonation.

2. **Separate image-hosting domain:** The HTML source references images hosted on `blueoceanfresh.com`, which differs from the sender domain. This is an observation requiring context, not proof of malicious activity.

3. **Tracking URL:** The promotional call-to-action uses a tracking URL on `ant.anki-tech.com`. Its final destination was not independently verified.

4. **Remote content:** Thunderbird blocked remote content when the email was viewed. The external content was therefore not loaded automatically.

### Investigation Limitations

- The final destination and behaviour of the promotional tracking URL were not independently verified.
- The VirusTotal results represent the analysis information shown at the time of review and may change.
- The related IP `43.255.56.3` displayed in the URL report was not independently investigated.
- The available evidence was insufficient to establish whether the email was genuinely authorised by ADT Security Services.

## 6. Final Assessment and Recommendations

### Final Assessment: Inconclusive

Based on the available evidence, the email cannot be conclusively classified as either legitimate or malicious.

The message passed SPF, DKIM and DMARC authentication checks. VirusTotal reported zero malicious detections for the sender domain, promotional tracking URL and image-hosting domain in the results reviewed.

However, the displayed sender identity requires verification, the email references a separate image-hosting domain, and the final destination of the promotional tracking URL was not established.

### Recommendations

- Do not follow promotional links unless their destinations have been independently verified.
- Verify unexpected messages claiming to represent an organisation through independently obtained contact details.
- Preserve the original email and its headers for further investigation.
- Recheck relevant indicators if new evidence becomes available.
- Avoid treating a zero-detection VirusTotal result as confirmation that an indicator is safe.

### Investigation Outcome

The investigation documented the email's available metadata, authentication results, extracted indicators, threat intelligence findings and outstanding verification requirements.

**Outcome:** Inconclusive — no confirmed malicious activity was established from the evidence reviewed.

## 7. Supporting Evidence

The following screenshots are stored in the project's `screenshots/` folder:

1. [Email headers](../screenshots/01-email-headers.png)
2. [Email authentication](../screenshots/02-email-authentication.png)
3. [Sender domain VirusTotal result](../screenshots/03-virustotal-domain.png)
4. [Promotional URL VirusTotal result](../screenshots/04-virustotal-url.png)
5. [Image-hosting domain VirusTotal result](../screenshots/05-virustotal-image-domain.png)
