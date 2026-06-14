# Cryptography

## Part 1: Quick Short Notes (Fundamentals)

### 1. Cryptography Fundamentals
*   **Cryptography:** The practice and study of techniques for secure communication in the presence of adversarial behavior.
*   **Plaintext:** The original, readable message.
*   **Ciphertext:** The scrambled, unreadable message.
*   **Encryption:** Converting plaintext to ciphertext.
*   **Decryption:** Converting ciphertext back to plaintext.
*   **Cipher:** An algorithm for performing encryption or decryption.

### 2. Symmetric vs. Asymmetric Key Cryptography
*   **Symmetric Key (Secret Key):** Uses the *same key* for both encryption and decryption. Faster, but key distribution is a major challenge (e.g., DES, AES).
*   **Asymmetric Key (Public Key):** Uses a *pair of keys* - a Public Key (shared with everyone) and a Private Key (kept secret by the owner). Slower, but solves the key distribution problem (e.g., RSA).
    *   *Rule:* If encrypted with A's Public Key, it can only be decrypted with A's Private Key.

### 3. DES & AES (Symmetric)
*   **DES (Data Encryption Standard):** An older symmetric-key algorithm. Uses a 56-bit key and 64-bit block size. It is now considered insecure due to its small key size (vulnerable to brute-force).
*   **AES (Advanced Encryption Standard):** The current standard for symmetric encryption. It is a block cipher that supports block sizes of 128 bits and key sizes of 128, 192, or 256 bits. Highly secure and efficient.

### 4. RSA (Asymmetric)
*   **RSA (Rivest-Shamir-Adleman):** The most widely used asymmetric algorithm.
*   **Mechanism:** Its security relies on the practical difficulty of factoring the product of two large prime numbers. Used for secure data transmission and digital signatures.

### 5. Hash Functions
*   **Definition:** A mathematical algorithm that maps data of arbitrary size to a fixed-size bit string (a hash value or message digest).
*   **Properties:**
    *   *Deterministic:* Same input always yields the same output.
    *   *Fast computation.*
    *   *Pre-image resistance (One-way):* Infeasible to generate the original message from its hash.
    *   *Collision resistance:* Infeasible to find two different messages that produce the same hash.
*   **Use Case:** Data integrity checks, storing passwords securely (e.g., SHA-256, MD5).

### 6. Digital Signatures
*   **Definition:** A mathematical scheme for verifying the authenticity and integrity of a digital message or document.
*   **How it works:**
    1.  Sender creates a hash of the message.
    2.  Sender encrypts the hash with their *Private Key* (this is the signature).
    3.  Receiver decrypts the signature using the Sender's *Public Key* to get the hash.
    4.  Receiver hashes the received message and compares it to the decrypted hash. If they match, the message is authentic and unaltered.
*   **Provides:** Non-repudiation, Authentication, and Integrity. Does *not* provide confidentiality (unless the message itself is also encrypted).

---

## Part 2: Placement-Related MCQs

1. Which of the following cryptographic techniques uses the same key for both encryption and decryption?

A) Asymmetric Key Cryptography

B) Public Key Cryptography

C) Symmetric Key Cryptography

D) Hash Functions

**Answer:** Option **C**

**Explanation:**

Symmetric Key Cryptography (also known as secret-key cryptography) uses a single, shared key to both encrypt the plaintext and decrypt the ciphertext. Both the sender and receiver must possess this secret key.

---

2. Why is the Data Encryption Standard (DES) largely considered insecure today?

A) Its block size is too large.

B) Its 56-bit key size is too short and vulnerable to brute-force attacks.

C) It uses asymmetric encryption which is slow.

D) The algorithm itself has mathematical flaws.

**Answer:** Option **B**

**Explanation:**

DES uses a relatively short 56-bit key. With modern computing power, a 56-bit key space can be searched exhaustively (a brute-force attack) in a very short amount of time, rendering the encryption insecure.

---

3. The security of the RSA algorithm fundamentally relies on the mathematical difficulty of which problem?

A) Calculating discrete logarithms

B) Factoring large prime numbers

C) Solving elliptic curve equations

D) Computing large factorials

**Answer:** Option **B**

**Explanation:**

The RSA algorithm's security is based on the integer factorization problem. Specifically, it is easy to multiply two large prime numbers together, but it is computationally infeasible to factor the resulting large composite number back into its original primes.

---

4. Which of the following is NOT a required property of a cryptographic hash function?

A) It must be a one-way function (pre-image resistance).

B) It must produce a fixed-length output regardless of input size.

C) It must be collision-resistant.

D) It must use a secret key to generate the hash.

**Answer:** Option **D**

**Explanation:**

Hash functions are generally keyless algorithms. They take an input and deterministically produce a fixed-size string (the hash). A hash function that uses a secret key is specifically called a Message Authentication Code (MAC), not a standard hash function.

---

5. In a Digital Signature scheme, what key does the sender use to create the signature?

A) The Sender's Public Key

B) The Sender's Private Key

C) The Receiver's Public Key

D) The Receiver's Private Key

**Answer:** Option **B**

**Explanation:**

To create a digital signature, the sender encrypts the hash of the message using their own Private Key. Because only the sender possesses this private key, it proves that the sender is the one who created the signature (Authentication and Non-repudiation). Anyone can verify it using the sender's Public Key.

---

6. Which of the following algorithms is the current US government standard for symmetric encryption?

A) DES

B) 3DES

C) AES

D) RSA

**Answer:** Option **C**

**Explanation:**

The Advanced Encryption Standard (AES) was established by NIST in 2001 to replace DES. It is a highly secure, fast, block cipher that supports key sizes of 128, 192, and 256 bits, making it the global standard for symmetric encryption.

---

7. Which security service is provided by Digital Signatures but NOT by simple symmetric encryption?

A) Confidentiality

B) Non-repudiation

C) Availability

D) Data compression

**Answer:** Option **B**

**Explanation:**

Non-repudiation ensures that a sender cannot deny having sent a message. Because a digital signature is created using the sender's unique private key, they cannot later claim someone else forged the signature. Symmetric encryption (where both parties share the key) cannot provide this because either party could have created the message.

---
