# Network Security

## Part 1: Quick Short Notes (Fundamentals)

### 1. Network Security Fundamentals
*   **Definition:** Policies and practices adopted to prevent and monitor unauthorized access, misuse, modification, or denial of a computer network and network-accessible resources.

### 2. Firewalls
*   **Concept:** A network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules. It acts as a barrier between a trusted internal network and an untrusted external network (like the Internet).
*   **Types:**
    *   *Packet Filtering:* Inspects individual packets (IP addresses, ports) and allows/blocks based on rules. Fast but basic. Operates at Network Layer.
    *   *Stateful Inspection:* Tracks the operating state and characteristics of network connections. More secure. Operates at Transport Layer.
    *   *Proxy/Application Level Gateway:* Acts as an intermediary, inspecting application-level data (e.g., HTTP traffic). High security but slower.

### 3. IDS & IPS
*   **IDS (Intrusion Detection System):** A passive system that monitors network traffic for malicious activity or policy violations and generates alerts. It *detects* but does not block.
*   **IPS (Intrusion Prevention System):** An active system placed in-line with the traffic. It monitors, detects, and automatically takes action to *block* or prevent the malicious activity.
*   **Detection Methods:**
    *   *Signature-based:* Compares traffic against a database of known attack patterns (like antivirus).
    *   *Anomaly-based:* Establishes a baseline of normal behavior and alerts on deviations (good for zero-day attacks).

### 4. VPN (Virtual Private Network)
*   **Concept:** Extends a private network across a public network (the Internet), allowing users to send and receive data securely as if their devices were directly connected to the private network.
*   **Mechanism:** Uses "Tunneling" to encapsulate data packets, and Encryption (like IPsec or OpenVPN) to ensure the data cannot be read if intercepted.
*   **Use Case:** Secure remote access for employees, masking IP addresses for privacy.

### 5. Authentication & Authorization
*   **Authentication:** Verifying the identity of a user or device (Who are you?).
    *   *Factors:* Something you know (Password), Something you have (Smart Card/OTP token), Something you are (Biometrics - Fingerprint).
    *   *MFA (Multi-Factor Authentication):* Using two or more of the above factors.
*   **Authorization:** Determining what an authenticated user is allowed to do or access (What are you allowed to do?).
    *   *Example:* User logs in (Authentication), but gets a "Permission Denied" error when trying to delete a file (Authorization).

---

## Part 2: Placement-Related MCQs

1. What is the primary function of a network firewall?

A) To increase the speed of the internet connection.

B) To act as a barrier to control incoming and outgoing traffic based on security rules.

C) To automatically assign IP addresses to devices on the network.

D) To encrypt all data stored on the local hard drive.

**Answer:** Option **B**

**Explanation:**

A firewall establishes a barrier between a secured, trusted internal network and an outside, untrusted network. It monitors and filters traffic based on an organization's previously established security policies.

---

2. Which type of firewall tracks the state of active network connections and makes decisions based on the context of the traffic?

A) Packet Filtering Firewall

B) Stateful Inspection Firewall

C) Proxy Firewall

D) Application-Level Gateway

**Answer:** Option **B**

**Explanation:**

Stateful inspection firewalls (also known as dynamic packet filtering) keep track of the state of network connections (such as TCP streams) traveling across it. They make filtering decisions based not only on rules but also on the context established by prior packets in the connection.

---

3. What is the key difference between an IDS (Intrusion Detection System) and an IPS (Intrusion Prevention System)?

A) IDS is hardware, IPS is software.

B) IDS encrypts data, IPS decrypts data.

C) IDS only monitors and alerts, whereas IPS monitors and actively blocks malicious traffic.

D) IDS operates on the internet, IPS operates on the local network.

**Answer:** Option **C**

**Explanation:**

An IDS is a passive monitoring system that triggers alerts when it detects suspicious activity. An IPS is an active control system that sits inline with traffic and can proactively drop malicious packets or block IP addresses to prevent the attack from succeeding.

---

4. Which IDS detection method is best suited for identifying new, unknown "zero-day" attacks?

A) Signature-based detection

B) Anomaly-based detection

C) Policy-based detection

D) Protocol-based detection

**Answer:** Option **B**

**Explanation:**

Anomaly-based detection establishes a baseline of "normal" network behavior. If traffic deviates significantly from this baseline, it flags it as an anomaly. Because it doesn't rely on known signatures, it can detect entirely new, previously unseen attacks (zero-day exploits).

---

5. A VPN (Virtual Private Network) primarily ensures data security across a public network by utilizing which two techniques?

A) Compression and Hashing

B) Tunneling and Encryption

C) Routing and Switching

D) Authentication and Authorization

**Answer:** Option **B**

**Explanation:**

A VPN creates a secure connection over a public network by "Tunneling" (encapsulating original packets inside new packets to hide routing info) and applying strong "Encryption" to the payload so that intercepted data remains unreadable.

---

6. In the context of access control, which of the following best describes "Authorization"?

A) Verifying that the user providing the password is the true owner of the account.

B) Asking the user for a fingerprint scan after they enter a password.

C) Determining whether the successfully logged-in user has the rights to access a specific file.

D) Encrypting the user's password before storing it in the database.

**Answer:** Option **C**

**Explanation:**

Authentication verifies *identity* (who the user is), whereas Authorization determines *access rights* (what the user is permitted to do). Checking if a logged-in user can access or modify a specific file is an authorization process.

---

7. Using a password alongside an SMS one-time password (OTP) is an example of:

A) Single Sign-On (SSO)

B) Biometric Authentication

C) Multi-Factor Authentication (MFA)

D) Authorization

**Answer:** Option **C**

**Explanation:**

Multi-Factor Authentication (MFA) requires the user to provide two or more verification factors to gain access. In this case, it combines "something you know" (password) with "something you have" (the mobile device receiving the OTP).

---
