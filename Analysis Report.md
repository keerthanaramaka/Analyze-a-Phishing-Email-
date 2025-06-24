# Phishing Email Analysis Report
## Objective
To identify phishing characteristics in a suspicious email claiming to be from Apple, and analyze its technical and behavioral indicators using industry tools and manual inspection.
## Email Summary
- Sender: Apple Support <support@apple-secure-login.com>
- Recipient: user@example.com
- Subject: [Urgent] Your Apple ID has been locked due to suspicious activity
- Attachment: verify_account_info.pdf.exe
- Embedded Link: https://appleid.apple.com.secure-verify-user-login.com
## Finding the Phishing
To identify this email as a phishing attempt, several technical and behavioral clues were analyzed:

🛠️ 1. Sender Domain Spoofing
Observed: support@apple-secure-login.com

Why it's phishing: Not an official Apple domain. Apple uses only @apple.com.

🔗 2. Fake Login Link
Displayed Link: Appears like Apple’s login page.

Actual URL: https://appleid.apple.com.secure-verify-user-login.com

Why it's phishing: Real Apple domain ends in .apple.com. This one is crafted to trick users.

⚠️ 3. Urgency & Threat
Text: "Your Apple ID will be permanently disabled" if no action is taken in 24 hours.

Why it's phishing: Common social engineering trick to pressure the user into clicking quickly.

📎 4. Suspicious Attachment
File: verify_account_info.pdf.exe

Why it's phishing: Double extension hides a malicious executable, likely used to infect systems.

📬 5. Header Authentication Failures
Checks: SPF, DKIM, and DMARC — all failed

Why it's phishing: Indicates the email was not sent from a verified Apple mail server.

🧠 6. Generic Language
Greeting: “Dear Customer”

Why it's phishing: Legitimate Apple emails are personalized.
## Conclusion
- The email is fake and not from Apple.
- It uses a spoofed domain and fake login link.
- Urgent language and malicious attachment are red flags.
- Authentication checks failed (SPF, DKIM, DMARC).
- It is a clear phishing attempt.
- Users should delete and report the email immediately.
## Advice
- Never click unknown links.
- Always check the sender’s email address.
- Report emails like this to your IT or security team.
