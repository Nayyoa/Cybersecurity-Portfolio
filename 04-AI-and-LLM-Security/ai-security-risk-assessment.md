
# AI Security Risk Assessment

## Enterprise GenAI & LLM Security

**Organization:** E2IP Technologies  
**Project Type:** Cybersecurity Engineering Internship  
**Focus:** AI Security | Risk Assessment | Threat Modeling | Risk Mitigation

---

## 1. Project Overview

This project focused on identifying, analyzing, and documenting cybersecurity risks associated with the use of Generative AI and Large Language Models in an enterprise environment.

The assessment examined security threats introduced by AI-powered applications, particularly risks related to sensitive data exposure, unauthorized AI usage, and vulnerabilities affecting LLM-based systems.

The objective was to establish a structured understanding of AI-related security risks and identify appropriate technical and organizational security measures.

The assessment was based on recognized AI security frameworks, including:

- OWASP Top 10 for LLM Applications (2025)
- NIST AI Risk Management Framework (AI RMF)

---

## 2. Assessment Objectives

The security assessment focused on five objectives:

1. Identify cybersecurity risks associated with enterprise GenAI adoption.
2. Analyze threats and vulnerabilities affecting LLM applications and AI usage.
3. Evaluate potential impacts on confidentiality, integrity, and availability.
4. Map identified risks using recognized AI security frameworks.
5. Recommend security measures to reduce exposure to AI-related threats.

---

## 3. Assessment Methodology

The assessment followed a structured risk analysis approach.

### Phase 1: Identification of AI Security Risks

Identified security threats associated with the use of GenAI and LLM-based applications.

Particular attention was given to:

- Sensitive information disclosure
- Prompt injection attacks
- Unauthorized AI application usage
- Insecure handling of AI-generated content
- Exposure of credentials and API keys
- Inadequate access controls
- Security and privacy risks related to external AI services

### Phase 2: Risk Analysis

Analyzed identified risks according to their potential impact on enterprise information systems and sensitive information.

The analysis considered:

- Threat scenarios
- Potential vulnerabilities
- Affected information assets
- Business and security impacts
- Existing or recommended security controls

### Phase 3: Risk Mapping

Organized identified risks into a structured mapping aligned with recognized AI security frameworks.

This approach helped connect technical AI threats with broader enterprise security and governance concerns.

### Phase 4: Security Recommendations

Identified technical and organizational measures to reduce AI-related security exposure.

Recommendations addressed:

- Data protection
- Security monitoring
- AI usage governance
- Access control
- Security awareness
- AI security policy enforcement

---

## 4. OWASP Top 10 for LLM Applications

The OWASP Top 10 for LLM Applications (2025) provided a reference for identifying and categorizing security risks affecting LLM-based systems.

| ID | Risk Category |
|---|---|
| LLM01 | Prompt Injection |
| LLM02 | Sensitive Information Disclosure |
| LLM03 | Supply Chain |
| LLM04 | Data and Model Poisoning |
| LLM05 | Improper Output Handling |
| LLM06 | Excessive Agency |
| LLM07 | System Prompt Leakage |
| LLM08 | Vector and Embedding Weaknesses |
| LLM09 | Misinformation |
| LLM10 | Unbounded Consumption |

### Key Risk Areas

**Prompt Injection**

Malicious or untrusted instructions may influence an LLM's behavior and potentially bypass intended application restrictions.

**Sensitive Information Disclosure**

Employees may unintentionally expose confidential business information, credentials, or personal data when interacting with external AI services.

**Improper Output Handling**

AI-generated outputs may introduce security risks when incorporated into downstream applications without appropriate validation.

**Excessive Agency**

LLM-based applications with excessive permissions or access to external tools may perform unintended actions.

**Supply Chain Risks**

Dependencies on external models, AI services, and third-party components introduce additional security and trust considerations.

---

## 5. NIST AI Risk Management Framework

The NIST AI RMF provided a governance-oriented approach for understanding and managing AI-related risks.

The assessment considered the framework's four core functions.

### GOVERN

Establish organizational policies, responsibilities, and processes for managing AI risks.

### MAP

Identify the context, stakeholders, and potential impacts associated with AI systems and their usage.

### MEASURE

Assess AI-related risks and evaluate the effectiveness of relevant security controls.

### MANAGE

Prioritize identified risks and define appropriate mitigation and monitoring measures.

### Generative AI Profile

The NIST AI RMF Generative AI Profile provided additional guidance for addressing risks specific to generative AI technologies.

It supported the identification of security, privacy, and governance concerns associated with enterprise GenAI adoption.

---

## 6. Enterprise AI Security Risk Mapping

The assessment addressed several categories of AI-related security risks.

| Risk Area | Security Concern | Relevant Mitigation |
|---|---|---|
| Sensitive Data Exposure | Confidential information submitted to AI services | DLP controls and data handling policies |
| Prompt Injection | Manipulation of LLM instructions | AI guardrails and input/output controls |
| Shadow AI | Use of unauthorized AI applications | Application visibility and usage governance |
| Credential Exposure | API keys or passwords disclosed through prompts | Sensitive information detection |
| Insecure AI Outputs | Unsafe or unreliable generated content | Output validation and security review |
| Access Control | Excessive permissions granted to AI applications | Least privilege and access management |
| Third-Party AI Services | Security and privacy risks associated with external providers | Vendor risk assessment and governance |

These categories were used to structure the analysis of enterprise AI security exposure and relevant mitigation approaches.

---

## 7. Data Protection & Sensitive Information

A major focus of the assessment was the protection of sensitive information when interacting with Generative AI services.

### Identified Concerns

- Disclosure of confidential company information
- Exposure of credentials and API keys
- Submission of sensitive customer information
- Unauthorized transfer of business data
- Inadequate visibility into external AI usage

### Security Measures

Relevant security measures included:

- Data Loss Prevention (DLP)
- Sensitive information detection
- AI usage monitoring
- Custom security policies
- Access restrictions
- Employee security awareness

These risk areas informed the subsequent evaluation of enterprise AI security solutions.

---

## 8. Connection to Security Solutions Evaluation

The risk assessment provided a foundation for evaluating technical controls through Netskope One AI Security and CrowdStrike.

The technical evaluation focused on the effectiveness of security mechanisms addressing identified AI risks.

### Evaluation Areas

- Detection of sensitive information
- Enforcement of security policies
- Custom policy configuration
- AI security monitoring
- Identification of unauthorized AI usage
- Detection accuracy
- False positive and false negative analysis

The results of these evaluations supported the assessment of available security controls and their limitations.

**Related documentation:**

[Netskope vs. CrowdStrike Security Evaluation](netskope-vs-crowdstrike-security-evaluation.md)

---

## 9. Security Recommendations

The assessment supported the development of recommendations across technical and organizational security areas.

### Technical Controls

- Implement AI-aware data protection controls.
- Monitor enterprise GenAI usage.
- Apply appropriate access restrictions.
- Configure security policies to detect sensitive information.
- Evaluate detection effectiveness through controlled testing.

### Organizational Controls

- Establish acceptable use policies for AI tools.
- Define responsibilities for AI security governance.
- Develop procedures for AI-related security incidents.
- Provide employee awareness and guidance.
- Review AI security risks as technologies and usage patterns evolve.

These recommendations contributed to the AI governance and security awareness workstream.

**Related documentation:**

[AI Governance & Security Awareness](ai-governance-and-security-awareness.md)

---

## 10. Skills Demonstrated

### AI Security

- Generative AI Security Assessment
- LLM Threat Identification
- AI Security Risk Mapping
- Sensitive Data Protection
- AI Security Controls Evaluation

### Risk Management

- Cybersecurity Risk Identification
- Risk Analysis
- Security Recommendations
- Framework-Based Assessment

### Frameworks

- OWASP Top 10 for LLM Applications
- NIST AI Risk Management Framework
- NIST AI RMF Generative AI Profile

### Professional Skills

- Security Documentation
- Risk Communication
- Technical Analysis
- Security Reporting

---

## 11. Conclusion

This project demonstrated the importance of systematically assessing security risks associated with enterprise Generative AI adoption.

By combining recognized AI security frameworks with an enterprise-focused risk assessment methodology, the work established a foundation for evaluating technical security controls and developing AI governance recommendations.

The assessment also highlighted the need to address AI security through a combination of technical safeguards, organizational policies, and continuous risk management.

---

## Related Project Documentation

- [AI & LLM Security — Overview](README.md)
- [Netskope vs. CrowdStrike Security Evaluation](netskope-vs-crowdstrike-security-evaluation.md)
- [AI Governance & Security Awareness](ai-governance-and-security-awareness.md)

---

## Confidentiality Notice

This document presents a professional overview of the security assessment methodology and the categories of risks examined.

Company-specific risk registers, internal security findings, confidential information, and proprietary documentation are not disclosed.
