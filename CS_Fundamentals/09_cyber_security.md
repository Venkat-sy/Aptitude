# Cyber Security

## Part 1: Quick Short Notes (Fundamentals)

### 1. CIA Triad
*   The core foundation of Information Security.
*   **Confidentiality:** Protecting data from unauthorized access (e.g., Encryption, Passwords).
*   **Integrity:** Ensuring data has not been tampered with or altered by unauthorized parties (e.g., Hashing, Digital Signatures).
*   **Availability:** Ensuring data and systems are available to authorized users when needed (e.g., Backups, DDoS mitigation, Redundancy).

### 2. Malware (Malicious Software)
*   **Virus:** Attaches itself to a clean file/executable and spreads when the user executes the file.
*   **Worm:** A standalone malware that self-replicates and spreads across networks automatically without user intervention.
*   **Trojan Horse:** Disguises itself as legitimate or useful software to trick the user into installing it. Does not self-replicate.
*   **Ransomware:** Encrypts the victim's data and demands payment (ransom) for the decryption key.
*   **Spyware:** Secretly monitors and gathers user information (e.g., Keyloggers capturing passwords).

### 3. Phishing & Spoofing
*   **Phishing:** A Social Engineering attack where attackers impersonate a trusted entity (via email, SMS) to trick victims into revealing sensitive info (passwords, credit cards) or clicking malicious links.
*   **Spear Phishing:** Highly targeted phishing aimed at a specific individual or organization.
*   **Spoofing:** Falsifying data to masquerade as another identity.
    *   *IP Spoofing:* Changing the source IP address in a packet to hide the sender's identity.
    *   *MAC Spoofing:* Changing the factory-assigned MAC address of a network interface.

### 4. DDoS Attacks (Distributed Denial of Service)
*   **DoS (Denial of Service):** An attack aimed at shutting down a machine or network, making it inaccessible to its intended users by flooding it with traffic.
*   **DDoS:** A DoS attack originating from multiple, distributed sources (often a botnet of compromised devices). Harder to stop because traffic comes from many IPs.

### 5. Web Security
*   **SQL Injection (SQLi):** Inserting malicious SQL code into web input fields to manipulate the backend database, bypass logins, or steal data. Prevention: Parameterized Queries.
*   **Cross-Site Scripting (XSS):** Injecting malicious client-side scripts (like JavaScript) into webpages viewed by other users to steal session cookies or hijack sessions. Prevention: Input Sanitization.
*   **CSRF (Cross-Site Request Forgery):** Tricking an authenticated user's browser into executing unwanted actions on a web application where they are currently logged in. Prevention: Anti-CSRF Tokens.

### 6. Incident Response & Digital Forensics
*   **Incident Response (IR):** A structured approach to handling and managing the aftermath of a security breach or cyberattack. Phases: Preparation $\rightarrow$ Identification $\rightarrow$ Containment $\rightarrow$ Eradication $\rightarrow$ Recovery $\rightarrow$ Lessons Learned.
*   **Digital Forensics:** The recovery, investigation, and analysis of material found in digital devices, often in relation to computer crime. Strict chain of custody must be maintained for evidence to be valid in court.

---

## Part 2: Placement-Related MCQs

1. Which element of the CIA Triad ensures that information is not modified by unauthorized individuals?

A) Confidentiality

B) Integrity

C) Availability

D) Authentication

**Answer:** Option **B**

**Explanation:**

Integrity ensures that data is accurate, complete, and has not been improperly modified or corrupted during storage or transit. This is often verified using hash functions.

---

2. What type of malware is self-replicating and spreads across networks without requiring any action from the user?

A) Virus

B) Trojan Horse

C) Worm

D) Ransomware

**Answer:** Option **C**

**Explanation:**

Unlike a virus, which requires a user to execute a host file, a worm is a standalone program that actively exploits network vulnerabilities to replicate and spread itself automatically from machine to machine.

---

3. An attacker sends an email that looks exactly like it came from your bank, asking you to click a link and verify your account details. What type of attack is this?

A) SQL Injection

B) Phishing

C) Denial of Service

D) Man-in-the-Middle

**Answer:** Option **B**

**Explanation:**

Phishing is a social engineering attack where the attacker masquerades as a trusted entity (like a bank) to deceive the victim into handing over sensitive information such as login credentials or credit card numbers.

---

4. Which web vulnerability occurs when user input is executed as a script in the victim's browser?

A) SQL Injection (SQLi)

B) Cross-Site Request Forgery (CSRF)

C) Cross-Site Scripting (XSS)

D) Buffer Overflow

**Answer:** Option **C**

**Explanation:**

Cross-Site Scripting (XSS) occurs when an application includes untrusted, unsanitized data in a web page. This allows attackers to inject malicious scripts (like JavaScript) into the web pages viewed by other users, often to steal session cookies.

---

5. What is the best defense mechanism against SQL Injection attacks?

A) Hashing passwords

B) Using SSL/TLS encryption

C) Implementing a web application firewall (WAF)

D) Using Parameterized Queries (Prepared Statements)

**Answer:** Option **D**

**Explanation:**

Parameterized queries (or prepared statements) ensure that the database treats user input strictly as data, not as executable code. This completely neutralizes SQL injection attempts, as malicious SQL commands will just be read as literal strings.

---

6. In a DDoS attack, the attacker typically utilizes a large number of compromised devices controlled remotely. What is this network of devices called?

A) A honeypot

B) A botnet

C) A VPN

D) A proxy chain

**Answer:** Option **B**

**Explanation:**

A botnet is a network of hijacked devices (computers, IoT devices, servers) infected with malware and controlled by a central attacker (botmaster). They are frequently used to generate the massive amounts of traffic required for a Distributed Denial of Service (DDoS) attack.

---

7. In the context of Incident Response, what is the primary goal of the "Containment" phase?

A) To identify who performed the attack.

B) To restore the systems from backup.

C) To limit the scope and magnitude of the incident and prevent it from spreading.

D) To write a report detailing how the breach occurred.

**Answer:** Option **C**

**Explanation:**

Once a security breach is identified, the immediate next step is Containment. The goal is to isolate the affected systems or network segments to prevent the threat (e.g., a spreading worm or ransomware) from damaging further assets.
