# NIST CSF 2.0 Assessment Matrix

**HealthBridge Solutions Security Maturity Assessment**

**Last Updated:** January 2026  
**Assessor:** Chisom Onyia

---

## Assessment Overview

This document contains the detailed assessment of HealthBridge Solutions against all 23 NIST Cybersecurity Framework 2.0 categories across 6 functions.

**Assessment Methodology:**
- Document review and analysis
- Stakeholder interviews
- Technical validation
- Evidence collection
- Maturity tier rating (0-4 scale)

**Maturity Tier Definitions:**
- **Tier 0:** Non-existent - Control does not exist
- **Tier 1:** Partial - Ad-hoc, reactive implementation
- **Tier 2:** Risk Informed - Risk-aware processes, inconsistent application
- **Tier 3:** Repeatable - Formal processes, consistently applied
- **Tier 4:** Adaptive - Continuous improvement, proactive optimization

---

## Assessment Summary

**Progress:** 6/23 categories completed (GOVERN function)

| Function | Categories | Completed | Average Current Tier | Average Target Tier |
|----------|-----------|-----------|---------------------|---------------------|
| GOVERN | 6 | 6/6 | 0.5 | 3.0 |
| IDENTIFY | 3 | 0/3 | - | - |
| PROTECT | 5 | 0/5 | - | - |
| DETECT | 2 | 0/2 | - | - |
| RESPOND | 4 | 0/4 | - | - |
| RECOVER | 2 | 0/2 | - | - |
| **TOTAL** | **22** | **6/22** | **TBD** | **~3.0** |

---

# FUNCTION 1: GOVERN (GV)

## GV.PO - Policy

**Category:** Organizational cybersecurity policy is established, communicated, and enforced

### Current State (Tier 0 - Non-existent)

HealthBridge has no formal cybersecurity policies documented. Only a basic acceptable use policy exists for employees (2 pages, last updated 2019). 

**Current Documentation:**
- No acceptable use policy
- No information security policy formally documented
- No incident response policy
- No access control policy
- No data classification/ handling policy
- No vendor management policy
- No change management policy
- Password policy: 12 characters minimum, 90-day rotation

**Process Gaps:**
- No policy development process
- No policy approval workflow
- No policy communication program
- No policy review schedule
- No policy exception process
- No policy compliance measurement
- HIPAA requires formal written policies and procedures
- SOC 2 trust criteria requires documented policies
- No SOC 2 certification and OCR compliance is lacking

**Company Profile:**
- Explicitly states: "No formal security policies documented"

### Tier Assessment

**Current Tier:** 0 (Non-existent)

**Justification:**
- No formal security policy framework exists
- Single outdated acceptable use policy insufficient
- Does not meet even Tier 1 criteria (ad-hoc implementation)
- Critical foundational control missing

**Target Tier:** 3 (Repeatable)

**Rationale:**
- Required for SOC 2 certification (Trust Services Criteria CC1.2, CC1.3)
- HIPAA Security Rule mandates documented policies (164.316(a))
- Industry standard for healthcare organizations
- Foundational for all other security controls

### Gap Analysis

**Gaps Identified:**

1. **No master information security policy** establishing governance framework
2. **No policy development and approval process** defined
3. **No comprehensive security policy framework** covering required domains
4. **No policy version control** or document management
5. **No formal policy communication and training program**
6. **No annual review and update process**
7. **No policy exception request and approval process**
8. **No measurement of policy compliance**
9. **Missing SOC 2 requirement:** Trust Services Criteria CC1.2, CC1.3
10. **Missing HIPAA requirement:** Security Rule 164.316(a) - policies and procedures

**Specific Policies Needed:**
- Information Security Policy (master document)
- Incident Response Policy
- Access Control Policy
- Data Classification and Handling Policy
- Acceptable Use Policy (updated version)
- Change Management Policy
- Vendor Management Policy
- Remote Access Policy
- Password and Authentication Policy
- Data Retention and Disposal Policy
- Business Continuity Policy
- Disaster Recovery Policy

### Priority

**Priority Level:** CRITICAL

**Justification:**
- **SOC 2 Blocker:** Cannot achieve certification without formal security policies
- **HIPAA Compliance Gap:** Required by Security Rule
- **$500K Revenue Impact:** Hospital contract requires SOC 2
- **Board Oversight:** Cannot govern without policy framework
- **Foundational Control:** Other controls reference and depend on policies
- **Regulatory Risk:** Increases potential fines in breach event
- **Audit Finding:** Will be major finding in any compliance audit

### Business Impact & Remediation

**Business Impact:**
- **Revenue:** $500K annual contract blocked (SOC 2 requirement)
- **Compliance:** HIPAA violation risk, potential OCR penalties up to $1.5M
- **Operations:** No clear standards for employee security behavior
- **Risk:** Increased likelihood and impact of security incidents
- **Reputation:** Cannot demonstrate security commitment to prospects

**Remediation Plan:**

**Phase 1 (Months 0-3): Develop Core Policy Set**
- Develop 10-12 core security policies
- Establish policy governance framework
- Define approval workflow
- **Resources:**
  - External consultant: $25,000 OR
  - Internal effort: 200 hours (IT Security Manager + Legal + Compliance)
  - Policy template licenses: $2,000
  - Policy management platform: $5,000/year
- **Owner:** IT Security Manager (lead), Legal (review), CEO (approval)

**Phase 2 (Months 3-6): Implement Policy Governance**
- Communicate policies organization-wide
- Conduct policy awareness training
- Implement policy acknowledgment system
- Establish annual review schedule
- **Resources:**
  - Policy training program: $10,000
  - Policy acknowledgment system: $3,000
  - Ongoing maintenance: 5 hours/month
- **Owner:** IT Security Manager

**Total Investment:** 
- **Cost:** $45,000
- **Time:** 225 hours
- **Duration:** 6 months

**Expected Outcome:**
- Achieve Tier 3 maturity for Policy category
- Enable SOC 2 Type II certification path
- Meet HIPAA Security Rule requirements
- Establish foundation for all other security controls
- Reduce regulatory risk exposure

---

## GV.RM - Risk Management Strategy

**Category:** Organizational priorities, constraints, risk tolerance and appetite statements, and assumptions are established, communicated, and used to support risk decisions

### Current State (Tier 0- Non-existent)

HealthBridge has no formal risk management strategy or framework documented. Risk assessment is performed ad-hoc when security issues arise.

**Current Approach:**
- Last HIPAA Security Risk Assessment: Over 2 years ago (outdated)
- No enterprise risk management (ERM) program
- No risk appetite statement
- No risk tolerance levels defined
- No formal risk assessment methodology
- Security decisions made reactively without risk framework

### Evidence Collected

**Document Reviewed**
- No risk appetite statement or business continuity plan in place
- Outdated HIPAA Risk assessment document
- Ad-hoc communication when security issues arise

**Interviews**
- IT Security Manager confirmed no formal business continuity plan (Interview: Feb 6, 2026)
- Security issues discussed and addressed but never through a proper risk assessment methodology
- Board is requesting risk qualification with no current mechanism to prove it

### Tier Assessment

**Current Tier:** 0 (Non-existent)

**Justification**
-  No enterprise risk management (ERM) framework
-  No formal risk appetite statement
-  No risk register
-  No mechanism to provide risk quantification
-  No updated HIPAA assessment

**Target Tier:** 3 (Repeatable)

**Rationale**
- HIPAA Security Rule requires accurate and thorough assessment of risks amd vulnerablities (45 CFR 164.308(a)(1))
- Industry standard for healthcare organizations
- Business continuity and disaster recovery plan mandatory and required to be renewed at least annually (NIST Special Publication 800-34)

### Gap Analysis

**Gap Identified**
1. **No updated HIPAA risk assessment
2. **No business continuity/ disaster recovery plan
3. **No risk appetite and risk tolerance statements
4. **No enterprise risk management framework
5. **No mechanism for risk quantification

### Priority

**Priority Level:** CRITICAL

**Justification:**
- **OCR audit exposure impact:** up to $1.5M per violation category
- **Lack of RBDM posture:** Inability to demonstrate risk-based decision making to board or insurers
- **No risk register and risk tolerance statements:** Lack of formal document to display risk quantification and prioritization process

### Business Impact & Remediation

**Business Impact:**
- **Revenue:** Annusl renewal cyber insurance increased by 49% (75k to 105k) 
(Insurer requirement)
- **Compliance:** potential OCR penalties up to $1.5M,
- **Operations:** No formal risk prioritization process, No data handling process
- **Risk:** Longer response time to incidents and insurance premium increase
- **Reputation:** Inability to show adequate protection to board of directors, and measurable risk reduction to insurers

**Remediation Plan**

**Phase 1: Define Risk management action plan**
- Conduct full HIPAA Security Risk Assessment immediately
- Establish enterprise risk register
- Define company risk tolerance level
- Create Data Loss Prevention (DLP) solution
- Create enterprise risk management framework

**Phase 2: Implement Action Plan**
- Document a formal risk prioritization process
- Document incident response plan
- Document company's disaster recovery/ business continuity plan
- Implement quarterly risk review cadence

**Expected Outcome:**
- Achieve Tier 3 maturity for Risk manan=gement strategy category
- Have up-to-date HIPAA security risk assessment
- Demonstrate security improvement to insurer for lower insurance rate
- Reassure board of directions about company's adequate protection
- Establish up-to-date documented incident responce plan and disaster recovery plan through all parts of the company security sectors


---

## GV.SC - Cybersecurity Supply Chain Risk Management

**Category:** Supply chain risk management processes are identified, established, managed, monitored, and improved by organizational stakeholders

### Current State (Tier 0)

HealthBridge has no formal third-party vendor risk management program. Critical vendors have access to patient data but are not assessed for security. The third-party vendors identified include stripe, twilio, SendGrid, Auth0, PagerDuty, Datadog, Surescripts, and Quest/LabCorp.

**Current Documentation:**
- No vendor security assessments performed
- No vendor due diligence process
- Contracts lack security requirements
- Critical vendors (Stripe, Twilio, Auth0, etc.) not evaluated but have access to critical information
- Vendors risk are not discussed before contract signing
- BAAs not confirmed for all PHI-handling vendors- potential HIPAA violation

**Process Gaps**
- No vendor management policy
- No vendor security assessments performed or security monitoring process
- Vendors are not evaluated before given access to PHI or production systems
- Contracts are not properly reviewed and risks posed by vendors are not taken into extensive consideration in a classification system
- No formal documentation for process to conclusion of a partnership or service agreement

## Evidence Collected

**Documentation Review**
- No vendor management policy found
- Contracts with vendors do not cover certain security measures such as incident planning, response, and recovery activities
- Third-party vendors are not assessed before signing contracts

**Company Profile:**
- Explicitly states: "No third-party vendor assessments"

### Tier Assessment

**Current Tier:** 0 (Non-existent)

**Justification**
- No vendor risk management prograam of any kind
- About 8 critical vendors with PHI access and zero security assessments represents extreme exposure
- Missing BAAs for PHI-handling vendors is an active HIPAA violation
- Third-party breach of vendors like Auth0 or SureScripts could direclty expose up 1.2M patient records

  **Target Tier:** 3 (Repeatable)
  **Rationale**
  - HIPAA 164.308(b)(1) requires written BAAs with all Business Associates handling ePHI
  - SOC 2 CC9.2 rwquires vendor and business partner risk management program
  - Healthcare supply chain attacks have dramatically increased
  - A vendor breach without a management program means Healthbridge has no visibility, control, or response capability
 
  ### Gap Analysis

  **Gaps Identified**
  - No 
---


