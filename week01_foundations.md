# Week 1 Study Guide
## Foundations and Classical Cryptography

**Estimated Study Time:** 3 to 5 hours

**Difficulty:** ⭐☆☆☆☆ (Introductory)

---

# 📖 Overview

Welcome to Applied Cryptography!

This week introduces the fundamental concepts that appear throughout the rest of the course. Although the encryption methods you'll study are historically simple, they reveal the strengths and weaknesses that shaped modern cryptography.

By the end of this week, you will understand the basic language of cryptography, how simple ciphers work, why they fail, and how attackers exploit their weaknesses.

Don't worry if you've never studied cryptography before. We will build each concept one step at a time.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Define cryptography and explain its primary goals.
- Explain confidentiality, integrity, and availability (CIA).
- Distinguish between plaintext, ciphertext, encryption, and decryption.
- Describe the purpose of a cryptographic key.
- Encrypt and decrypt messages using a Caesar Cipher.
- Explain why frequency analysis breaks simple substitution ciphers.
- Describe Kerckhoffs' Principle.
- Explain why the One Time Pad achieves perfect secrecy.

---

# 🧠 Why This Matters

Every secure technology you use today depends on cryptography.

When you unlock your phone, log into Canvas, shop online, connect to WiFi, or send an encrypted message, cryptographic algorithms are protecting your information behind the scenes.

Modern algorithms such as AES and RSA solve the same basic problem people have faced for centuries:

> **How can two people communicate securely if someone else is listening?**

The ciphers you'll study this week are no longer secure, but they introduce the vocabulary and design principles used throughout modern cryptography.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Plaintext | The original readable message. |
| Ciphertext | The encrypted message. |
| Encryption | Converting plaintext into ciphertext. |
| Decryption | Recovering plaintext from ciphertext. |
| Cipher | An algorithm used to encrypt and decrypt information. |
| Key | A secret value used by the cipher. |
| Key Space | The total number of possible keys. |
| Brute Force Attack | Trying every possible key until the correct one is found. |
| Cryptanalysis | The study of breaking cryptographic systems. |
| Confidentiality | Preventing unauthorized disclosure of information. |
| Integrity | Ensuring information has not been modified. |
| Availability | Ensuring systems remain accessible when needed. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the assigned references.
3. Work through the AI tutor prompts.
4. Study the worked example.
5. Complete the Python exercise.
6. Solve the practice problems.
7. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Khan Academy
**Introduction to Cryptography**

https://www.khanacademy.org/computing/computer-science/cryptography

**Focus**

- Encryption
- Decryption
- Plaintext
- Ciphertext
- Keys

Estimated Time: 15 minutes

---

### 2. Crash Course Computer Science
**Cryptography**

https://www.youtube.com/watch?v=jhXCTbFnK8o

**Focus**

- History of cryptography
- Why encryption exists
- Modern applications

Estimated Time: 12 minutes

---

### 3. Computerphile

https://www.youtube.com/@Computerphile

Search for:

- Caesar Cipher
- Vigenère Cipher
- Frequency Analysis

Estimated Time: 20 minutes

---

## 📖 Read

### Caesar Cipher

https://en.wikipedia.org/wiki/Caesar_cipher

Focus on:

- Shift value
- Key space
- Brute force attacks

---

### Vigenère Cipher

https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher

Focus on:

- Polyalphabetic encryption
- Why it improved on Caesar Cipher

---

### Kerckhoffs' Principle

https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle

Read only the introduction.

---

# 🤖 AI Tutor Prompts

## Learn the Basics

```
You are an expert cryptography professor.

Assume I know only basic algebra.

Teach me Week 1 of Applied Cryptography.

Start with:

• plaintext
• ciphertext
• encryption
• decryption
• keys

Use simple examples.

After every concept, ask me one question before continuing.
```

---

## Learn by Doing

```
Teach me Caesar Cipher one letter at a time.

Encrypt the word

HELLO

using a shift of three.

Explain every letter individually.

Then let me try another message.
```

---

## Think Like the Attacker

```
Pretend I intercepted a Caesar Cipher.

Teach me how to recover the plaintext without knowing the key.

Do not use software.

Show every step manually using frequency analysis.
```

---

## Quiz Me

```
Ask me ten questions about Week 1.

Only ask one question at a time.

If I answer incorrectly,

• explain why

• reteach the concept

• ask another similar question.
```

---

# ✍ Worked Example

## Caesar Cipher

Plaintext

```
HELLO
```

Key

```
3
```

Encrypt one letter at a time.

```
H → K

E → H

L → O

L → O

O → R
```

Ciphertext

```
KHOOR
```

To decrypt the message, shift every letter three positions backward.

---

# 💻 Python Exercise

Write a Python function that:

- Accepts a message.
- Accepts a shift value.
- Encrypts the message.
- Preserves spaces and punctuation.

**Bonus Challenge**

Write a second function that decrypts the message.

---

# 🧩 Practice Problems

## Easy

Encrypt

```
APPLE
```

using a shift of **4**.

---

## Medium

Decrypt

```
WKH FDW LV VDIH
```

---

## Challenge

Explain why increasing the Caesar Cipher key from **3** to **19** does **not** make it more secure.

---

# 🛡 Think Like an Attacker

Answer these questions.

- How many possible Caesar Cipher keys exist?
- How long would a brute force attack take?
- Why does frequency analysis work?
- Why is English easier to attack than random text?

---

# ⚠ Common Mistakes

❌ Encryption guarantees integrity.

✔ Encryption provides confidentiality. Additional mechanisms are needed to verify integrity.

---

❌ Secret algorithms are more secure.

✔ Modern cryptography assumes attackers know the algorithm. Only the key remains secret.

---

❌ Larger keys always make weak algorithms secure.

✔ A weak algorithm remains weak regardless of key size.

---

# 🌎 Real World Connections

Although Caesar Cipher is no longer used to protect sensitive information, the concepts introduced this week appear everywhere.

Examples include:

- HTTPS
- SSH
- Signal
- WhatsApp
- Password Managers
- VPNs
- Secure WiFi

Modern systems use stronger algorithms, but the terminology and design principles remain the same.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- What is the difference between plaintext and ciphertext?
- What is a cryptographic key?
- What is the purpose of encryption?
- Why does Caesar Cipher fail?
- What is frequency analysis?
- What is Kerckhoffs' Principle?
- What is brute force?
- What is the CIA Triad?
- Why is the One Time Pad considered perfectly secure?

---

# 🚀 Looking Ahead

Next week you will study modern symmetric cryptography.

You will learn how algorithms such as AES replaced classical ciphers and why modern encryption can securely protect everything from online banking to encrypted messaging applications.
