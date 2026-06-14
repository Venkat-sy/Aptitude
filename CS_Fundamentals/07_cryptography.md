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

8. What is a major disadvantage of Symmetric Key Cryptography compared to Asymmetric Key Cryptography?

A) It is much slower.

B) The key distribution problem.

C) It uses more CPU power.

D) It cannot encrypt large files.

**Answer:** Option **B**

**Explanation:**

The biggest challenge with symmetric cryptography is key distribution. The secret key must be shared between the sender and receiver securely before they can communicate. If an attacker intercepts the key during this initial distribution, the entire system is compromised.

---

9. In Asymmetric Cryptography, if Alice wants to send a secret, confidential message to Bob, which key should she use to encrypt the message?

A) Alice's Public Key

B) Alice's Private Key

C) Bob's Public Key

D) Bob's Private Key

**Answer:** Option **C**

**Explanation:**

To ensure confidentiality, Alice must encrypt the message with Bob's Public Key. This guarantees that only Bob (who is the sole possessor of Bob's Private Key) can decrypt and read the message.

---

10. A cryptographic attack that systematically tries every possible key until the correct one is found is called a:

A) Dictionary Attack

B) Man-in-the-Middle Attack

C) Brute-Force Attack

D) Replay Attack

**Answer:** Option **C**

**Explanation:**

A brute-force attack involves exhausting the entire key space by trying every possible combination of a cryptographic key or password until the correct one is found. The effectiveness of this attack depends on the length of the key.

---

11. Which of the following is a widely used hashing algorithm that produces a 256-bit hash value?

A) MD5

B) SHA-1

C) SHA-256

D) RC4

**Answer:** Option **C**

**Explanation:**

SHA-256 (Secure Hash Algorithm 256-bit) is a widely used cryptographic hash function belonging to the SHA-2 family. It deterministically generates a 256-bit (32-byte) signature for a text. MD5 produces a 128-bit hash, and SHA-1 produces a 160-bit hash.

---

12. The process of hiding a secret message within a larger, ordinary-looking file (like an image or audio file) is called:

A) Encryption

B) Hashing

C) Steganography

D) Watermarking

**Answer:** Option **C**

**Explanation:**

Steganography is the practice of concealing a file, message, image, or video within another file, message, image, or video. While cryptography scrambles a message to make it unreadable, steganography hides the very existence of the message.

---

13. What is the block size used by the Advanced Encryption Standard (AES)?

A) 64 bits

B) 128 bits

C) 256 bits

D) 512 bits

**Answer:** Option **B**

**Explanation:**

AES operates on a fixed block size of 128 bits. While it supports three different key lengths (128, 192, and 256 bits), the block size it encrypts at one time is always exactly 128 bits.

---

14. Which cryptographic concept ensures that even if an attacker intercepts the ciphertext, they cannot figure out the original plaintext without the key?

A) Integrity

B) Non-repudiation

C) Confidentiality

D) Availability

**Answer:** Option **C**

**Explanation:**

Confidentiality is the principle that information should only be accessible to authorized parties. Encryption provides confidentiality by transforming plaintext into ciphertext, making it unreadable to anyone without the decryption key.

---

15. What is a "Salt" in the context of password hashing?

A) A secret key used to decrypt the password.

B) A random string of data added to the password before hashing.

C) An algorithm used to compress the password.

D) The process of resetting a forgotten password.

**Answer:** Option **B**

**Explanation:**

A salt is a random string of characters added to a password before it is hashed. This ensures that even if two users have the exact same password, their hashes will be completely different, protecting against rainbow table attacks.

---

16. In the context of digital certificates, what does a Certificate Authority (CA) do?

A) Encrypts all web traffic on the internet.

B) Generates symmetric keys for users.

C) Verifies the identity of entities and issues digital certificates binding their identity to a public key.

D) Stores all private keys securely.

**Answer:** Option **C**

**Explanation:**

A Certificate Authority (CA) is a trusted third-party organization that acts as a notary. It verifies the identity of an individual or organization and issues a digital certificate, which contains the entity's public key and is digitally signed by the CA.

---

17. An attacker intercepts an encrypted message and its hash. They alter the message and compute a new hash, sending both to the receiver. To prevent this, what should be used instead of a standard hash?

A) A larger key size

B) Asymmetric encryption

C) Message Authentication Code (MAC)

D) Steganography

**Answer:** Option **C**

**Explanation:**

A MAC is similar to a hash, but it uses a shared secret key. Because the attacker does not possess the secret key, they cannot generate a valid MAC for the altered message. The receiver will compute the MAC using the shared key and realize it doesn't match the received MAC, thus detecting the tampering.

---

18. Which attack involves an attacker secretly relaying and possibly altering the communications between two parties who believe they are directly communicating with each other?

A) Denial of Service (DoS)

B) Man-in-the-Middle (MitM)

C) Brute-Force

D) Phishing

**Answer:** Option **B**

**Explanation:**

In a Man-in-the-Middle (MitM) attack, the attacker intercepts the communication channel between two parties. The attacker can eavesdrop on the conversation or even inject false messages, while both victims believe they are talking securely to one another.

---

19. Which of the following is considered an older, broken hash function that should no longer be used for secure applications due to collision vulnerabilities?

A) SHA-256

B) SHA-3

C) MD5

D) AES

**Answer:** Option **C**

**Explanation:**

MD5 (Message-Digest algorithm 5) is a widely used but fundamentally broken hash function. Researchers have demonstrated how to easily generate collisions (two different inputs producing the same MD5 hash), making it unsuitable for security-critical tasks like digital signatures.

---

20. The Diffie-Hellman algorithm is used primarily for:

A) Encrypting massive databases.

B) Generating digital signatures.

C) Securely exchanging cryptographic keys over a public channel.

D) Hashing user passwords.

**Answer:** Option **C**

**Explanation:**

The Diffie-Hellman key exchange is a mathematical method of securely exchanging cryptographic keys over a public channel. It allows two parties that have no prior knowledge of each other to jointly establish a shared secret key, which can then be used for symmetric encryption.
