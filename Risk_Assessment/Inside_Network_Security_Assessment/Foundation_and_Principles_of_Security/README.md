
# **Basic Security Principles**

confidentiality, integrity, and availability **(CIA)** form the basic building blocks of any good security initiative.

## Availability

- The concept of availability provides that information and systems are available when needed.
- Disaster recovery is tied closely to availability because it’s all about getting critical systems up and running quickly. Availability is attacked by denial-of-service (DoS) attacks.
- If you need access at 2 am to backup tapes that are stored in a facility that allows access only from 8 am to 5 pm, you have an availability problem.

## Integrity

- Integrity provides for the correctness of information and allows users of information to have confidence in its correctness.
- Integrity must be protected in two modes: **storage** and **transit**.
    - Storage
        - Information in storage can be protected by using access and audit controls.
        - Cryptography can also protect information in storage through the use of hashing algorithms (MD5, WFP, etc).
    - Transit
        - Integrity in transit can be ensured by the protocols used to transport the data. These security controls include checksums, hashing, and cryptography.

## Confidentiality

- Confidentiality addresses the secrecy and privacy of information.
- Confidentiality must be protected in storage and in transit.
    - Storage
        - Items such as locked doors, armed guards, and fences.
    - Transit
        - Cryptography a useful tool to protect the confidentiality of information in transit. By sending information in an encrypted form, attackers are denied the opportunity to sniff clear text information.

---

# **Security Requires Information Classification**

> All companies should take steps to protect the integrity and confidentiality of their information assets. An information classification system is one big step toward accomplishing this goal.
> 

there is more than one way to categorize informations. The governmental information classification system is one widely used method. Another is the commercial information classification system.

## The governmental information classification system

> The governmental system is most concerned with protecting the confidentiality of information
> 

**it is divided into categories:**

- **Unclassified:** Information is not sensitive and need not be protected. Its loss or
disclosure would not cause damage.
- **Confidential:** Its disclosure could cause damage to national security and should
be safeguarded against disclosure.
- **Secret:** Its disclosure would be expected to cause serious damage to national
security and may disclose significant scientific or technological developments.
- **Top Secret:** Its disclosure would cause grave damage to national security. This
information requires the highest level of control.

## **Commercial Information Classification System**

> The nongovernmental private sector also has established information classification standards.
> 

**it is divided into categories:**

- **Public:** Similar to unclassified information in that its disclosure or release would
cause no damage to the corporation.
- **Sensitive:** This information requires controls to prevent its release to unauthorized parties. Damage could result from its loss of confidentiality or its loss of integrity.
- **Private:** This category of restricted information is considered personal in nature
and might include medical records or human resource information.
- **Confidential:** This is the most sensitive rating. This is the information that keeps
a company competitive. Not only is this information for internal use only, but its
release or alteration could seriously affect or damage the corporation.

---

# **The Policy Framework**

> Policies put everyone on the same page and make it clear where senior management stands on policy issues.They also set the overall tone and define how security is perceived by those within an organization. Policy must flow from the top
> 

## **Types of Policies**

- **Management:** These policies define security roles and responsibilities within an
organization.They also define how policies are created, revised, and retired.
- **Operational:** These policies deal with operational aspects of an organization.
Examples of operational controls include physical security and employee training
and awareness.
- **Technical:** These policies address all things that are technical. These are the policies that IT employees are familiar with. These types of policies cover such things as identification, authentication, and account management.

### Policies should do six things for a company:

- Protect confidential, and sensitive information from unauthorized disclosure, modification, theft or destruction.
- Define appropriate and inappropriate activities of employees and include consequences.
- Reduce or eliminate legal liability to employees and outsiders.
- Prevent waste of company IT resources.
- Comply with federal, state, provincial, local, and regulatory requirements.
- Demonstrate due diligence and due care.

---

# **Defining Appropriate Policy**

- **Purpose:**  why the policy was created, what is its purpose, and what
the organization will gain from its creation.
- **Scope:** Specifies who the policy applies to.
- **Responsibility:** Defines who is responsible. Someone must be in charge of the
policy and verify that it is properly implemented.

> When the draft policy is developed, it must be approved by upper management and evaluated to ascertain that the objectives that drove the policy development have been met or exceeded
> 

# **Deploying Policy**

After the policies have been created, you will need the help of the entire organization to get them deployed and put in place.

## Three critical items are needed for success:

- **Implementation:** Policies should be introduced gradually in stages to avoid disruptions such as system lockouts or overloaded help desks.
- **Employee Awareness:** Employees must be informed and trained on new policies. HR and security should work together to provide training, enforce usage rules.
- **Employee Buy-In:** Mid-management and staff acceptance is critical. If policies are overly annoying, employees may resist or bypass controls, creating new risks. Policies should balance security with usability.

## **Policy Life Cycle**

Policies require continuous monitoring, updating to stay relevant. Each update must again be deployed, explained, and supported.

---

### **AAA in Security: Authentication, Authorization, and Accountability**

These three functions form the foundation of enforcing security policies, controlling access, and auditing activities.

### **1. Authentication** – Verifying identity

- **Something you know:** Passwords.
    - Early passwords were short and weak.
    - Complexity rules improved security but often led users to insecure habits (writing them down).
    - Still the weakest authentication method.
- **Something you have:** Tokens.
    - Generate **one-time passwords (OTPs)**.
    - Two types:
        - **Synchronous tokens:** Time-based codes synced with a server.
        - **Asynchronous tokens:** Use a challenge–response process.
    - Often combined with passwords for **two-factor authentication**.
- **Something you are:** Biometrics.
    - Based on unique physical traits (fingerprints, voice, etc.).
    - Enrollment required for comparison later.
    - Accuracy measured by **False Acceptance Rate (FAR)**, **False Rejection Rate (FRR)**, and **Crossover Error Rate (CER)**.
    - Advantages: cannot be forgotten, shared, or easily stolen.

---

### **2. Authorization** – What a user is allowed to do

- Comes **after authentication**.
- Determines what commands, processes, and resources a user can access, based on policies.
- **Three main models:**
    1. **Mandatory Access Control (MAC)**
        - System-controlled, **static** access based on classification labels (e.g., *Top Secret, Secret, Sensitive*).
        - Common in military and government (DoD, CIA, NSA, FBI).
        - Users cannot change access rights.
    2. **Discretionary Access Control (DAC)**
        - **Owner-controlled** access (decentralized).
        - Widely used in commercial systems (e.g., Windows NT, 2000, XP).
        - Users assign permissions (read/write/full control) to others.
    3. **Role-Based Access Control (RBAC)**
        - Access tied to a **user’s role** within the organization.
        - Maps to organizational structure.
        - Reduces administrative burden (permissions assigned to roles/groups, not individuals).
        - Common in banks, enterprises, and systems like Windows Server 2003+.

---

### **3. Accountability** – Tracking and auditing user actions

- Ensures administrators can see **who did what, and when (e.g. Logs)**.
- Used for:
    - Incident response
    - Intrusion detection
    - Forensics & troubleshooting
- Requires **strong authentication** to link actions to specific individuals.
- Must comply with **laws & regulations**:
    - Organizations should use **acceptable use policies** or **login banners** to notify users of monitoring.
    - Without notice, legal prosecution may fail or organizations may face privacy violation lawsuits.

---

### **Encryption** – Protecting data from unauthorized access

- **Definition:** Encoding data so only authorized parties can read it.
- **Why it’s needed:** To protect sensitive information (banking details, credit cards, SSNs, trade secrets, etc.).

---

### **Social Engineering** – Human manipulation in security attacks

- **Definition:** Tricking people into revealing sensitive info or granting access.
- **Protection:** Best defense is **security awareness training** for employees.

**Phishing:** Common social engineering attack using fake emails to steal passwords, credit card numbers, or bank info.

---

| **Term** | **Simple Definition** |
| --- | --- |
| **Accountability** | Tracking actions on a system back to a specific user. |
| **AES (Advanced Encryption Standard)** | Current U.S. encryption standard (128, 192, or 256-bit keys); fast and secure. |
| **Authentication** | Verifying a person’s identity (passwords, tokens, biometrics). |
| **Authorization** | Granting or denying access to resources based on credentials. |
| **Availability** | Ensuring systems and data are accessible to authorized users when needed. |
| **Bell-LaPadula Model** | Access control model focused on **confidentiality** (used in military). |
| **Biba Model** | Access control model focused on **integrity** (protects data accuracy). |
| **Clark-Wilson Model** | Integrity model for commercial systems; enforces separation of duties, auditing, and controlled access. |
| **CERT (Computer Emergency Response Team)** | Organization that helps with incident response, alerts, and security improvement. |
| **Confidentiality** | Ensuring data is not disclosed to unauthorized people. |
| **CER (Crossover Error Rate)** | Point where false accept rate = false reject rate in biometrics; lower CER = more accurate. |
| **DES (Data Encryption Standard)** | Older symmetric encryption (56-bit key, 64-bit blocks); now insecure, replaced by 3DES or AES. |
| **Defense in Depth** | Layered security approach with multiple protections (admin, technical, physical). |
| **DoS (Denial-of-Service) Attack** | Attack that overloads systems/networks to deny access to legitimate users. |
| **DAC (Discretionary Access Control)** | Access model where resource **owners decide** who can access their data. |
| **Encryption** | Converting readable text into ciphertext to protect data. |
| **FAR (False Acceptance Rate)** | Biometric error rate where an unauthorized person is wrongly accepted. |
| **FRR (False Rejection Rate)** | Biometric error rate where a valid user is wrongly rejected. |
| **Hashing Algorithm** | One-way function to verify data integrity (detects any changes). |
| **Inference Attacks** | Attacks that guess sensitive info by linking unrelated data. |
| **Integrity** | Ensuring data is accurate, complete, and unaltered. |
| **MAC (Mandatory Access Control)** | System-enforced access model based on labels/classifications (e.g., Top Secret). |
| **RAID (Redundant Array of Inexpensive Disks)** | Disk system using multiple drives for fault tolerance & performance. |
| **RBAC (Role-Based Access Control)** | Access model where permissions are assigned to roles, not individuals. |
| **Social Engineering** | Tricking people into revealing information or breaking security. |
| **TCSEC (Trusted Computer Security Evaluation Criteria)** | Standards for rating system security; also called the **Rainbow Series**. |

---
[➡️ Next Chapter](/Risk_Assessment/Inside_Network_Security_Assessment/Why_Risk_Assessment)
---
