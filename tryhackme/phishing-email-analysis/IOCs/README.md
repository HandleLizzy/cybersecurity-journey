# Indicators of Compromise (IOCs)

## Overview

This document records the indicators identified during the phishing email investigation.

The indicators were extracted from the available email headers and examined as part of the investigation.

**Note:** Identified indicators are not automatically confirmed malicious.

## Identified Indicators

| Indicator Type | Value | Description |
|---|---|---|
| Sender Email | newsletters@ant.anki-tech.com | Email sender address |
| Reply-To | reply@ant.anki-tech.com | Reply destination |
| Domain | ant.anki-tech.com | Sender domain |
| IP Address | 43.255.56.161 | Originating IP address |

## Threat Intelligence Results

VirusTotal was used to investigate available indicators.

| Indicator | Result |
|---|---|
| Domain | 0/92 vendors flagged |
| Investigated URL | 0/91 vendors flagged |

These results represent the recorded detection results at the time of investigation and do not establish that the indicators are safe.

## Assessment

- The sender domain was identified for further investigation.
- The originating IP address was extracted from the email headers.
- The investigated domain and URL received no detections in the recorded VirusTotal results.
- No indicator was conclusively established as malicious based on the available evidence.

## Limitations

The exact investigated URL and its full analysis details should be retained with the supporting evidence. The originating IP address also requires further reputation analysis before any malicious classification can be made.

## Conclusion

The identified indicators provide useful starting points for further threat intelligence investigation. Based on the available evidence, their malicious status remains unconfirmed.
