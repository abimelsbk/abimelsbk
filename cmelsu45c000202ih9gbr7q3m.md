---
title: "Abimel S B Kulumala secures CVE-2025-51092 recognition in NVD for uncovering critical SQL Injection vulnerability"
seoTitle: "Abimel S B Kulumala secures CVE-2025-51092"
seoDescription: "Abimel S B Kulumala secures CVE-2025-51092 recognition in NVD for uncovering critical SQL Injection vulnerability"
datePublished: Thu Aug 21 2025 19:33:06 GMT+0000 (Coordinated Universal Time)
cuid: cmelsu45c000202ih9gbr7q3m
slug: abimel-s-b-kulumala-secures-cve-2025-51092-recognition-in-nvd-for-uncovering-critical-sql-injection-vulnerability
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1756658092674/5c1d26ab-7767-4bad-a8a1-c1e4528c3fbe.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1756658071970/51ca9d4b-0eb2-4c12-ad87-d5b9e0999aba.jpeg
tags: sqlinjection

---

**Vulnerability Type** - SQL Injection

**CVE ID:** CVE-2025-51092

**Additional Information**

Suggested Mitigation: Replace string concatenated SQL with mysqli\_prepare() and bound parameters. Sanitize and whitelist table names if they must be dynamic. Replace prepareData() with robust input validation libraries or frameworks. Restrict direct access to database-related files in production.

**Affected Component**

DataBase.php ? logIn() function DataBase.php ? signUp() function DataBase.php ? Improper handling of $table variable (table injection) prepareData() function may be insufficient for full sanitization

**Attack Type-** Remote

**Impact Information Disclosure** - true

**Other CVE Impacts**

The SQL injection and table name injection vulnerabilities in the LogIn-SignUp project allow attackers to bypass authentication, extract sensitive user data (usernames, emails, hashed passwords), manipulate or delete database contents, and potentially escalate privileges. These flaws can lead to full compromise of the application's confidentiality, integrity, and availability, posing significant risks including account takeover, data exfiltration, and denial of service.

**Attack Vectors**

Remote unauthenticated attackers can exploit the login or signup POST endpoints by injecting SQL commands via form inputs (username, password, fullname, email) or tampering the $table parameter passed from external sources.

**Discoverer** - no

**Reference**

[https://nvd.nist.gov/vuln/detail/CVE-2025-51092](https://nvd.nist.gov/vuln/detail/CVE-2025-51092)

[https://www.cve.org/CVERecord?id=CVE-2025-51092](https://www.cve.org/CVERecord?id=CVE-2025-51092)

[https://vulners.com/cve/CVE-2025-51092](https://vulners.com/cve/CVE-2025-51092)

[https://gist.github.com/abimelsbk/0072479d644e245b762a58751a9df101](https://gist.github.com/abimelsbk/0072479d644e245b762a58751a9df101)

[https://www.cisa.gov/news-events/bulletins/sb25-237](https://www.cisa.gov/news-events/bulletins/sb25-237)

[https://en.wikipedia.org/wiki/SQL\_injection](https://en.wikipedia.org/wiki/SQL_injection)

**Vendor of Product**

Vendor Name: Vishnu Sivadas

Affected Product Code Base - [https://github.com/VishnuSivadasVS/LogIn-SignUp](https://github.com/VishnuSivadasVS/LogIn-SignUp) 1; LogIn-SignUp PHP Project (no versioning system, latest commit used at the time of testing) 1

**Reported by** - [Abimel S B kulumala](https://www.linkedin.com/in/abimelsbk/)

**CVE ID:** CVE-2025-51092

**About Abimel S B Kulumala:** Abimel S B Kulumala is a cybersecurity researcher with expertise in vulnerability discovery and secure application development. His contributions focus on improving web security by uncovering critical flaws and recommending effective remediation strategies. He is ranked 34 in the list of top 200 cybersecurity professionals Published by Favikon.