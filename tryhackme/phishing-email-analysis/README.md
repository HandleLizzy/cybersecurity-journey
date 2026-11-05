Phishing Email Investigation – ADT-Themed Email

1. Investigation Overview

**Investigation type:** Phishing Email Analysis  
**Email date:** 21 June 2021  
**Status:** Completed – Inconclusive

**Objective:** Analyse an ADT-themed email, examine its headers and associated indicators, and review available threat intelligence and sandbox results to assess potential malicious activity.

2. Email Details

| Field | Finding |
|---|---|
| Sender | newsletters@ant.anki-tech.com |
| Display name | ADT Security Services |
| Reply-To | reply@ant.anki-tech.com |
| Subject | Help protect your budget by protecting your home |
| Sending IP | 43.255.56.161 |

The email advertised ADT home security services, including promotional pricing and a reward card offer. It contained tracking links, unsubscribe links and externally hosted images. No file attachments were identified.

3. Header Analysis

| Authentication check | Result |
|---|---|
| SPF | Pass |
| DKIM | Pass |
| DMARC | Pass (p=NONE) |

All three authentication checks passed. However, this does not independently establish that the sender was authorised by ADT or that the email was safe.

4. IOC Investigation

VirusTotal was used to investigate the sending IP, associated domains, hostname and tracking URL.

| Indicator | Type | Detections |
|---|---|---|
| 43.255.56.161 | IP address | 0/92 |
| ant.anki-tech.com | Domain | 0/92 |
| anki-tech.com | Domain | 0/92 |
| blueoceanfresh.com | Domain | 0/92 |
| smtp3-160.piican.com | Hostname | 0/92 |
| Investigated tracking URL | URL | 0/91 |

Historical DNS information showed that the tracking domain had resolved to multiple IP addresses over time. Shared infrastructure did not establish common ownership or malicious activity.

*Results reflect the time of analysis and do not guarantee that the indicators are safe.*
5. Sandbox Behaviour Analysis

A related email file was examined through its VirusTotal report.

**SHA-256:** `f56d0d5fcbb3e2932032d89746fc16cd97e06be8150aaeb98ac4d02646d71a19`

Observed behaviour included:

- Outlook process activity.
- DNS resolutions involving the email's tracking domain and image host.
- WMI system information queries.
- A medium-severity Sigma rule match.
- Automated MITRE ATT&CK technique mappings.

The Sigma rule concerned an Office application initiating a network connection to a non-local IP address. The exact network event was unavailable, so the match does not confirm malicious activity or exploitation.

*The related email file was not confirmed to be identical to the original sample.*

6. Key Findings

- SPF, DKIM and DMARC authentication checks passed.
- The email contained promotional content and tracking links.
- No attachments were identified in the original email.
- No security vendor detections were reported for the investigated indicators at the time of analysis.
- Sandbox activity generated additional investigation leads, but did not confirm malware execution.
- The sender's association with ADT could not be independently verified.

7. Conclusion

**Final assessment: Inconclusive**

The email resembles a bulk promotional marketing message, but its association with ADT could not be independently verified. Although the authentication checks passed and VirusTotal reported no detections for the investigated indicators, these results do not establish that the email is legitimate.

The sandbox observations warrant attention but do not independently confirm malicious activity. Further verification would be required before trusting the sender or its links.

8. Analyst Recommendations

1. Verify the sender through an official communication channel.
2. Avoid interacting with unverified links.
3. Review email and network logs for similar messages and related connections.
4. Preserve the original email, headers and identified indicators.
5. Escalate if further evidence confirms malicious activity.

9. Investigation Limitations

- The sender's relationship with ADT could not be verified.
- The exact event behind the Sigma rule match was unavailable.
- The related sandbox email file was not confirmed to be identical to the original.
- Recipient interaction with the email could not be established.

**Tools used:** Thunderbird, VirusTotal and TryHackMe.
