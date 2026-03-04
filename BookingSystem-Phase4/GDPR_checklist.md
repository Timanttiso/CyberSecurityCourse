# GDPR Compliance Checklist – Web-based Booking System

| **Result** | **Personal data mapping and minimization** | **Notes** |
| :----: | :--- |:--- |
| &nbsp;❌&nbsp; | Have all personal data collected and processed in the system been<br> identified? (e.g., name, email, age, username) | The IP address of the user is collected in the login logs, which is not specified anywhere. |
| &nbsp;✅&nbsp; | Have you ensured that only necessary personal data is collected (data minimization)? | From what I can tell only necessary data is collected. |
| &nbsp;✅&nbsp; | Is user age recorded to verify that the booker is over 15 years old? | The user age itself is not stored anywhere, but the age can be calculated from the birthday provided. User accounts under 15 are not also allowed to be made. |

---

| **Result** | **User registration and management** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅&nbsp; | Does the registration form (page) include GDPR-compliant consent for processing<br> personal data (e.g., acceptance of the privacy policy)?| The check box to accept the terms would qualify as consent. |
| &nbsp;❌&nbsp; | Can users view, edit, and delete their own personal data via their account? | Account info can be viewed but not deleted or edited. |
| &nbsp;⚠️&nbsp; | Is there a mechanism for the administrator to delete a reserver in<br> accordance with the "right to be forgotten"? | There is no clear admin panel accessable through the UI nor anything of the like that you can use to delete users, but technically speaking users and other information could be deleted straight from the database but that would be hard and time consuming |
| &nbsp;✅&nbsp; | Is underage registration (under 15 years) and booking functionality restricted? | People under 15 are not able to register |

---

| **Result** | **Booking visibility** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅&nbsp; | Are bookings visible to non-logged-in users only at the resource level<br> (without any personal data)? | This is fine. Account info is not visible to not logged in users. |
| &nbsp;⚠️&nbsp; | Is it ensured that names, emails, or other personal data of bookers are not exposed<br> publicly or to unauthorized users? | No information is visible to not logged in users, but other reservers can see the emails of other reservers, which could be problematic, since anyone can sign up. Best practice would probably be that the admin can only see the emails of the users. |

--- 

| **Result** | **Access control and authorization** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Have you ensured that only administrators can add, modify, and delete<br> resources and bookings? | |
| &nbsp;✅/❌/⚠️&nbsp; | Is the system using role-based access control (e.g., reserver vs. administrator)? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are administrator privileges limited to ensure GDPR compliance (e.g., administrators<br> cannot use data for unauthorized purposes)? | |

---

| **Result** | **Privacy by Design Principles** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Has Privacy by Default been implemented (e.g., collecting the minimum data by default)? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are logs implemented without unnecessarily storing personal data? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are forms and system components designed with data protection in mind<br> (e.g., secured login, minimal fields)? | |

---

| **Result** | **Data security** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Are CSRF, XSS, and SQL injection protections implemented? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are passwords securely hashed using a strong algorithm (e.g., bcrypt, Argon2)? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are data backup and recovery processes GDPR-compliant? | |
| &nbsp;✅/❌/⚠️&nbsp; | Is personal data stored in data centers located within the EU? | |

---

| **Result** | **Data anonymization and pseudonymization** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Is personal data anonymized where possible? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are pseudonymization techniques used to protect data while maintaining its utility? | |

---

| **Result** | **Data subject rights** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Can users download or request all personal data related to them (data access request)? | |
| &nbsp;✅/❌/⚠️&nbsp; | Is there an interface or process for users to request the deletion of their personal data? | |
| &nbsp;✅/❌/⚠️&nbsp; | Can users withdraw their consent for data processing? | |

---

| **Result** | **Documentation and communication** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;✅/❌/⚠️&nbsp; | Is there a privacy policy available to users during registration and easily accessible? | |
| &nbsp;✅/❌/⚠️&nbsp; | Are administrators and developers provided with documented data protection practices <br>and processing activities? | |
| &nbsp;✅/❌/⚠️&nbsp; | Is there a documented data breach response process (e.g., how to notify authorities <br>and users of a breach)? | |

---

**Symbols used:**  
✅ Pass (a note can be added)  
❌ Fail (a note can be added)  
⚠️ Attention (a note can be added)
