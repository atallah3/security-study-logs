# Scoping the Project
Scoping is the official start of a vulnerability assessment. A formal document is created to define project activities, schedule, needed support, and which parts of the network are included or excluded. This document serves as a roadmap and must be approved by a senior security officer. It should also include legal and nondisclosure clauses to protect the team and data.

## **Defining the Scope of the Assessment**

Defining the scope is a **critical early step** in any vulnerability assessment. Before meeting with management, it’s important to understand **what is driving the assessment**, such as:

- Compliance requirements.
- A recent security breach.
- Legal obligations.
- general due diligence.

> management might not have all the answers, and that's why they rely on **your expertise**.
> 

Before the initial meeting, gather **network documentation**, understand the **technology in use**, and review how **security is currently managed**. In the meeting, focus on identifying:

- What’s most **critical** to the organization.
- Key **products and services.**
- Supporting **technologies.**
- **sensitive information** that must be protected.

---

### **Key Events During Scoping**:

- Identifying **driving events**
- Holding the **initial meeting**
- Taking on the role of **project manager**
- **Staffing** the assessment team
- Conducting the **kickoff meeting**
- **Building the project timeline**

---

## **Driving Events**

The reason behind a vulnerability assessment affects how deep and wide it goes. Common driving events include:

- **Due diligence** (e.g. during mergers) – focuses on tech, roles, integration, Training and awareness.
- **Compliance** (e.g. HIPAA, SOX) – ensures legal requirements are met to avoid fines or penalties.
- **Security breach** – often internal, requires fast, technical response (access controls, hardening, etc.).

Stricter security (like “deny all” firewall rules) means better preparedness. Always have an **incident response plan** ready before problems happen.

---

## Initial Meeting

Before meeting with management, you should gather **key information** to better understand the **scope and effort** of the assessment. A **standardized information request form** helps collect this data in advance or right after the project is approved.

The form covers four main areas:

1. Administrative
    1. What is the core mission of the organization?
    2. How many locations does the organization have?
    3. What is the total number of locations?
    4. Does the assessment encompass all locations, a limited number of sites, or a sampling across all sites?
    5. What event is driving this assessment?
    6. Does the organization have existing security policies and procedures?
    7. Does the organization have physical controls in place to control the movement of employees and visitors?
    8. Do any vendors or corporate partners have access to the network?
    9. Are IT services outsourced, and if so, which ones?
2. Technical
    1. How many servers are located at each site?
    2. What OSs are in place for these servers?
    3. How many workstations are located at each site?
    4. What OSs are in place for these workstations?
    5. What networking protocols are used?
    6. Are there any mainframes?
    7. How many connections are there to the Internet?
    8. What services are made available externally?
    9. What services are made available internally?
    10. Are wireless technologies used?
    11. Is VoIP used?
    12. What types of redundant systems are in place?
3. Security
    1. What type of encryption technologies are used?
    2. Is there aVPN?
    3. Is authentication centralized?
    4. What type of authentication systems are used?
    5. How is access controlled?
    6. What type of firewalls are used?
    7. Is there an IDS in place?
4. Legal
    1. What state, provincial, and federal laws must the organizations comply with?
    2. HIPAA
    3. GLB
    4.  SOX
    5.  Family Education Rights and Privacy Act
    6.  National Institute of Standards and Technologies
    7.  Management of Information Technology Security (MITS)

---

## **Becoming the Project Manager**

If you're involved in scoping the project, you're likely the **team leader** or a key figure in the assessment. This role requires both **technical** and **project management skills** — including the ability to manage people effectively.

As the **project manager**, your responsibilities include:

- Selecting team members
- Defining the scope
- Launching and overseeing the assessment
- Keeping the team focused and motivated
- Managing time and deadlines
- Organizing and communicating results

---

## **Staffing the Assessment Team**

The size and type of the assessment determine how many and what kind of people you’ll need. Look for team members with:

- **Technical skills** (OS, networking, security, scanners, etc.)
- **Role-based traits** (Inspectors, Team Builders, Idea People, Critics)

Assessments vary:

- **Level I**: Policy-based (less technical)
- **Level II**: Technical (requires scanner use, firewall analysis.)
- **Level III**: Penetration testing (may need outside specialists)

Use the **SMART** method when assigning tasks (Specific, Measurable, Achievable, Realistic, Time-limited, Written-project planning).

Also, create a **team directory** with all contact details.

---

### **Kickoff Meeting**

This is the **official start** of the assessment, where you meet with management and stakeholders to finalize plans. Key tasks include:

- **Introductions** (break the ice)
- **Mission statement** (align goals)
- **Identify critical systems/info**
- **Review assessment levels**:
    - *Level I*: Policy review only
    - *Level II*: Adds vulnerability scanning
    - *Level III*: Penetration testing
- **Finalize the scope** (lock in what’s in/out)
- **Identify key personnel** (across locations)
- **Set logistics** (team workspace, access, etc.)
- **Get written approval** (for scope + legal protections)

---

### **Building the Assessment Timeline**

The timeline defines:

- **How long** the project takes
- **What happens when**
- Helps **prevent scope creep** (uncontrolled expansion of scope)

Tips:

- Watch for schedule/cost overruns
- Stick to the agreed scope
- Communicate regularly with the team

> A typical assessment lasts about 12 weeks and follows these 7 steps:
> 

### **Seven Scoping Steps:**

1. Determine driving events
    1. Hold the initial meeting
2. Establish the team
    1. Hold the kickoff meeting
3. Identify critical items
    1. Create the timeline
4. Develop a written protocol

![Screenshot 2025-09-10 at 5.23.22 PM.png](attachment:5ffcf59e-ffec-463a-a207-5f261a03c07c:Screenshot_2025-09-10_at_5.23.22_PM.png)

---

## Reviewing Critical Systems and Information

At this stage, the goal is to identify the organization’s **most critical systems and data**. If management hasn’t already done this, you must. The recommended approach is the **NSA Information Assessment Methodology (IAM)**, which provides a structured way to evaluate importance using three factors: **confidentiality, integrity, and availability (CIA)**.

The process uses two matrices:

1. **Organization Information Criticality Matrix (OICM)** – identifies and ranks the importance of information assets.
2. **Systems Criticality Matrix (SCM)** – ranks the systems that store, process, or transmit that information.

This ensures you know exactly **what’s most valuable and what must be prioritized** in the assessment.

## **Organization** Information Criticality Matrix

this process looks at the impact if info or systems are lost. It’s done in the **kickoff meeting** with management input. Steps:

1. Identify information types
2. List impact attributes
3. Define impact levels

### **1. Identify Information Types**

Information includes all data the company handles (e.g., customer details, HR data, firewall configs). In the kickoff meeting, brainstorm a list but **filter out irrelevant items** (like cafeteria menus) that don’t affect the mission.

Then, **roll up the data** into broader categories for clarity. Common categories:

- Human resource data
- Customer data
- Network data
- Management data
- Facilities/plant data
- Financial data

Important: Keep the focus on **information**, not systems (e.g., email is a system, not an information type).

### **2. List Impact Attributes**

Once information types are listed, the next step is to define **impact attributes**—factors that measure how losing or compromising that information would hurt the organization. This is **qualitative** (ranked, not dollar-based).

The core attributes are the **CIA triad**:

- **Confidentiality**
- **Integrity**
- **Availability**

Other factors (like authorization, accountability, audit, etc.) can be added, but keeping the list short makes the process easier.

### 3. Define Impact Levels

Impact levels show how much **damage or loss** the organization would face if confidentiality, integrity, or availability of information is compromised.

They can be ranked in different ways (e.g., scales of 1–10, 0–5), but a simple **High/Medium/Low** model is often easiest:

- **Low** → Minor inconvenience or delay
- **Medium** → Significant impact (e.g., fines, loss of confidence, lost partnerships)
- **High** → Severe damage (e.g., loss of key customers, lawsuits, even loss of life)

Organizations should **adapt the scale** to fit their size and structure, but simplicity makes the analysis easier to use and explain.

![Screenshot 2025-09-10 at 7.55.52 PM.png](attachment:8397db31-7b2b-4b42-9266-cac14fa07c31:Screenshot_2025-09-10_at_7.55.52_PM.png)

As facilitator, you guide the company in rating each **information type** (e.g., training, client, sales, HR) against **confidentiality, integrity, and availability** as **High/Medium/Low**.

- Example: Training info rated **Low** across all three, since losing or altering it wouldn’t critically harm operations.
- Some owners may argue for higher ratings, but the goal is a **high-level overview**, not detailed asset evaluation.

The final matrix showed:

- **Sales info (confidentiality & integrity)** = **High** → the top priority, since leaks or tampering could be disastrous in competitive bidding.
- Other categories rated lower.

A **“high-water mark”** is then created: the **highest rating in each column** carried down, highlighting the organization’s **most critical attributes**.

![Screenshot 2025-09-10 at 8.03.16 PM.png](attachment:f7e73438-288e-4558-971f-562a0e1c3c39:Screenshot_2025-09-10_at_8.03.16_PM.png)

## **Systems Criticality Matrix (SCM)**

After identifying critical information, the next step is identifying **critical systems** that store, process, or transmit it. Examples include **financial, HR, sales, client databases, and security systems**.

- The process is the same as the OICM: rate systems by **confidentiality, integrity, availability (CIA)**.
- Example: Sales systems rated **High** for confidentiality and integrity (critical for bidding). Internet systems rated **Low** since they don’t impact sales.
- A **high-water mark** is created, showing confidentiality and integrity as top priorities.

### **Compiling the Needed Documentation**

With critical systems identified, the team must gather **security documentation** for review. Standards like **NSA IAM**, **NIST 800-26**, and **ISO 17799** define required policies, divided into three categories:

- **Management** (e.g., roles, contingency planning, configuration management)
- **Technical** (e.g., authentication, auditing, malware protection)
- **Operational** (e.g., media controls, physical security, training)

Policies can be:

- **Advisory** → set consequences (e.g., illegal software use)
- **Informative** → educate staff (e.g., resource guidelines)
- **Regulatory** → ensure compliance with laws (e.g., records retention)

Also gather **system diagrams**:

- **Logical** (how data flows from a user perspective)
- **Physical** (hardware, connectivity, interfaces)

---

### Document Control Form

To manage all documents, use a **tracking system** noting request date, review date, and custodian. One person should be assigned to control document flow.

![Screenshot 2025-09-10 at 8.09.23 PM.png](attachment:3d361330-be2b-4e42-b4cd-426a856f65fa:Screenshot_2025-09-10_at_8.09.23_PM.png)

## Chapter Key terms

| **Term** | **Definition** |
| --- | --- |
| **BIA (Business Impact Analysis)** | Part of business continuity; identifies which functions are most critical after a disaster. |
| **Criticality** | The level of importance of information or systems to the organization. |
| **Ethical Hackers** | Security pros who legally test systems to find vulnerabilities. |
| **Kick-off Meeting** | First meeting with team & management to align goals, scope, and plan. |
| **Level I Assessment** | Reviews policies/procedures; no hands-on testing (interviews, docs). |
| **Level II Assessment** | Adds vulnerability scans and hands-on technical testing. |
| **Level III Assessment** | Penetration test; adversarial, simulates real-world attacks. |
| **NSA IAM** | NSA’s structured method for vulnerability assessments. |
| **OICM** | Organizational Information Criticality Matrix; ranks information types by confidentiality, integrity, availability (CIA). |
| **SCM** | Systems Criticality Matrix; ranks systems that store/process/transmit information. |
| **Penetration Test** | Authorized simulation of an attack to uncover weaknesses. |
| **Qualitative Assessment** | Risk analysis using descriptive scales (low/medium/high). |
| **Scope Creep** | Uncontrolled expansion of project scope → delays & cost overruns. |
| **Vulnerability** | Weakness in software, hardware, or people that attackers can exploit. |

---
[➡️ Next Chapter](/Risk_Assessment/Inside_Network_Security_Assessment/Understanding_The_Attacker)
---
