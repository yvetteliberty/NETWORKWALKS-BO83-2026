# Black-Box Web Application Penetration Test — Mediroza Hospital
This project documents an authorised black-box security assessment of the Mediroza Hospital web application. This is part of Networkwalks  Week 4 Penetration testing Project. The assessement involves  a controlled of Back box penetration test.It required more than identifying possible vulnerabilities: Each milestone had to be demonstrated through actual access, retrieval, recovery and evidence-backed reporting.
The assessment developed into a chained compromise involving exposed application structure, authentication weaknesses, weak document protection and publicly accessible legacy data.

# Project Overview.
- Target : https://medirozahospital.com
- Assessment Type : Black-box Penetration Testing
- Duration : 5 Days
- Scope : Web  Application Assessment.

## The test was divided into Four Milestones.
| Milestone | Objective | Status |
|---|---|---|
| **M1** | Identify and retrieve three confidential patient PDF reports from the authorised lab environment | ✅ Complete |
| **M2** | Recover the passwords protecting all three retrieved PDF reports and verify access | ✅ Complete |
| **M3** | Identify and document critical data exposure on the client server | ✅ Complete |
| **M4** | Produce a detailed, evidence-backed penetration testing report | ✅ Complete |
# Objectives
 The assessment objectives was to:
- Conduct reconnaissance against the target.
- Identify exposed application entry points.
- Analyse authentication mechanisms.
- Test application input handling.
- Identify and validate security vulnerabilities.
- Demonstrate the impact of confirmed vulnerabilities.
- Document findings and provide remediation recommendations

# Methodology
The assessment followed a black-box penetration-testing approach:
-	Reconnaissance
- Identification of exposed entry points
- Analysis of authentication mechanisms
-	Input validation testing
- Controlled exploitation of identified vulnerabilities
- Evidence collection
-	Risk assessment
-	Remediation recommendations
# Tools
Tools used during the assessment included:
-	Burp Suite
- cURL
- Nmap/reconnaissance tools
-  QL Injection testing techniques
-	Other authorized web-application testing tools
  
# Findings and Proof of Exploitation
 Finding 1 : Public directory listing and exposed database backup URL:/Old/
Description: 
Public directory listing occurs when sensitive or confidential information is unintentionally made accessible through publicly available directories, web pages, file listings, or online databases. This may expose information such as employee details, shareholder records, contact information, internal documents, system information, or other organizational data to unauthorized individuals.
Exposed File: mediroza_db_backup_2019 sql Unauthorized access to database information. The file was accessible without authentication.
Impact: The exposed potentially allows an unauthorized visitor to obtain confidential organizations data.
 # Proof of concept: 
 <img width="570" height="157" alt="image" src="https://github.com/user-attachments/assets/6fec3113-d92d-45a8-b731-c70f3bab7f3e" />
 <img width="1110" height="302" alt="image" src="https://github.com/user-attachments/assets/12c20f1a-c791-47a8-9f5a-c46031bda165" />

Finding  2:  Sensitive Information exposure Shareholders Records.
Description:
Sensitive information exposure involving shareholders’ records occurs when confidential shareholder data is accessed, disclosed, shared, or made available to unauthorized individuals or parties. Such records may contain personal and financial information, including shareholders’ names, contact details, shareholdings, ownership percentages, identification information, dividend details, or other confidential corporate records.

Evidence: Public directory listing permitted retrieval of an internal, database backup which contains   staff table, shareholder information including salary data 

<img width="882" height="127" alt="image" src="https://github.com/user-attachments/assets/1ec48361-dfb6-43ca-8e32-8ff7617b3341" />
Impact: An unauthorized party who can retrieve the exposed database backup could access confidential shareholder compensation information

Finding 3: SQL Injection in Patient Login Portal
Description
A SQL Injection vulnerability was identified in the patient login functionality.
The application accepts user-controlled input through the login form. Testing demonstrated that specially crafted input could alter the application's interaction with the underlying database.
The successful test indicates that the application does not adequately validate or safely process input before using it in a database query.
Impact
- An attacker could potentially use this vulnerability to:
- Bypass authentication controls.
-	Access restricted patient areas.
-	Retrieve sensitive information from the database.
-	Access confidential patient records.
-	Potentially modify or manipulate database information, depending on the application's database privileges.
Because the affected system belongs to a healthcare organization, unauthorized disclosure of patient information could have serious confidentiality and privacy implications.

<img width="975" height="405" alt="image" src="https://github.com/user-attachments/assets/07b1e846-e588-4af2-a61b-2218386f4dec" />

