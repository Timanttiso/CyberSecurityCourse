# 1️⃣ Introduction

**Tester(s):**  
- Name: Niko Asujamaa

**Purpose:**  
- The purpose of this test is to find vulnerabilities in the bookingsystem's registration page.

**Scope:**  
- Tested components: Registration page
- Exclusions: -
- Test approach: Gray-box 

**Test environment & dates:**  
- Start:  23.1.2026 12.47
- End:  23.1.2026 13.02
- Test environment details (OS, runtime, DB, browsers): Windows 11 Pro, PostgreSQL, Opera GX(Google)

**Assumptions & constraints:**  
- Limited to only testing the registration page of the system.

---

# 2️⃣ Executive Summary

Penetration testing done to the registration page of the booking system with ZAP. The testing showed a lot of faults in the page, such as vulnerabilities to SQL injections, path traversal and the site lacks security in how it stores passwords.

**Overall risk level:** High

**Top 5 immediate actions:**  
1.  Hashing/encrypting passwords in database.
2.  Fix issue with path traversal.
3.  Fix logs exposing username information.
4.  Fix vulnerability to SQL injections.
5.  Fix weak password policy

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration page | Input field allows OR '1'='1` -- and AND '1'='1` -- injections | ZAP report flag |
| F-02 | 🔴 High | Passwords in database exposed | Passwords are not hashed/encrypted in the database | Passwords clearly visible: https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/AddedUsers.png |
| F-03 | 🔴 High | Path traversal | Files and directories possibly accessable for attackers | ZAP report flag |
| F-05 | 🟡 Low | Weak password policy | Accepts weak passwords and no checks done to how long the password is or what it contains | In picture passwords like "123" and "ZAP" allowed: https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/AddedUsers.png |

---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred): https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/zap_report_round1.md.

---

**Instructions:**
1. Check lecture recordings
2. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---
