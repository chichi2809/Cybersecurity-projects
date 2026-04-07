# HealthBridge Solutions - Company Profile

**NIST Cybersecurity Framework Assessment**

**Document Version:** 1.0  
**Date:** January 2026  
**Classification:** Internal Use

---

## Executive Summary

HealthBridge Solutions is a healthcare technology company providing cloud-based Electronic Health Record (EHR) and patient portal solutions to medical practices across the United States.

**Company Overview:**
- **Founded:** 2015
- **Industry:** Healthcare Technology (B2B SaaS)  
- **Headquarters:** Miami, Florida
- **Employees:** 450
- **Annual Revenue:** $45 million
- **Customers:** 3,500 medical practices
- **Patient Records:** 1.2 million
- **Technology Platform:** AWS cloud-based

**Regulatory Requirements:**
- HIPAA (Health Insurance Portability and Accountability Act)
- HITECH Act
- PCI-DSS Level 4 (payment card data)
- SOC 2 compliance (customer requirement)
- State privacy laws

---

## Business Overview

### Mission
Empower small and medium-sized healthcare providers with affordable, secure, and user-friendly technology that improves patient care.

### Business Model
- Subscription-based SaaS platform
- Pricing: $500-$2,000 per month per practice
- Annual contracts
- Revenue growth: 25% year-over-year
- Customer retention: 92%

### Primary Product - HealthBridge EHR Platform
- Electronic Health Records management
- Patient portal (appointments, results, messaging)
- e-Prescribing integration
- Lab integration (HL7/FHIR standards)
- Billing and claims management
- Telehealth capabilities
- Mobile apps (iOS and Android)

### Target Customers
- Small medical practices (1-15 physicians)
- Medium practices (15-50 physicians)
- Specialties: Primary care, pediatrics, internal medicine
- Geographic: All 50 U.S. states

---

## Technology Environment

### Cloud Infrastructure - Amazon Web Services (AWS)
- **Primary Region:** US-East-1 (N. Virginia)
- **DR Region:** US-West-2 (Oregon)
- **Architecture:** Multi-tenant SaaS application
- **Uptime SLA:** 99.9%

### AWS Services Used
- **EC2** - Application servers
- **RDS** - PostgreSQL databases
- **S3** - Document/image storage
- **CloudFront** - Content delivery network
- **Route53** - DNS management
- **VPC** - Network isolation
- **CloudWatch** - Monitoring
- **IAM** - Access management
- **WAF** - Web application firewall

### Application Stack
- **Frontend:** React.js (web), React Native (mobile)
- **Backend:** Node.js, Express.js
- **API:** RESTful APIs
- **Primary Database:** PostgreSQL (patient data)
- **Analytics Database:** MongoDB (logs, audit trails)
- **Cache:** Redis
- **Message Queue:** RabbitMQ

### Data Volume
- 1.2 million patient records
- 50TB total data storage
- 10,000 API requests per minute (average)
- 200,000 daily active users

### Third-Party Integrations
**Critical Vendors:**
- **Stripe** - Payment processing
- **Twilio** - SMS notifications, telehealth
- **SendGrid** - Email delivery
- **Auth0** - Identity management
- **PagerDuty** - Incident alerting
- **Datadog** - Application monitoring
- **Surescripts** - e-Prescribing network
- **Quest/LabCorp** - Lab integration

---

## Current Security Posture

### IT Security Team
- **IT Security Manager** (reports to CTO) - 8 years experience
- **Security Engineer** - 4 years experience  
- **Security Analyst** - 2 years experience
- **Annual Security Budget:** $450,000

### Existing Security Controls

#### Identity & Access Management
- AWS IAM with role-based access control
- Multi-factor authentication (MFA) for administrative accounts
- Single Sign-On (SSO) via Auth0 for employees
- Password policy: 12 characters minimum, 90-day rotation

#### Network Security
- AWS VPC with public/private subnets
- Security groups restricting traffic
- AWS WAF protecting web applications
- VPN for remote employee access

#### Data Protection
- Encryption at rest (AWS RDS, S3 encryption enabled)
- Encryption in transit (TLS 1.2 or higher)
- Daily database backups (30-day retention)
- **NO data loss prevention (DLP) solution**

#### Monitoring & Detection
- AWS CloudWatch for infrastructure monitoring
- Datadog for application monitoring
- Basic log aggregation
- **NO SIEM solution**
- **NO intrusion detection system (IDS)**

#### Endpoint Security
- CrowdStrike Falcon (EDR) on all endpoints
- Automatic updates enforced
- Mobile device management (Microsoft Intune)

#### Vulnerability Management
- Weekly Nessus vulnerability scans
- Manual patch management
- Average patch time: 45 days
- No formal prioritization process

#### Security Awareness
- Annual HIPAA compliance training
- Monthly phishing simulations (KnowBe4)
- No role-based security training

### Known Gaps
- ❌ No formal security policies documented
- ❌ No incident response plan
- ❌ HIPAA risk assessment outdated (2+ years old)
- ❌ No business continuity/disaster recovery plan
- ❌ Asset inventory incomplete and manual
- ❌ No formal change management process
- ❌ No security code reviews (SAST/DAST)
- ❌ No third-party vendor assessments

---

## Recent Security Incidents

### Incident 1: Phishing Attack (November 2025)
- **Date:** 2 months ago
- **Description:** Phishing email sent to 15 employees impersonating DocuSign with fake link
- **Impact:** 3 employees clicked and entered credentials
- **Response:** Detected within 2 hours by alert employee, passwords reset, company-wide alert
- **Outcome:** No unauthorized access (MFA prevented), no data breach
- **Lesson Learned:** Need better email filtering and awareness

### Incident 2: Unauthorized Access Attempt (July 2025)
- **Date:** 6 months ago
- **Description:** Multiple failed login attempts from foreign IP (Russia)
- **Impact:** Targeted administrative accounts over 3 days
- **Response:** Blocked by AWS WAF geofencing rules, monitored
- **Outcome:** No successful access, no data exposure
- **Lesson Learned:** Need better alerting for such events

---

## Business Drivers for Assessment

### 1. Revenue Growth Opportunity ($500K contract)
Major hospital system interested in HealthBridge platform.
- **Contract value:** $500,000 annually
- **Requirement:** SOC 2 Type II certification within 6 months
- **Current state:** No SOC 2 certification
- **Impact:** Cannot close deal without certification

### 2. Board of Directors Concerns
Board receiving reports of healthcare breaches in the news.
- Questions about cyber risk exposure
- Need for risk quantification and board-level reporting
- Concern about adequate protection

### 3. HIPAA Audit Requirements
Office for Civil Rights (OCR) increasing healthcare audits.
- Formal HIPAA Security Risk Assessment required
- Last assessment: 2+ years ago (outdated)
- OCR penalties: Up to $1.5M per violation category

### 4. Cyber Insurance Premium Increase
Annual renewal increased 40% ($75K to $105K).
- **Insurer requirements:** Demonstrate security improvements or face higher costs
- Need to show measurable risk reduction

### 5. Competitive Pressure
Competitors marketing their security certifications (SOC 2, HITRUST).
- **Impact:** Lost deals, lengthy security reviews delaying sales
- Need security as competitive differentiator

---

## Assessment Scope

### In Scope
- AWS production and staging environments
- All application servers, databases, storage
- Network infrastructure (VPC, security groups, WAF)
- Employee endpoints (laptops, mobile devices)
- Identity and access management systems
- Protected Health Information (PHI) and PII
- Critical third-party vendors with data access
- Security governance and processes

### Out of Scope
- Customer-owned systems (medical office hardware)
- Customer on-premise servers
- Legacy systems being decommissioned
- Physical security of customer offices

---

## Assessment Objectives

### Primary Objectives
1. Assess current security maturity against NIST Cybersecurity Framework 2.0
2. Identify security gaps across all 6 CSF Functions (23 categories)
3. Develop prioritized 18-month remediation roadmap
4. Enable SOC 2 Type II readiness
5. Quantify risk and demonstrate ROI of security investments

### Success Criteria
- All 23 NIST CSF categories assessed with evidence
- Gap analysis completed with risk ratings
- Remediation roadmap with costs and timelines
- Executive presentation delivered
- **Target:** Achieve NIST CSF Tier 3.0 (Repeatable) within 18 months

### Timeline
- **Week 1-2:** Document review, stakeholder interviews, setup
- **Week 3-5:** Current state assessment (all 23 categories)
- **Week 6:** Gap analysis and prioritization
- **Week 7:** Remediation roadmap development
- **Week 8:** Executive presentation and final report

### Stakeholders
- **CEO** - Overall business impact
- **CTO** - Technology strategy, resources
- **CFO** - Budget approval
- **IT Security Manager** - Primary contact
- **General Counsel** - Legal compliance
- **Board of Directors** - Risk oversight

---

## Document Information

**Prepared By:** Chisom Onyia  
**Date:** January 2026  
**Version:** 1.0  
**Next Review:** March 2026
