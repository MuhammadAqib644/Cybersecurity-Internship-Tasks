
# 🔐 OWASP Juice Shop Security Enhancement Project

### 👨‍💻 Author: Muhammad Aqib  
### 🖥️ Environment: Kali Linux VM | OWASP Juice Shop | Node.js | MongoDB  
### 📁 Project Scope: Comprehensive Web App Security Hardening & Testing

---

## 📌 Overview

This project focuses on identifying, exploiting, and securing vulnerabilities in the OWASP Juice Shop application. The tasks span from ethical hacking to secure deployment and cover best practices in real-world application security.

---

## ✅ Completed Security Tasks

### 1. 🛡️ Intrusion Detection & Monitoring

- **Tools Used:** Fail2Ban
- **Objective:** Monitor and block brute-force login attempts.
- **Setup:**
  - Custom filter and jail created for Juice Shop.
  - Logs monitored from `/var/log/juiceshop.log`.
- **Outcome:** IPs with repeated failed login attempts are automatically banned.

### 2. 🔐 API Security Hardening

- **Goal:** Prevent abuse through rate limiting and secure access.
- **Steps:**
  - Added express-rate-limit in the app.
  - Restricted access to sensitive routes.
  - Implemented proper status codes and error handling.

### 3. 🧠 Security Headers & CSP Implementation

- **Tool:** Helmet.js
- **Enhancements:**
  - Set `Content-Security-Policy`, `Strict-Transport-Security`, `X-Content-Type-Options`, and `X-Frame-Options` headers.
  - Verified via browser dev tools and online header analyzers.

### 4. 🧪 Ethical Hacking Basics

- **Tools:** nmap, nikto, ping, whois
- **Practices:**
  - Performed service detection & OS fingerprinting.
  - Enumerated open ports on Juice Shop instance.

### 5. 💉 SQL Injection & Exploitation

- **Tool:** sqlmap, Burp Suite
- **Findings:**
  - Vulnerable query endpoint discovered.
  - SQLi confirmed with payload `' OR 1=1 --`.
- **Fix:** Used prepared statements in backend.

### 6. 🔁 Cross-Site Request Forgery (CSRF) Protection

- **Tool:** csurf middleware
- **Steps:**
  - Simulated CSRF attack with PoC HTML.
  - Integrated CSRF tokens in requests.
  - Verified fix using Burp Suite.

### 7. 📋 Security Audits & Compliance

- **Tools:** Lynis, Owasp Zap
- **Audit Output:**
  - Executed `lynis audit system`.
  - Extracted warnings/suggestions.
  - Addressed critical misconfigurations.

### 8. 🚀 Secure Deployment Practices

- **Nginx Reverse Proxy:**
  - Added headers for HSTS, CSP, and XSS protection.
- **Dependencies:**
  - Used `npm audit fix` and manual patches.
- **Other Configs:**
  - Disabled X-Powered-By.
  - Enforced HTTPS and strong ciphers.

### 9. 🧨 Final Penetration Testing

- **Tools Used:** Burp Suite, OWASP ZAP
- **Activities:**
  - Performed active and passive scans.
  - Validated protections for previously exploited endpoints.
  - Confirmed security patches were effective.

---

## 📷 Screenshots

<img width="684" height="371" alt="image" src="https://github.com/user-attachments/assets/d221b05d-2b89-4355-8ffc-1f8719abc0de" />

<img width="940" height="436" alt="image" src="https://github.com/user-attachments/assets/64a5382c-e8dc-4cbf-bd83-c74f7547fd7d" />

<img width="940" height="507" alt="image" src="https://github.com/user-attachments/assets/2047b17e-f470-4f2a-b878-b2ba992721a7" />

<img width="940" height="436" alt="image" src="https://github.com/user-attachments/assets/c97746ba-78b0-444b-bae6-c976e070aef6" />


---

## 📁 How to Run

1. Clone Juice Shop:
   ```bash
   git clone https://github.com/juice-shop/juice-shop
   cd juice-shop
   npm install
   npm start
   ```

2. Run Security Features:
   - Ensure custom logs are written for Fail2Ban.
   - Launch app behind Nginx reverse proxy.

3. Validate:
   - Run Burp Suite to inspect headers, responses.
   - Test CSRF tokens, SQLi inputs, rate limits.

---

## 📘 References

- OWASP Juice Shop Docs: https://owasp.org/www-project-juice-shop/
- OWASP Top 10: https://owasp.org/www-project-top-ten/

---

## 🏁 Conclusion

Through the completion of 9 critical security tasks, I successfully demonstrated end-to-end protection of a web application. This involved proactive threat detection, defensive coding, and secure deployment. The result is a hardened Juice Shop instance ready to resist common web threats.

---

> *This project reflects practical implementation of web security standards. Ideal for developers, pentesters, and students exploring secure app design.*
