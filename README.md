# RobotProject MAXX
## 🔒 Security

The MAXX Byte Robot Food Delivery Service uses a layered security approach to protect the ordering application, robot fleet communication, and user data.

### Authentication & Access Control
- **JWT-based authentication** via Spring Security on all protected endpoints
- **Role-based access control (RBAC)** separating customer, staff, and admin permissions
- Key protected routes include `/profile`, `/orders`, and `/cart` — all require a valid JWT token

### Network & Robot Security
- Secure communication architecture defined for the robot ↔ server ↔ customer app pipeline
- Firewall and port rules documented for deployment
- HTTPS and secure headers enforced via deployment security checklist

### Rate Limiting
- Global rate limiting caps total system requests per time window to prevent any single user, robot, or attacker from overwhelming the service
- Per-IP and per-API-key thresholds enforced; offenders receive `429 Too Many Requests` with a `Retry-After` header

### Security Testing
The security team performs ongoing testing using the following open-source tools:

| Tool | Purpose |
|------|---------|
| OWASP ZAP | Automated vulnerability scanning (XSS, SQLi, etc.) |
| Burp Suite Community | Manual request interception and auth testing |
| Postman | API endpoint and authentication flow testing |
| Wireshark | Network traffic capture and analysis |
| Nmap | Network discovery and port scanning |


[Security Team Guide - Robot Project.docx](https://github.com/user-attachments/files/25909278/Security.Team.Guide.-.Robot.Project.docx)
