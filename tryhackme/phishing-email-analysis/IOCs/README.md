# Indicators of Compromise (IOCs)

## Overview

This file documents the indicators extracted from the ADT-themed promotional email investigated in this project.

The indicators are recorded for investigation and reference purposes. Their presence does not automatically establish malicious activity.

## 1. Email Indicators

| Indicator Type | Value |
|---|---|
| Sender Email | newsletters@ant.anki-tech.com |
| Reply-To Email | reply@ant.anki-tech.com |
| Sender Domain | ant.anki-tech.com |
| Originating IP Address | 43.255.56.161 |

## 2. URL Indicator

**Main promotional tracking URL:**

`https://ant.anki-tech.com/ga/click/2-952622232-3970-423304-838253-590962-350694bcf9-17b3b9c21a`

The URL was extracted from the original email source. Its final destination was not independently verified.

## 3. Image-Hosting Domain

| Indicator Type | Value |
|---|---|
| Domain | blueoceanfresh.com |
| Purpose observed | Hosting images referenced in the email HTML |

## 4. VirusTotal Results

| Indicator | Result |
|---|---|
| ant.anki-tech.com | 0/92 detections |
| Promotional tracking URL | 0/91 detections |
| blueoceanfresh.com | 0/92 detections |

These are the results displayed in the VirusTotal reports reviewed during the investigation. Zero detections do not guarantee that an indicator is safe.

## 5. Handling and Assessment

- Preserve these indicators as investigation evidence.
- Do not open suspicious links directly.
- Verify URLs in a controlled analysis environment.
- Reassess indicators if new threat intelligence becomes available.

**Overall assessment:** Inconclusive. No confirmed malicious activity was established from the available evidence.
