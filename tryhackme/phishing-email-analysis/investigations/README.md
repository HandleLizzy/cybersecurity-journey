# Phishing Email Investigation

## Investigation Overview

This investigation examines a promotional email displaying the name **ADT Security Services**, received on 21 June 2021.

The objective was to examine the email's metadata, authentication results, associated URLs and domains, and available threat intelligence to assess potential phishing indicators.

## Email Under Investigation

| Field | Details |
|---|---|
| Display Name | ADT Security Services |
| Sender | newsletters@ant.anki-tech.com |
| Recipient | alexa@yahoo.com |
| Subject | Help protect your budget by protecting your home |
| Date | 21 June 2021 |
| Originating IP | 43.255.56.161 |

## Investigation Activities

The following activities were completed:

1. Reviewed the original email and its available content.
2. Examined the raw email headers.
3. Checked SPF, DKIM and DMARC authentication results.
4. Extracted the sender domain, Reply-To address, originating IP and promotional tracking URL.
5. Identified the separate image-hosting domain referenced in the email's HTML source.
6. Reviewed the sender domain, promotional URL and image-hosting domain using VirusTotal.
7. Documented observations, limitations and recommendations.

## Key Findings

- SPF, DKIM and DMARC authentication checks passed.
- VirusTotal reported 0/92 detections for `ant.anki-tech.com`.
- VirusTotal reported 0/91 detections for the promotional tracking URL.
- VirusTotal reported 0/92 detections for `blueoceanfresh.com`.
- The email referenced an image-hosting domain separate from its sender domain.
- Thunderbird blocked remote content when the email was viewed.
- The final destination of the promotional tracking URL was not independently verified.

## Investigation Conclusion

**Assessment: Inconclusive**

The available evidence did not establish that the email was malicious or confirm that it was genuinely authorised by ADT Security Services.

Successful email authentication and zero VirusTotal detections do not guarantee that an email or its associated indicators are safe.

Further verification would be required to reach a definitive conclusion.

## Project Resources

- [Full Investigation Report](../reports/README.md)
- [Indicators of Compromise (IOCs)](../IOCs/README.md)
- [Screenshots and Evidence](../screenshots/README.md)
- [Tools Used](../tools/README.md)

## Evidence

Screenshots supporting this investigation are available in the [screenshots folder](../screenshots/).
