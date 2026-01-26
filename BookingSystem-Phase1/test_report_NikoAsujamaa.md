# 1️⃣ Introduction

**Tester(s):**  
- Name: Niko Asujamaa

**Purpose:**  
- The purpose of this test is to find vulnerabilities in the booking system's registration page.

**Scope:**  
- Tested components: Registration page
- Exclusions: Log in page
- Test approach: Gray-box 

**Test environment & dates:**  
- Start:  23.1.2026 12.47
- End:  23.1.2026 13.02
- Test environment details (OS, runtime, DB, browsers): Windows 11 Pro, Docker desktop, PostgreSQL, Opera GX(Google)

**Assumptions & constraints:**  
- Limited scope to only testing the registration page of the system.

---

# 2️⃣ Executive Summary

Penetration testing done to the registration page of the booking system with ZAP. The testing showed a lot of faults in the page, such as vulnerabilities to SQL injections, path traversal and the site lacks security in how it stores passwords and what passwords are allowed.

**Overall risk level:** High

**Top 5 immediate actions:**  
1.  Hashing/encrypting passwords in database.
2.  Fix issue with path traversal.
3.  Fix logs exposing username information.
4.  Fix vulnerability to SQL injections.
5.  Fix weak password policy by validating user input based on the length of the password and by forcing it to include special characters and numbers.

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings 


| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration page | Input field allows OR '1'='1` -- and AND '1'='1` -- injections | ZAP report flag, found in the ZAP report |
| F-02 | 🔴 High | Passwords in database exposed | Passwords are not hashed/encrypted in the database | Passwords clearly visible: https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/AddedUsers.png |
| F-03 | 🔴 High | Path traversal | Files and directories possibly accessable for attackers | ZAP report flag, found in the ZAP report |
| F-04 | 🟠 Medium | Content Security Policy header not set | CSP headers which help to mitigate and detect certain types of attacks are not set | ZAP report flag, found in the ZAP report |
| F-05 | 🟡 Low | Weak password policy | Accepts weak passwords and no checks done to how long the password is or what it contains | In picture passwords like "123" and "ZAP" allowed: https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/AddedUsers.png |


# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
-  https://github.com/Timanttiso/CyberSecurityCourse/blob/main/BookingSystem-Phase1/zap_report_round1.md.


