# Performing the Assessment

To perform effective security assessments, IT professionals must understand the **structured methodology** for evaluating an organization's security posture. This chapter introduces the **three-level assessment approach** that builds from administrative foundations to technical exploitation:

- **Level I**: Policy review, interviews, and demonstrations
- **Level II**: Vulnerability scanning and technical testing
- **Level III**: Exploitation to prove impact

This systematic approach ensures both **administrative controls** and **technical defenses** are properly evaluated.

---

## The Three Assessment Levels

### Level I: Information Assessment

**Purpose**: Understand if policies exist, are followed, and align with reality.

**Three Main Activities**:

1. **Policy Review** - Examine all 18 classes of security policies across Management, Technical, and Operational categories
2. **Employee Interviews** - Talk to data owners, custodians, and users to understand actual practices
3. **System Demonstrations** - Observe employees performing procedures to verify policy implementation

**Key Principle**: This is an **assessment, not an audit**. Focus is on the big picture and whether procedures protect core business. Uses **nonattribution policy** - comments won't be attributed to specific individuals.

### Level II: Technical Assessment

**Purpose**: Identify technical vulnerabilities in systems and networks.

**Activities**:

- Vulnerability scanning using tools (Nessus, SAINT, ISS Internet Scanner, Retina, SARA)
- Evaluate firewall rule sets and network configurations
- Find vulnerable systems and unpatched services

**Important**: Results must correlate with Level I findings. Produces large amounts of data requiring analysis. Don't skip Level I to jump here.

### Level III: Exploitation

**Purpose**: Actually exploit vulnerabilities to demonstrate real-world impact.

**Tools**: Metasploit, CANVAS, Core IMPACT

**When to Use**:

- To show what attackers can access
- Determine information leakage
- Demonstrate consequences of uncovered vulnerabilities

**Planning Requirements**:

- Schedule for off-hours (late nights, weekends)
- Maintain emergency contact numbers
- Minimize organizational impact
- Keep management informed throughout

---

## 18 Policy Classes (3 Categories)

### Management Controls

Focus on IT security management and risk management.

**1. INFOSEC Documentation**

- **Policies** (top tier): High-level, strategic documents defining what to protect and acceptable risk
- **Guidelines**: Flexible recommendations and best practices
- **Procedures** (most specific): Detailed, step-by-step instructions tied to specific technologies

**2. INFOSEC Roles and Responsibilities**

- **Data Owner**: Senior management (CEO, CIO, CSO) - ultimately responsible for assets
- **Data Custodian**: IT staff who implement controls on behalf of owners
- **User**: End users who must comply with policies and practice due care
- **Security Auditor**: Examines procedures and mechanisms (frequency depends on industry regulations)

**3. Contingency Planning**

- **BCP (Business Continuity Planning)**: Keep operations running during disruptions
- **DRM (Disaster Recovery Management)**: Restore operations after disasters
- Downtime classifications: Critical (minutes-hours), Urgent (1 day), Important (3 days), Normal (1 week), Nonessential (1 month)

**4. Configuration Management**

- 6-step process: Define process → Receive requests → Plan implementation → Implement/monitor → Evaluate/report → Modify plan
- Often managed by Change Control Board
- Critical when moving between software versions or beta to final release

### Technical Controls

Automated security controls executed by computer systems.

**5. Identification and Authentication**

- Three authentication methods: Something you **know** (password), **have** (token), **are** (biometric)
- Password policies must balance security vs. usability

**6. Account Management**

- **Problem**: Up to 60% of accounts may be invalid in some organizations
- Must address: initialization, change control, privilege access, termination, lockout, password changes
- Also covers: password requests, synchronization, lost passwords, help desk authentication

**7. Session Controls**

- **Account lockouts**: Limit failed login attempts before disabling account
- **Screensaver locks**: Activate after predetermined inactivity
- **System timeouts**: Automatic logout after inactivity
- **Warning banners**: Required for legal prosecution - CERT.org warns that failure to include banners makes prosecution difficult

**8. Auditing**

- **Clipping levels**: Alarm thresholds (e.g., lockout after 3 failed logins)
- Detective control that measures how well other controls work
- Best practices: Centralize logging, automate processes, export logs to prevent tampering, maintain manageable log size

**9. Malicious Code Protection**

- Covers all malware: viruses, worms, spyware, Trojans
- Requires both software mechanisms and user training
- All malware threatens availability, integrity, or confidentiality

**10. Maintenance**

- Verify maintenance personnel before allowing access to sensitive areas
- Inadequate verification policies lead to theft by fake maintenance workers

**11. System Assurance**

- **Certification**: Technical validation that systems work as expected
- **Accreditation**: Management's formal approval of certification
- Must repeat if system changes
- Standards: Rainbow Series (NCSC), ITSEC (European), Common Criteria (ISO 15408), ISO 17799

**12. Networking Connectivity**

- Must address all connection types: Wireless, LAN, WAN, VPN, Internet, Modem, Third-party
- Protection mechanisms: ACLs, firewalls, mandatory access control, VLANs, "deny all" policies

**13. Communications Security**

- Protects data in transit (data, voice, fax communications)
- Methods: IPSec, PGP, WPA, VPNs
- Encryption is most direct protection method

### Operational Controls

Security methods implemented by people, not systems.

**14. Media Controls**

- Lifecycle management of all media: paper, disks, CDs, DVDs, hard drives, USB drives
- **Disposal methods**:
    - Paper: Shredding
    - CDs: Destruction
    - Hard drives: Wiping (DOD 5220-22M standard - overwrite with character, complement, random character)
- **Warning**: Los Alamos incident (June 2000) - hard drives with nuclear secrets found missing behind copier

**15. Labeling**

- Formal document classification system
- Two types: Government classification and Commercial classification

**16. Physical Environment**

- Components: Locks, guards, CCTV, fences
- **Critical**: Logical security is useless without physical protection (e.g., someone can just remove hard drive)

**17. Personal Security**

- **Hiring**: Background checks, reference checks, criminal checks, educational history verification
- **NDAs (Nondisclosure Agreements)**: Provided at hire, reviewed at exit - limited protection but provides right to sue
- **Termination**: Exit interview, NDA reminder, account lockout, password changes

**18. Education, Training and Awareness**

- **Tailor to audience**:
    - **Data Owners (Senior Management)**: Costs, benefits, ramifications - not technical details
    - **Data Custodians (Mid-Management)**: Implementation methods, responsibilities, costs of noncompliance
    - **End Users**: Daily tasks, job-specific functions
- **Training types**: Degreed programs, continuing education, in-house training, web-based, classroom, vendor training, on-the-job

---

## The Interview Process

### Purpose

- See how policy matches reality
- Identify where policy and practice deviate
- Solicit improvement ideas from employees (they're the organization's greatest asset)

### Interview Candidates

| **Data Owners** | **Data Custodians** | **End Users** |
| --- | --- | --- |
| Chief security officer | Network manager | Users |
| Chief executive officer | Security administrator | Privileged users |
| Chief technology officer | Department heads | Database administrators |
| Executive staff | Facilities manager |  |

### Interview Best Practices

**Environment**:

- Private location, no supervisors present
- Don't record interviews (inhibits some employees)
- Have second person take notes
- Position yourself without desk/obstruction between you and interviewee

**Nonattribution Policy**:

- Comments won't be attributed to specific individuals outside meeting
- Critical for building trust
- Not about finding guilty parties - about learning what's right and wrong
- Example: If janitor reports seeing confidential info in trash, simply state "media control policies not being followed"

**Time Allocation**:

- End users: 30 minutes
- Data custodians and owners: 1 hour
- Technical interviews: 1.5 hours
- Leave time between interviews for notes and to prevent queuing

**Detecting Dishonesty**:

- Body language: scratching nose, not looking directly at interviewer
- Tone of voice
- Word choice

### Key Interview Questions

- Who is the employee and relationship to organization?
- How long with organization?
- What data can they access? How? What applications?
- What do they perceive as critical/sensitive data and resources?
- Where do they see policy and practice deviate?
- What changes would improve security?
- What vulnerabilities is organization not addressing?

### System Demonstrations

**Purpose**: Clarify disagreements between policy and interviews. Verify policy implementation by having employees perform stated procedures.

**Examples**:

- Test if account lockout works after 3 failed logins (when policy says it should)
- Check if cleaning crew sees restricted documents in trash (not shredded per policy)

**Limitations**: Cannot prove everything works correctly. Technical items best verified with Level II assessment.

---

## Common Policy Problems

Organizations often have **missing, outdated, or poorly written policies**.

**Example**: Detailed modem policy but nothing about wireless devices.

### Well-Designed Documentation System Components

1. **Policy Development**
    - Consider organizational needs, requirements, environment
    - Senior management sets tone and motivates employees
2. **Change Management**
    - Controls for approving policy changes
    - Documentation of changes
    - Who can make changes
3. **Acceptance**
    - Policies routinely bypassed = ineffective
4. **Testing**
    - No way to gauge effectiveness without testing
    - Example: Penetration tests to verify firewall procedures work
5. **Implementation**
    - Must have scheduled implementation
    - Don't let policies exist without being implemented
6. **Reviewing**
    - Policies are **living documents**
    - Must adapt: times change, technologies change, laws change
    - Avoid "dusty book" syndrome

### The Five Ws of Policy Writing

- **What**: What is to be protected (topic)
- **Who**: Who is responsible (responsibilities)
- **Where**: Where does policy reach (scope)
- **How**: How compliance monitored (compliance)
- **When**: When does policy take effect (timing)
- **Why**: Why was policy developed (reason)

**Purpose**: Clear up confusion, not generate new problems. Write for specific audience without needing to sit and explain each item.

---

## Reference Standards

### ISO 17799 (Industry Best Practices)

10 comprehensive sections covering:

1. Security Policy - What policies should look like, how to review
2. Organizational Security - Roles and responsibilities
3. Asset Classification and Control - Ownership and classification
4. Personnel Security - Employment lifecycle
5. Physical and Environmental Security - Prevent unauthorized physical access
6. Communications and Operations Management - Secure communications, change management, media handling
7. Access Control - Principle of least privilege
8. Systems Development and Maintenance - Security built into systems
9. Business Continuity Management - Business continuity controls
10. Compliance - Legal, regulatory, legislative, contractual requirements

### RFC 2196 (5-Step Approach)

1. Identify what you're protecting
2. Determine what you're protecting from
3. Determine likelihood of threats
4. Implement cost-effective controls
5. Periodically review and improve when weaknesses found

### COBIT (Control Objectives for Information and Technology)

- 34 high-level IT control practices
- 318 recommended detailed control objectives
- Audit Guidelines for each practice
- **Purpose**: Bridge gap between control requirements, technical issues, business risks; communicate control levels to stakeholders

---

## Level II & III Details

### Level II: Vulnerability Scanning

**Activities**:

- Probe network
- Evaluate firewall rule sets
- Assess network configurations
- Find vulnerable systems
- Identify unpatched services

**Caveats**:

- Cannot just run tool and consider network secured
- Produces massive amounts of data requiring analysis
- May need infrastructure groups to assist
- Good at foundational issues but requires substantial input for organizational context
- Large organizations may only sample network sections

**Reference**: OSSTMM (Open Source Security Testing Methodology Manual) tests information/data controls, personnel awareness, fraud/social engineering, networks, physical security

### Level III: Vulnerability Exploitation

**Reasons to Perform**:

1. See what attackers can access and infiltrate
2. Determine information leakage
3. Demonstrate end result of vulnerabilities

**Impact**: Very dramatic - can show passwords, secret plans, confidential files

**Drawback**: There will ALWAYS be weaknesses. Identify priority risks and ensure policy structure enables long-term security.

**Sourcing**: Perform internally or hire outside consultants (check references, experience, run background checks)

### Response to Security Incidents

**Process**:

- Users report to help desk or security operations center
- Criticality determined (Critical, Major, Minor)
- **SIRT (Security Incident Response Team)** deployed - includes IT, security, legal, HR
- Investigate without altering forensic evidence
- Internal attackers require strict HR procedures

---

## Chapter Key terms

| **Term** | **Definition**  |
| --- | --- |
| **Audit** | Independent check of records and activities to assess security controls and compliance. |
| **Business Continuity Planning (BCP)** | Method to resume critical functions within a set time after disruption or disaster. |
| **Clipping Level** | Threshold at which an alarm or trigger is activated. |
| **Configuration Management** | Process of controlling and documenting changes to systems, networks, or software. |
| **Contingency Planning** | Preparing for disasters or issues in advance to reduce impact. |
| **COBIT** | IT governance framework with objectives and controls to maximize IT benefits. |
| **Data Owner** | Person responsible for policy and decision-making for data. |
| **Data Custodian** | Person implementing security controls for data, under the owner’s direction. |
| **Ethical Hack** | Authorized hacking to find vulnerabilities; follows rules and legal boundaries. |
| **Guidelines** | Recommended actions or directions in policies/procedures. |
| **NIST 800-42** | Guide for network security testing techniques and tools. |
| **Nonattribution** | Avoiding reference to a source of information. |
| **Policies** | High-level formal security documents. |
| **Procedure** | Detailed, step-by-step instructions for tasks. |
| **RFC-2196** | Practical guidance for securing organizational information and services. |
| **Spyware** | Software that secretly monitors user activity. |
| **Trojan** | Malicious program hidden inside something legitimate. |
| **Virus** | Program that replicates with user interaction; can be benign or destructive. |
| **Worm** | Self-replicating program that spreads independently, often causing denial of service. |
