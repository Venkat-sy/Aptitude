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

---

8. What is "Spear Phishing"?

A) A phishing attack sent to millions of random email addresses.

B) A targeted phishing attack aimed at a specific individual or organization.

C) An attack involving physical USB drops.

D) Hacking into a bank's database to steal credit card numbers.

**Answer:** Option **B**

**Explanation:**

Spear phishing is highly targeted. Unlike standard phishing which uses a "spray and pray" approach, spear phishing attackers gather specific information about their target (like their name, job title, or colleagues) to make the fraudulent email appear highly convincing.

---

9. Which type of malware encrypts a user's files and demands a financial payment in exchange for the decryption key?

A) Spyware

B) Adware

C) Ransomware

D) Rootkit

**Answer:** Option **C**

**Explanation:**

Ransomware is a type of malicious software designed to block access to a computer system or files until a sum of money is paid. It typically uses strong encryption so the user cannot recover the files without paying the attacker for the key.

---

10. Maintaining a strict "Chain of Custody" is crucial in which cyber security domain?

A) Penetration Testing

B) Software Development

C) Digital Forensics

D) Firewall Configuration

**Answer:** Option **C**

**Explanation:**

In Digital Forensics, the Chain of Custody is a chronological documentation that records the sequence of custody, control, transfer, analysis, and disposition of physical or electronic evidence. If this chain is broken, the evidence may be deemed inadmissible in a court of law.

---

11. An attacker alters the source IP address of their packets to make it appear as though the traffic is coming from a trusted internal IP. What is this technique called?

A) Phishing

B) IP Spoofing

C) Sniffing

D) SQL Injection

**Answer:** Option **B**

**Explanation:**

IP Spoofing is the creation of IP packets with a forged source IP address, with the purpose of concealing the identity of the sender or impersonating another computing system.

---

12. Which of the following is an example of a Social Engineering attack?

A) Cross-Site Scripting

B) Buffer Overflow

C) Tailgating / Piggybacking

D) Port Scanning

**Answer:** Option **C**

**Explanation:**

Social engineering attacks exploit human psychology rather than technical vulnerabilities. Tailgating (following an authorized person into a secure restricted area without a badge) is a physical social engineering attack.

---

13. What is a "Zero-Day" vulnerability?

A) A vulnerability that has existed for exactly one day.

B) A security flaw that is known to the software vendor but does not yet have a patch available.

C) A virus that wipes the hard drive clean (zeros it out).

D) A flaw in the firewall hardware.

**Answer:** Option **B**

**Explanation:**

A zero-day vulnerability refers to a security hole in software that is unknown to the vendor. Because the vendor has had "zero days" to fix the flaw, no patch exists, making it highly valuable to attackers.

---

14. The practice of testing a computer system, network, or web application to find security vulnerabilities that an attacker could exploit is called:

A) Incident Response

B) Digital Forensics

C) Penetration Testing (Pen Testing)

D) Network Monitoring

**Answer:** Option **C**

**Explanation:**

Penetration testing (or ethical hacking) is an authorized simulated cyberattack on a computer system, performed to evaluate the security of the system. The goal is to identify weaknesses before malicious hackers can exploit them.

---

15. What does CSRF stand for in web security?

A) Cross-Site Request Forgery

B) Client-Server Resource Fetching

C) Cross-Site Routing Firewall

D) Code Security Response Framework

**Answer:** Option **A**

**Explanation:**

Cross-Site Request Forgery (CSRF) is an attack that forces an end user to execute unwanted actions on a web application in which they're currently authenticated. It exploits the trust that a site has in a user's browser.

---

16. What is the primary purpose of a "Keylogger"?

A) To encrypt the hard drive.

B) To generate secure passwords.

C) To secretly record the keystrokes pressed by a user.

D) To unlock encrypted files.

**Answer:** Option **C**

**Explanation:**

A keylogger is a type of spyware that monitors and records every keystroke typed on a specific computer's keyboard. Attackers use it to steal passwords, credit card numbers, and other sensitive data.

---

17. Which of the following best describes the "Eradication" phase in Incident Response?

A) Determining how the attack happened.

B) Restoring systems to normal operation.

C) Removing the malware, attacker access, and vulnerabilities that caused the breach.

D) Writing a final report.

**Answer:** Option **C**

**Explanation:**

Once an incident is contained, the Eradication phase involves identifying the root cause of the incident and removing the threat entirely from the environment. This means deleting malware, disabling breached user accounts, and patching vulnerabilities.

---

18. What is "Whaling" in the context of cyber security?

A) A massive DDoS attack against a large corporation.

B) A highly targeted phishing attack aimed at senior executives (CEOs, CFOs).

C) Stealing large databases of customer information.

D) Using supercomputers to crack encryption keys.

**Answer:** Option **B**

**Explanation:**

Whaling is a specific type of spear phishing attack directed specifically at high-profile and high-level targets within an organization, such as C-level executives. The goal is to trick them into authorizing large wire transfers or giving up highly sensitive company info.

---

19. Which security principle ensures that a user is given only the minimum level of access rights necessary to perform their job?

A) Separation of Duties

B) Defense in Depth

C) Principle of Least Privilege

D) Security through Obscurity

**Answer:** Option **C**

**Explanation:**

The Principle of Least Privilege (PoLP) states that a subject (user, application, process) should be granted only the privileges necessary to complete its required tasks, and no more. This limits the potential damage from accidents or compromised accounts.

---

20. A program that appears to be a legitimate utility but actually contains malicious code is called a:

A) Virus

B) Trojan Horse

C) Worm

D) Logic Bomb

**Answer:** Option **B**

**Explanation:**

A Trojan Horse relies on deceiving the user into installing it by masquerading as a harmless or desirable program (like a game or a tool). Unlike viruses and worms, Trojans do not inject themselves into other files or self-replicate.
