# FUTURE_CS_01
Vulnerability Assessment Report for a Live Website

# Overview:
This project is a **read-only Vulnerability Assessment** conducted as part of my Cyber Security Internship at Future Interns.

The target application was the **IBM Altoro Mutual demo banking website**:  
https://demo.testfire.net/

The assessment followed a **black-box approach**, focusing on identifying security weaknesses without exploiting them.

# Objectives
- Perform reconnaissance and network analysis  
- Identify open ports and services  
- Detect web application vulnerabilities  
- Classify risks based on severity  
- Provide remediation recommendations  


# Tools Used
- **Kali Linux** – Testing environment  
- **Nmap** – Port scanning & service detection  
- **OWASP ZAP** – Vulnerability scanning (Spider + Active Scan)  
- **Browser DevTools** – Header & cookie analysis  


# Methodology

### 1. Reconnaissance
- Checked connectivity using ping  
- Performed DNS lookup (nslookup)  
- Gathered domain details using WHOIS  

### 2. Network Scanning
- Identified open ports (80, 443, 8080) using Nmap  
- Detected exposed services and server information  

### 3. Web Application Scanning
- Crawled the application using OWASP ZAP  
- Performed passive and active scans  
- Detected vulnerabilities like SQL Injection and XSS  

### 4. Manual Analysis
- Inspected HTTP headers and cookies  
- Checked for information disclosure  


## Key Findings

A total of **19 security issues** were identified:

- High: 2  
- Medium: 10  
- Low: 7  
- Informational: 5  

# Critical Vulnerabilities
- **SQL Injection (4 instances)**  
  → Risk of database access and manipulation  

- **Reflected XSS (2 instances)**  
  → Execution of malicious scripts in user browsers  

# Other Issues
- Missing security headers (CSP, HSTS, X-Frame-Options)  
- No CSRF protection  
- Weak cookie configurations  
- Server version disclosure  
- Mixed content issues  

# Risk Assessment
> **Overall Risk Level: HIGH**
These vulnerabilities could lead to:
- Data breaches  
- Account compromise  
- Unauthorized transactions  

# Remediation Summary
- Use **parameterized queries** to prevent SQL Injection  
- Implement **output encoding** to prevent XSS  
- Add security headers (CSP, HSTS, X-Frame-Options, X-Content-Type-Options)  
- Secure cookies with **HttpOnly, Secure, SameSite**  
- Implement **CSRF protection**  
- Remove sensitive server information  

# Key Learnings
- Learned structured vulnerability assessment methodology  
- Gained hands-on experience with Nmap & OWASP ZAP  
- Understood real-world impact of vulnerabilities in banking systems  
- Improved ability to explain technical risks clearly  

# Conclusion
This project helped me understand that cybersecurity is not just about finding vulnerabilities, but about **analyzing risk, prioritizing fixes, and communicating effectively**.

