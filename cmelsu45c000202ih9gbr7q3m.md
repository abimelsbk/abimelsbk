---
title: "SQL Injection Vulnerability at LogIn-SignUp PHP Project"
datePublished: Thu Aug 21 2025 19:33:06 GMT+0000 (Coordinated Universal Time)
cuid: cmelsu45c000202ih9gbr7q3m
slug: sql-injection-vulnerability-at-login-signup-php-project
tags: sqlinjection

---

**Vulnerability Type** - SQL Injection

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

[https://en.wikipedia.org/wiki/SQL\_injection](https://en.wikipedia.org/wiki/SQL_injection)

**Vendor of Product**

Vendor Name: Vishnu Sivadas

Affected Product Code Base - [https://github.com/VishnuSivadasVS/LogIn-SignUp](https://github.com/VishnuSivadasVS/LogIn-SignUp) 1; LogIn-SignUp PHP Project (no versioning system, latest commit used at the time of testing) 1

**Reported by** - [Abimel S B kulumala](https://www.linkedin.com/in/abimelsbk/)