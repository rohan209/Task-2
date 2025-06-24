## 📧 Phishing Email Analysis Report

### 📝 Objective
Identify and document phishing characteristics in a suspicious email using forensic techniques.

---

### 🛠️ Tools Used
- Email client or `.txt` file viewer
- [MxToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- VirusTotal (https://virustotal.com)
- Web browser (for inspecting link destinations)

---

### 📂 Sample Phishing Email (Safe Text Version)

From: Netflix Support no-reply@netfliix-billing.com

To: user@example.com

Subject: Payment Failed – Your Account Will Be Cancelled

Dear Customer,

We were unable to process your recent payment. Your Netflix subscription will be cancelled within 24 hours unless billing information is updated.
Please update your payment details by clicking the secure link below:
https://www.netflix.com.account-update-secure.com/payment
Failure to act will result in immediate service interruption.
If you have any questions, please contact our support team.

Thanks for being a valued member.

Netflix Billing Department


---

### 🔍 Phishing Indicators Found

| Feature                         | Observation                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| Spoofed sender address           | `no-reply@netfliix-billing.com` – extra “i” in `netfliix`                   |
| Header discrepancies             | Would likely show spoofed origin, unverified SPF/DKIM                      |
| Urgency and threatening tone     | “Account will be cancelled within 24 hours”                                |
| Suspicious link                  | Displayed as Netflix, real domain is `account-update-secure.com`           |
| Attachment                       | No attachment in this case, but link is likely to a fake login form        |
| Generic greeting                 | “Dear Customer” instead of actual name                                     |
| Spelling/grammar issues          | Slightly awkward sentence: “Failure to act will result in immediate…”      |

---

### ✅ Summary

This phishing email impersonates Netflix to scare the user into clicking a malicious payment update link. It uses a typo-squatted domain, vague greeting, and urgent language to pressure the victim. The link leads to a fake site intended to steal payment details.
