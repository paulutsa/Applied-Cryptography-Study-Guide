# Week 2 Study Guide
## Modern Symmetric Encryption

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐☆☆☆ (Beginning to Intermediate)

---

# 📖 Overview

Last week, you learned how classical ciphers such as the Caesar Cipher work and why they fail.

This week, you'll take a major step into modern cryptography by studying the **Advanced Encryption Standard (AES)**, the encryption algorithm that protects online banking, secure messaging, password managers, WiFi, VPNs, and countless other systems.

Unlike classical ciphers, AES was designed using mathematics rather than language. Instead of shifting letters, AES transforms binary data through multiple carefully designed rounds that create confusion and diffusion, making patterns nearly impossible to detect.

By the end of this week, you'll understand why AES has remained the world's encryption standard for more than twenty years.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the difference between symmetric and asymmetric encryption.
- Describe why DES was replaced by AES.
- Explain how AES encrypts fixed-size blocks of data.
- Describe the purpose of confusion and diffusion.
- Identify the four major AES transformations.
- Compare ECB, CBC, CTR, and GCM modes of operation.
- Explain why ECB should almost never be used.
- Describe the purpose of initialization vectors (IVs).

---

# 🧠 Why This Matters

Nearly every secure application you use today relies on AES.

Examples include:

- HTTPS websites
- WiFi (WPA2 and WPA3)
- BitLocker
- FileVault
- Signal
- WhatsApp
- VPNs
- Cloud storage

Learning AES helps you understand how modern systems protect sensitive information at incredible speed while remaining resistant to known attacks.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Symmetric Encryption | The same secret key is used for encryption and decryption. |
| AES | Advanced Encryption Standard. The modern symmetric encryption standard. |
| DES | Data Encryption Standard, the predecessor to AES. |
| Block Cipher | Encrypts fixed-size blocks of data. |
| Round | One repetition of AES transformations. |
| SubBytes | Substitutes every byte using a lookup table called the S-box. |
| ShiftRows | Rotates rows of the AES state matrix. |
| MixColumns | Mixes data mathematically across each column. |
| AddRoundKey | Combines the round key with the data using XOR. |
| Key Expansion | Generates round keys from the original secret key. |
| IV | Initialization Vector used by several encryption modes. |
| ECB | Electronic Codebook Mode. Encrypts blocks independently. |
| CBC | Cipher Block Chaining Mode. Links each block to the previous block. |
| CTR | Counter Mode. Converts AES into a stream cipher. |
| GCM | Galois Counter Mode. Provides both encryption and authentication. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the introductory videos.
2. Read the AES overview.
3. Explore AES interactively.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**AES Explained (Advanced Encryption Standard)**

https://www.youtube.com/watch?v=O4xNJsjtN6E

**Focus**

- Why AES replaced DES
- Block ciphers
- AES rounds
- High level intuition

Estimated Time: 24 minutes

Reference: Computerphile  [oai_citation:0‡YouTube](https://www.youtube.com/watch?v=O4xNJsjtN6E&utm_source=chatgpt.com)

---

### 2. Computerphile

**Modes of Operation**

https://www.youtube.com/watch?v=Rk0NIQfEXBA

**Focus**

- ECB
- CBC
- Why modes matter
- Chaining blocks

Estimated Time: 17 minutes

Reference: Computerphile  [oai_citation:1‡YouTube](https://www.youtube.com/watch?v=Rk0NIQfEXBA&utm_source=chatgpt.com)

---

### 3. Computerphile

**AES GCM**

https://www.youtube.com/watch?v=-fpVv_T4xwA

**Focus**

- Authenticated encryption
- Why GCM is widely used today
- Integrity and confidentiality together

Estimated Time: 18 minutes

Reference: Computerphile  [oai_citation:2‡YouTube](https://www.youtube.com/watch?v=-fpVv_T4xwA&utm_source=chatgpt.com)

---

## 📖 Read

### NIST FIPS 197

Advanced Encryption Standard (AES)

https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.197-upd1.pdf

Read:

- Introduction
- Section 1
- AES overview

Do **not** worry about understanding every mathematical detail yet.

Reference: AES is the U.S. federal encryption standard.  [oai_citation:3‡Wikipedia](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard?utm_source=chatgpt.com)

---

## 🧪 Explore

### CryptoHack

Symmetric Cryptography

https://cryptohack.org/challenges/aes/

Recommended challenges:

- How AES Works
- Keyed Permutations
- Resisting Bruteforce

Don't worry if you cannot solve every challenge yet. The goal is to become familiar with how AES behaves.

Reference: CryptoHack AES challenges.  [oai_citation:4‡CryptoHack](https://cryptohack.org/challenges/aes/?utm_source=chatgpt.com)

---

# 🤖 AI Tutor Prompts

## Learn the Big Picture

```text
You are an expert cryptography professor.

Assume I understand Caesar Cipher but know nothing about modern encryption.

Explain why DES became insecure and why AES replaced it.

Do not discuss mathematics until I understand the motivation behind AES.
```

---

## Learn AES One Round at a Time

```text
Teach me AES using one 16-byte block.

Explain only one round.

Show the state matrix after

- SubBytes
- ShiftRows
- MixColumns
- AddRoundKey

Explain why each transformation exists before moving to the next.
```

---

## Visual Learner

```text
Draw an ASCII diagram showing how AES encrypts one block.

Show every transformation separately.

Explain what changes after each step.
```

---

## Learn Modes of Operation

```text
Compare ECB, CBC, CTR, and GCM.

Use the same plaintext example for all four modes.

Explain the strengths, weaknesses, and common use cases for each.
```

---

## Quiz Me

```text
Ask me ten questions about AES.

Ask only one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question
```

---

# ✍ Worked Example

Suppose you want to encrypt a document.

AES first divides the document into **128-bit (16-byte) blocks**.

Each block passes through multiple rounds of transformation.

Each round performs:

```
Plaintext Block

↓

SubBytes

↓

ShiftRows

↓

MixColumns

↓

AddRoundKey

↓

Ciphertext Block
```

Instead of shifting letters like Caesar Cipher, AES continually mixes and transforms binary data until no recognizable patterns remain.

---

# 💻 Python Exercise

Write a Python program that:

- Reads a text file.
- Splits the file into 16-byte blocks.
- Displays each block in hexadecimal.

**Bonus Challenge**

Use Python's `pycryptodome` library to encrypt the file using AES-128 in CBC mode.

---

# 🧩 Practice Problems

## Easy

Why does AES always encrypt fixed-size blocks?

---

## Medium

Explain why ECB mode reveals patterns in encrypted images.

---

## Challenge

A company encrypts customer records using AES in ECB mode.

Explain why this decision creates a security risk even though AES itself is considered secure.

---

# 🛡 Think Like an Attacker

Consider these questions.

- If AES is secure, why do attacks still occur?
- What mistakes do developers make when using AES?
- Why is using the wrong encryption mode dangerous?
- Why is key management often more difficult than encryption itself?

---

# ⚠ Common Mistakes

❌ AES uses a 256-bit block.

✔ AES always encrypts **128-bit blocks**.

Only the key length changes (128, 192, or 256 bits).

---

❌ AES is broken because researchers publish attacks.

✔ Most published attacks apply only to reduced-round versions or unrealistic scenarios.

---

❌ ECB is secure because it uses AES.

✔ AES is secure.

ECB is usually **not** secure because identical plaintext blocks produce identical ciphertext blocks.

---

❌ CBC provides integrity.

✔ CBC provides confidentiality only.

Integrity requires additional protection such as a MAC or an authenticated mode like GCM.

---

# 🌎 Real World Connections

AES protects data every day.

Examples include:

- Online banking
- Password managers
- BitLocker
- FileVault
- WPA2 and WPA3 WiFi
- VPN tunnels
- HTTPS connections
- Cloud backups

Many modern systems now use **AES-GCM** because it provides both confidentiality and integrity.  [oai_citation:5‡YouTube](https://www.youtube.com/watch?v=-fpVv_T4xwA&utm_source=chatgpt.com)

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- Why was DES replaced?
- What makes AES a symmetric algorithm?
- Why does AES encrypt blocks instead of individual characters?
- What are the four AES transformations?
- What is the purpose of key expansion?
- Why is ECB considered insecure?
- What is an initialization vector?
- When would you choose CBC?
- When would you choose CTR?
- Why is GCM commonly used today?

---

# 🚀 Looking Ahead

Next week you'll study **cryptographic hash functions**.

Unlike encryption, hashing is **one-way**. You'll learn how algorithms such as SHA-256 verify data integrity, protect passwords, and secure technologies such as Git, digital signatures, and blockchain.
