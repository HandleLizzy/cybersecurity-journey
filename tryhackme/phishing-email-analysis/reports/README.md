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


## 3. Email Header Analysis

The original email headers were reviewed to examine the sending infrastructure and authentication results.

### Authentication Results

| Authentication Check | Result |
|---|---|
| SPF | PASS |
| DKIM | PASS |
| DMARC | PASS |

### Header Observations

- The originating IP address was `43.255.56.161`.
- The SPF result indicates that the IP was authorised to send email for `ant.anki-tech.com`.
- DKIM authentication passed for the sender domain.
- DMARC authentication also passed, with the policy set to `p=NONE`.

### Assessment

All three email authentication checks passed. This indicates that the message passed the domain's configured authentication checks. However, successful authentication does not guarantee that the email content is legitimate or safe.

- The display name identifies the sender as ADT Security Services.
- The sender and Reply-To addresses use the `ant.anki-tech.com` domain.
- The email contains promotional content and tracking links.
- The email's HTML source references images hosted on `blueoceanfresh.com`, a separate domain.

**Note:** These observations identify items for further investigation; they do not independently establish that the email is malicious.


## 4. Threat Intelligence Analysis

VirusTotal was used to review the sender domain, the promotional tracking URL, and the domain hosting images referenced in the email.

### 4.1 Sender Domain

- **Indicator:** `ant.anki-tech.com`
- **VirusTotal result:** 0/92 security vendors flagged the domain as malicious.
- **Last analysis:** 11 days before this investigation was documented.

### 4.2 Promotional Tracking URL

- **Indicator:** Main promotional CTA tracking URL on `ant.anki-tech.com`
- **VirusTotal result:** 0/91 security vendors flagged the URL as malicious.
- **Last analysis:** 1 month ago.

### 4.3 Image-Hosting Domain

- **Indicator:** `blueoceanfresh.com`
- **VirusTotal result:** 0/92 security vendors flagged the domain as malicious.
- **Last analysis:** 5 months ago.

### Threat Intelligence Assessment

None of the three indicators received malicious detections in the VirusTotal results reviewed. However, these results do not guarantee that the indicators are safe. The analysis dates also differ, so the results should be understood in their respective time contexts.

## 5. Suspicious Observations

The following observations were identified during the investigation:

1. **Sender identity:** The email displays the name ADT Security Services, while the sender address uses `ant.anki-tech.com`. This difference warrants further verification but does not prove impersonation.

2. **Separate image-hosting domain:** The HTML email references images hosted on `blueoceanfresh.com`, which differs from the sender domain.

3. **Tracking links:** The promotional call-to-action uses a tracking URL on `ant.anki-tech.com`. Tracking links are common in marketing emails, but their final destination should be verified before being trusted.

4. **Remote content blocked:** Thunderbird blocked remote content when the email was viewed. This prevented the external content from loading automatically.

### Limitations

- The final destination of the promotional tracking URL was not independently verified.
- No malicious detections were reported for the three indicators in the VirusTotal results reviewed.
- The original email's legitimacy could not be confirmed from the available evidence alone.


## 6. Final Assessment and Recommendations

### Final Assessment: Inconclusive

Based on the available evidence, the email cannot be conclusively classified as either legitimate or malicious.

The email passed SPF, DKIM and DMARC authentication checks. VirusTotal also reported no malicious detections for the sender domain, promotional tracking URL or image-hosting domain at the time of their respective analyses.

However, the difference between the displayed sender identity and sender domain, the use of a separate image-hosting domain, and the presence of tracking links warrant further verification.

### Recommendations

- Do not click promotional links unless their final destinations have been verified.
- Verify unexpected promotional emails directly with the organisation using independently obtained contact details.
- Continue monitoring the sender domain and associated indicators for changes in reputation.
- Preserve the original email and headers for further investigation.
- Treat the email cautiously until its legitimacy can be established.

### Investigation Outcome

The investigation documented the available email evidence, authentication results, threat intelligence findings and areas requiring further verification.

**Outcome:** Inconclusive — no confirmed malicious activity identified from the evidence reviewed.
