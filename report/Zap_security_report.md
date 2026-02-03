# OWASP ZAP Security Assessment Report

## Target
https://pwning.owasp-juice.shop

---

## 1. Missing Anti-CSRF Tokens
- **Risk Level:** Medium
- **Description:** Forms lack CSRF protection, allowing attackers to perform unauthorized actions.
- **Impact:** Account takeover, unauthorized requests.
- **Mitigation:** Implement CSRF tokens for all state-changing requests.

---

## 2. Content Security Policy (CSP) Not Set
- **Risk Level:** Medium
- **Description:** No CSP header detected.
- **Impact:** Increased XSS risk.
- **Mitigation:** Add strict CSP headers.

---

## 3. X-Frame-Options Header Missing
- **Risk Level:** Low
- **Description:** Application can be embedded in iframes.
- **Impact:** Clickjacking attacks.
- **Mitigation:** Set `X-Frame-Options: DENY`.

---

## Conclusion
The application contains multiple security misconfigurations. While the application is intentionally vulnerable, the findings reflect common real-world security issues.

