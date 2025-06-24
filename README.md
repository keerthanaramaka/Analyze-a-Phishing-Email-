# Analyze-a-Phishing-Email:Apple ID Account Lock Scam
## overview
The email analyzed is a phishing attempt impersonating Apple Support. It aims to trick users into revealing sensitive information or downloading malware. Multiple red flags confirm its malicious nature:
- Spoofed Email Address
- Fake Login Link
- Malicious Attachment
- Generic Greeting
- Foreign Login Alert
- Email Authentication Failures
## key findings
| **Indicator**            | **Details**                                                               | **Severity** |
| ------------------------ | ------------------------------------------------------------------------- | ------------ |
| **Spoofed Email Domain** | `apple-secure-login.com` mimics Apple but is not an official domain       | High         |
| **Mismatched URL**       | Visible link resembles Apple, but actually redirects to a phishing domain | High         |
| **Urgency Tactic**       | Claims the Apple ID will be "permanently disabled" in 24 hours            | High         |
| **Attachment Trick**     | `.pdf.exe` is a disguised executable potentially carrying malware         | Critical     |
| **Generic Greeting**     | "Dear Customer" instead of personalized name                              | Medium       |
| **Login Location Bait**  | "Lagos, Nigeria" used to trigger suspicion and fear                       | Medium       |
## Header Analysis
| **Header Field**  | **Finding**                                                           |
| ----------------- | --------------------------------------------------------------------- |
| Return-Path       | `<noreply@apple-support-alert.ru>` (Non-Apple source)                 |
| SPF Check         | **Fail** – Unauthorized sender                                        |
| DKIM Check        | **Fail** – Invalid signature                                          |
| DMARC Check       | **Fail** – Sender not aligned with domain policy                      |
| Source IP Address | `185.200.118.42` – Found on **Spamhaus** and **AbuseIPDB** blacklists |
##  Tools Used
✅ MXToolbox Header Analyzer

✅ AbuseIPDB & VirusTotal (for IP and domain reputation)

✅ WHOIS Lookup (to verify domain ownership)

✅ Manual Content & Link Review
##  Safety Recommendations
- Never click links in emails asking for sensitive information
- Verify sender email domains – Apple uses @apple.com only
- Manually access websites like https://appleid.apple.com
- Do not open attachments unless verified
- Report phishing attempts to: reportphishing@apple.com
