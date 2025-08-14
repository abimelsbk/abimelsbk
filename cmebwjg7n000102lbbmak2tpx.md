---
title: "CVE-2025-51092: SQL Injection Vulnerability"
seoTitle: "CVE-2025-51092: SQL Injection by Abimel S B kulumala"
seoDescription: "CVE-2025-51092: SQL Injection Vulnerability in DataBase.php logIn() and signUp() Functions"
datePublished: Thu Aug 14 2025 21:19:05 GMT+0000 (Coordinated Universal Time)
cuid: cmebwjg7n000102lbbmak2tpx
slug: cve-2025-51092-sql-injection-vulnerability
tags: vulnerability

---

## **CVE-2025-51092: SQL Injection Vulnerability in DataBase.php** `logIn()` and `signUp()` Functions

**CVE ID:** CVE-2025-51092  
**Severity:** High  
**Date Published:** 2025-08-14  
**Reported By:** Abimel S B Kulumala  
**Vendor Status:** Notified / Pending Patch

---

### **Summary**

A SQL Injection vulnerability has been identified in the `DataBase.php` file of the project LogIn-SignUp hosted at [GitHub](https://github.com/VishnuSivadasVS/LogIn-SignUp) affecting the `logIn()` and `signUp()` functions.  
This flaw allows unauthenticated remote attackers to manipulate SQL queries, leading to unauthorized data access or modification.

### **Affected Component**

* **File:** `DataBase.php`
    
* **Functions:** `logIn()` and `signUp()`
    
* **Vulnerability Type:** SQL Injection (CWE-89)
    

### **Vulnerability Details**

The `logIn()` and `signUp()` functions construct SQL queries by directly concatenating user-controlled input into the query string without proper sanitization or parameterization.

**Example Vulnerable Code (logIn):**

```bash
public function logIn($table, $username, $password) {
    $sql = "SELECT * FROM " . $table . " WHERE username = '$username' AND password = '$password'";
    $result = mysqli_query($this->conn, $sql);
    return $result;
}
```

**Impact:**  
An attacker can inject malicious SQL payloads through `$username` or `$password` fields, bypass authentication, extract sensitive data, or modify database content.

### **Proof of Concept (PoC)**

**Login bypass example:**

```bash
Username: admin' --
Password: anything
```

This payload comments out the password check, allowing an attacker to log in as `admin` without knowing the password.

**Data exfiltration example:**

```bash
Username: ' UNION SELECT database(), version(), user() --
Password: anything
```

This payload retrieves the current database name, MySQL version, and database user.

### **Impact Assessment**

* **Confidentiality:** High – Attackers can read sensitive data.
    
* **Integrity:** High – Attackers can modify or delete data.
    
* **Availability:** Low – Less likely to cause downtime, but possible with destructive queries.
    
* **CVSS v3.1 Score:** 8.1 (High)
    

### **Remediation**

Developers should:

1. Use **prepared statements** with parameterized queries.
    
2. Validate and sanitize all user input.
    
3. Avoid dynamically constructing SQL queries using untrusted data.
    

**Example Fix (Prepared Statement in PHP/MySQLi):**

```bash
$stmt = $this->conn->prepare("SELECT * FROM users WHERE username = ? AND password = ?");
$stmt->bind_param("ss", $username, $password);
$stmt->execute();
$result = $stmt->get_result();
```

### **References**

* [OWASP SQL Injection Prevention](https://owasp.org/www-community/attacks/SQL_Injection)
    
* [MITRE CWE-89](https://cwe.mitre.org/data/definitions/89.html)
    
* CVE-2025-51092 - SQL Injection Vulnerability - [Abimel S B kulumala](https://gist.github.com/abimelsbk)
    

---

**Reporter:** Abimel S B Kulumala

.