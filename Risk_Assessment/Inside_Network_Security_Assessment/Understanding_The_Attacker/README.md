# Understanding the Attacker

To assess risks effectively, IT security professionals must **think like attackers** — understanding **who** they are, **why** they attack, **how** they do it, and **what** they target. This knowledge helps in building **stronger defenses** across the entire IT infrastructure. The chapter introduces four key areas:

- **Who attacks**: Insiders, outsiders, hackers, etc.
- **What they do**: Exploit vulnerabilities, bypass controls.
- **Why they do it**: Motivations like money, revenge, or politics.
- **How they do it**: Tools and methods used in attacks.

This attacker-focused view allows professionals to build a **smart, strategic defense**.

---

## Who Are the Attackers?

Attackers can be **internal** or **external**:

- **Internal attackers**: Often disgruntled employees, contractors, or third-party users. They're more dangerous because they may already have access to sensitive systems, especially if they're IT staff.
- **External attackers**: Come from outside the organization and try to exploit system vulnerabilities.

**Internal attacks** are more damaging due to insider access. That’s why companies must enforce **Acceptable Use Policies**, **confidentiality agreements**, and proper **HR exit procedures**.

A **threat** is any event that can harm a system. This includes:

- Unauthorized access
- Data destruction or modification
- Disclosure of sensitive info
- Denial of Service (DoS) attacks

### Attacker Types and Their Characteristics

- **Black Hat Hacker**: Skilled, unethical hacker attacking systems to exploit weaknesses.
- **Cracker**: Expert in reverse engineering and solving complex code problems.
- **Cyber-Terrorist/Cyber-Criminal**: Funded individuals or groups targeting governments or corporations with serious attacks (e.g., DoS, infrastructure sabotage).
- **Disgruntled Employee**: Insider threat with system access, often angry due to job-related issues.
- **Hacker**: Broad term for skilled programmers, often overlaps with "cracker."
- **Phreaker**: Attacks telecom systems to steal services or access.
- **Program Cracker**: Specializes in breaking software licenses and keys.
- **Script/Click Kiddies**: Inexperienced users using pre-made tools to launch basic attacks.
- **System Cracker**: Targets operating system vulnerabilities; often behind major malware.
- **Whacker**: Focuses on hacking wireless networks.
- **White Hat Hacker**: Ethical hacker with permission, helping organizations improve security.

### Who Are the Greatest Threat?

The **greatest threat** to an organization’s IT infrastructure comes from **internal users,** employees, contractors, and third parties who have access to sensitive systems. Among them, **disgruntled employees**, especially IT staff, pose the highest risk due to their access and technical knowledge. To reduce this threat, companies must enforce **background checks**, **Acceptable Use Policies (AUPs)**, and **confidentiality agreements**.

The **second greatest threat** is from **insecure computing habits** by employees, including:

- Sharing infected USBs or CDs
- Installing unauthorized or pirated software
- Downloading unsafe freeware that may contain spyware or adware
- Opening email attachments without caution
- Being careless with confidential data (e.g., leaving screens unlocked or documents exposed)

---

## **What Do Attackers Do?**

Attackers begin by selecting a target and conducting their **own risk and vulnerability assessment**. If the target appears too well-protected, they may move on to an easier one.

Their actions depend on **motivation**:

- For **personal reasons** (e.g., revenge or embarrassment), they may target high-profile companies like PayPal or Citibank.
- For **financial gain**, they go after systems with valuable data, but only if the **risk of getting caught or blocked** is worth the reward.

> Attackers weigh the **risk vs. reward** — sometimes skipping heavily protected systems if the benefit doesn’t justify the effort or exposure.
> 

### Four Kinds of Attacks:

There are **four main types of attacks** on IT infrastructures:

1. **Coordinated Attack**

- Involves **multiple systems and people**, planned in advance (e.g., cyber-terrorist attacks).
- Uses remote-controlled agents to flood the target, causing **network overload** and denial of service.

2. **Direct Attack**

- Targets a **known vulnerability** (e.g., outdated software not patched).
- Examples include **Ping of Death** and **phishing scams** targeting specific individuals.

3. **Indirect Attack**

- Uses **malware like viruses, worms, or Trojans** to exploit common system flaws.
- These are **self-propagating** and cause massive global damage and downtime.

4. **Unstructured Attack**

- Done by **novice attackers** (like Script Kiddies) with no specific plan.
- They use ready-made tools to scan and attack systems casually, often for fun or curiosity.

### Things That Attackers Attack

Attackers target **vulnerabilities** in IT systems when they believe they can succeed without getting caught. These vulnerabilities are usually:

1. **Security Defects**

- Unintended flaws in software (e.g., in firmware, OS, or configs).
- Often patched after vendors release **security bulletins**.

2. **Security Limits**

- Known, documented weaknesses (e.g., FTP or POP3 using **unencrypted transmission**).
- Not bugs, but limitations users must be aware of.

3. **Software Vulnerabilities**

- Caused by coding errors or design flaws (e.g., **buffer overflows**, **injection points**).
- Can allow attackers to run malicious code or access sensitive data.

When these issues are exploited, it leads to **security incidents**. The organization’s **SIRT team** (Security Incident Response Team) responds, and **forensic experts** may collect evidence if legal action is needed.

---

## **Why they do it?**

Attackers are driven by different motives, and not all attacks are targeted or malicious. Some attackers are simply testing their skills or acting on impulse. Common motivations include:

- **Intellectual**: To challenge themselves or "beat the system" — not always meant to harm, but still illegal and potentially damaging.
- **Personal**: Often from **disgruntled employees** seeking revenge or to embarrass the organization.
- **Political**: Driven by ideology — examples include **cyberterrorism**, **website defacement**, or attacks on public infrastructure.
- **Financial**: For **monetary gain** or extortion — includes blackmail, theft, or disruption of e-commerce systems.
- **Ego**: To gain recognition or bragging rights within hacking communities — even if no clear target or benefit exists.

---

## How Do Attackers Attack?

Attackers follow a **logical 3-stage process** when launching attacks on IT systems:

### Stage 1: Reconnaissance, Probing & Scanning

- Attackers **scan for vulnerabilities** using tools like:
    - DNS/SNMP/IP discovery tools
    - Port scanners
    - OS fingerprinting tools
    - Spyware or Trojans
- Goal: Find exploitable weak points before launching the actual attack.

### Stage 2: Access & Privilege Escalation

- Attackers **exploit vulnerabilities** to gain unauthorized access.
- Then they try to **escalate privileges** (e.g., from user to admin) using methods like:
    - Buffer overflows
    - Web form injection

### Stage 3: Eavesdropping, Data Theft or Damage

- Once inside, attackers may:
    - **Steal data** (e.g., credentials, confidential info)
    - **Cause damage** or system disruption
    - **Spy** on communications or activities

Understanding these stages helps security teams **detect and block attacks** more effectively.

### **Reducing the Risk of an Attack**

Understanding how attackers operate allows security professionals to **proactively defend** IT systems using proper security controls. Key mitigation strategies include:

- **PING Sweeps**: Disable ICMP echo on hosts and routers.
- **Port Scanning**: Use **IDS**, firewalls, and network segmentation to detect and limit access.
- **OS Fingerprinting**: Deploy IDS/IPS systems and block device responses.
- **Password Sniffing**: Use **switched Ethernet** and **encrypted passwords**.
- **Password Cracking/Guessing**: Enforce **strong password policies** and **regular changes**.
- **Malformed Data Attacks**: Integrate security in the **software development life cycle** and validate input fields.
- **Banner Grabbing**: Avoid displaying system information in banners or messages.

### **How to Respond to an Attack**

When a security incident occurs:

- **Users report** it to the help desk or security operations center.
- The **criticality** of the incident (Critical, Major, Minor) determines the urgency of the response.
- A **Security Incident Response Team (SIRT)** is deployed—usually including IT, security, legal, and HR staff.
- The SIRT investigates without altering **forensic evidence**, especially when dealing with **internal attackers**, where HR procedures must be strictly followed.

---

## Chapter key terms

| **Term** | **Definition** |
| --- | --- |
| **Acceptable Use Policy (AUP)** | Defines what users (employees, contractors, etc.) are allowed to do on the organization’s IT systems. |
| **Adware** | Software that forces pop-up ads but doesn’t track user behavior like spyware. |
| **Botnet** | A network of remotely controlled infected computers used in coordinated attacks. |
| **Buffer Overflow** | Writing data beyond memory limits due to coding errors, opening doors for malicious exploits. |
| **Confidentiality Agreement** | Legal agreement requiring users to protect sensitive data they access. |
| **Cookies** | Small data files stored by a browser to remember user preferences and sessions. |
| **Defense-in-Depth** | A layered security strategy across multiple areas of the IT infrastructure. |
| **Denial of Service (DoS)** | Attack that floods a system with traffic, making it unavailable. |
| **Distributed Denial of Service (DDoS)** | A DoS attack launched from multiple systems simultaneously. |
| **Domain Name System (DNS)** | Translates domain names to IP addresses and vice versa. |
| **Enterprise Vulnerability Management** | Managing and addressing vulnerabilities across the organization. |
| **Finger** | A Unix utility showing logged-in users and personal info. |
| **Hash** | A mathematical method to verify message integrity and detect tampering. |
| **Honeypots** | Decoy systems set up to lure and monitor hackers’ behavior. |
| **Identity Theft** | Stealing personal or financial data to impersonate someone else. |
| **Insecure Computing Habits** | Poor security behaviors by users due to lack of awareness/training. |
| **Intrusion Detection System (IDS)** | Monitors network activity for suspicious or unauthorized access attempts. |
| **IT Security Architecture and Framework** | Structured hierarchy of policies, standards, and procedures for IT security. |
| **Minimum Acceptable Level of Risk** | The defined risk threshold an organization is willing to tolerate. |
| **Phishing** | Deceiving users into providing confidential information by pretending to be legitimate sources. |
| **Security Bulletins** | Official vendor notices about known security flaws and patch instructions. |
| **Security Defect** | An undocumented flaw that can be exploited as a vulnerability. |
| **Security Incident Response Team (SIRT)** | A cross-functional team that handles real-time security incidents. |
| **Smurf Attack** | A DDoS attack using spoofed PING requests to overwhelm a system. |
| **SNMP Community Strings** | Passwords used to access SNMP-managed devices (default: “public”/“private”). |
| **Social Engineering** | Tricking people into revealing secure information (e.g., pretending to be tech support). |
| **Software Bug** | A programming error that can lead to vulnerabilities if not patched. |
| **Software Flaw** | A design-level error requiring system reengineering rather than a simple patch. |
| **Spyware** | Software that secretly gathers and reports user activity to third parties. |
| **SYN Flood Attack** | A DDoS attack that overwhelms a server by initiating many incomplete TCP connections. |
| **URL (Uniform Resource Locator)** | The address of a website or resource on the internet. |
| **WHOIS** | A tool that provides info about a domain name or IP address (e.g., owner, registrar). |
