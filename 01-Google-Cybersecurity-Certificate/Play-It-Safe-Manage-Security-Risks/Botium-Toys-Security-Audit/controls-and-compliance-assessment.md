
# Botium Toys Controls and Compliance Assessment

## 1. Assessment Methodology

The audit was conducted using the scope, goals, and risk assessment report provided in the Google Cybersecurity Professional Certificate exercise.

The assessment involved:

1. Reviewing the organization's assets and existing security practices.
2. Identifying implemented and missing security controls.
3. Evaluating compliance-related practices.
4. Documenting security gaps.
5. Prioritizing recommendations based on potential risk.

## 2. Security Controls Assessment

| Security control | Status | Findings |
|---|---|---|
| Least privilege | No | Employees have excessive access to sensitive information. |
| Disaster recovery plans | No | No disaster recovery plan is established. |
| Password policies | Yes | A policy exists, but requirements are weak. |
| Separation of duties | No | Responsibilities and access permissions are not adequately separated. |
| Firewall | Yes | A firewall filters traffic using defined security rules. |
| Intrusion detection system (IDS) | No | No IDS is installed. |
| Backups | No | Critical data is not backed up. |
| Antivirus software | Yes | Antivirus software is installed and regularly monitored. |
| Legacy system monitoring | Yes | Manual maintenance exists but lacks a regular schedule. |
| Encryption | No | Sensitive payment card information is not encrypted. |
| Password management system | No | No centralized password management system exists. |
| Physical locks | Yes | Physical facilities have adequate locks. |
| CCTV surveillance | Yes | Surveillance systems are installed and maintained. |
| Fire detection and prevention | Yes | Fire safety systems are operational. |

**Summary:** 7 controls present, 7 controls missing.

A control marked "Yes" indicates its presence, not necessarily its effectiveness.

## 3. Compliance Assessment

### 3.1 PCI DSS

| Best practice | Status |
|---|---|
| Restrict cardholder data access to authorized users | No |
| Secure payment card data processing and storage | No |
| Implement encryption for payment card data | No |
| Adopt secure password management practices | No |

**Result: 0/4**

The organization lacks several essential safeguards for protecting payment card information.

### 3.2 GDPR

| Best practice | Status |
|---|---|
| Protect EU customers' personal information | No |
| Maintain a breach notification plan | Yes |
| Classify and inventory sensitive data | No |
| Establish and enforce privacy policies and procedures | Yes |

**Result: 2/4**

Privacy policies and a notification plan exist, but significant data protection weaknesses remain.

### 3.3 SOC 1 / SOC 2

| Best practice | Status |
|---|---|
| Establish appropriate user access policies | No |
| Maintain confidentiality of sensitive information | No |
| Ensure data integrity | Yes |
| Ensure data availability | Yes |

**Result: 2/4**

The organization has implemented data integrity and availability controls but needs stronger access management and confidentiality safeguards.

## 4. Key Security Findings

### Finding 1 – Excessive Access Permissions

**Priority: Critical**

Employees may access sensitive customer information without appropriate restrictions.

**Recommendation:**
Implement role-based access control (RBAC), least privilege, and separation of duties. Review user permissions periodically.

### Finding 2 – Missing Data Encryption

**Priority: Critical**

Payment card information is not adequately protected through encryption.

**Recommendation:**
Implement encryption for sensitive data at rest and in transit, and review payment data handling practices.

### Finding 3 – Missing Backup and Recovery Capabilities

**Priority: Critical**

The organization lacks critical data backups and a disaster recovery plan.

**Recommendation:**
Establish automated backups, secure backup storage, documented recovery procedures, and periodic restoration testing.

### Finding 4 – Weak Authentication Controls

**Priority: High**

Password requirements are insufficient, and centralized password management is unavailable.

**Recommendation:**
Strengthen password requirements, introduce centralized password management, and improve authentication governance.

### Finding 5 – Limited Threat Detection

**Priority: High**

No intrusion detection system is currently installed.

**Recommendation:**
Deploy an IDS, establish security monitoring procedures, and define incident escalation workflows.

### Finding 6 – Incomplete Asset Management

**Priority: High**

Asset identification and classification are incomplete, and legacy systems are not maintained according to a regular schedule.

**Recommendation:**
Maintain an asset inventory, classify sensitive information, and document scheduled legacy-system maintenance procedures.

## 5. Recommended Remediation Priorities

| Priority | Recommended action |
|---|---|
| Critical | Restrict access to customer and payment data |
| Critical | Encrypt sensitive information |
| Critical | Implement backups and disaster recovery |
| High | Strengthen password management |
| High | Deploy intrusion detection capabilities |
| High | Improve asset inventory and legacy-system maintenance |
| Ongoing | Review security controls and compliance practices |

## 6. Conclusion

The audit identified significant weaknesses in Botium Toys' security posture, particularly in access management, data confidentiality, and business continuity.

Although several preventive and physical security controls are present, additional safeguards are required to reduce exposure to unauthorized access, data loss, and operational disruption.

The recommended remediation measures provide a prioritized approach to improving the organization's overall security posture.

---
