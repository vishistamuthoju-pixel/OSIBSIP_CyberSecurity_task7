# OSIBSIP_CyberSecurity_task7
Performed web server vulnerability assessment using Nikto to identify security misconfigurations such as missing HTTP security headers and analyzed risks with mitigation recommendations.
# 🔍 Task 7 – Vulnerability Scanning with Nikto

## 📌 Internship Domain
Cyber Security – OIBSIP Internship

---

## 🎯 Objective

The objective of this task is to perform a vulnerability assessment on a web server using the Nikto web vulnerability scanner and identify potential security misconfigurations and weaknesses.

---

## 🛠 Tools Used

- Kali Linux
- Nikto v2.5.0
- Target Web Server: http://vulnweb.com
- Terminal (Bash Shell)

---

## 🔎 Steps Performed

1. Opened Kali Linux environment.
2. Verified Nikto installation.
3. Selected a test web server (vulnweb.com).
4. Executed the vulnerability scan using:

   nikto -h http://vulnweb.com -o nikto_scan_results.txt

5. Waited for scan completion.
6. Analyzed the output file to identify vulnerabilities.
7. Documented findings and mitigation recommendations.

---

## 🚨 Vulnerabilities Identified

### 1️⃣ Missing X-Frame-Options Header
- Risk: Clickjacking attacks
- Severity: Medium
- Description: The server does not prevent the website from being loaded inside an iframe, which may allow attackers to trick users into clicking hidden elements.

### 2️⃣ Missing X-Content-Type-Options Header
- Risk: MIME-type sniffing attacks
- Severity: Medium
- Description: The browser may interpret files as a different content type, which could allow execution of malicious scripts.

---

## 📊 Risk Analysis

The identified vulnerabilities are related to missing security headers. While not critical, they expose the web server to potential client-side attacks such as clickjacking and MIME-type sniffing. These misconfigurations should be addressed to improve the security posture of the application.

---

## 🛡 Recommendations

- Enable X-Frame-Options header (SAMEORIGIN or DENY).
- Enable X-Content-Type-Options header (nosniff).
- Regularly update server software.
- Perform periodic vulnerability assessments.
- Implement additional security headers such as Content-Security-Policy (CSP).

---

## 📁 Project Deliverables

- nikto_scan_results.txt
- README.md
- Demo Video (3–10 minutes)

---

## 🎥 Demo Video Explanation

In the demonstration video:
- Nikto scan execution is shown.
- Vulnerabilities identified are explained.
- Risk analysis and recommendations are discussed.
- GitHub repository structure is presented.

---

## 📈 Outcome

This task successfully demonstrates practical knowledge of web vulnerability scanning using Nikto. The assessment identified security misconfigurations and provided actionable recommendations to enhance web application security.

---

