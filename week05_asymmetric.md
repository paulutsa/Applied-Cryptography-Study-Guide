# Week 5 Study Guide
## Public Key Cryptography, RSA, and Diffie-Hellman

**Estimated Study Time:** 5 to 7 hours

**Difficulty:** ⭐⭐⭐⭐☆ (Intermediate)

---

# 📖 Overview

Imagine you want to send an encrypted message to someone you've never met.

AES is extremely secure, but it has one important limitation.

Both people must already know the same secret key.

That creates a difficult question:

> **How can two strangers securely exchange a secret key over the Internet without an attacker stealing it?**

This problem remained unsolved until the invention of **public key cryptography**.

This week you'll learn how public and private keys work, why RSA changed the Internet forever, and how Diffie-Hellman allows two strangers to establish a shared secret without ever transmitting that secret across the network.

These ideas form the foundation of HTTPS, SSH, VPNs, secure email, digital certificates, and nearly every secure Internet protocol used today.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the difference between symmetric and asymmetric cryptography.
- Describe why public key cryptography was revolutionary.
- Explain public and private keys.
- Describe RSA at a high level.
- Explain why prime numbers are important.
- Describe modular arithmetic.
- Explain Diffie-Hellman key exchange.
- Compare RSA and Diffie-Hellman.
- Explain why hybrid cryptography is used on the Internet.

---

# 🧠 Why This Matters

Every time you visit a secure website, your browser must establish a secure connection with a server it has never communicated with before.

How is that possible?

Public key cryptography solves this problem.

Without RSA and Diffie-Hellman, secure web browsing, online banking, encrypted messaging, SSH, VPNs, and software updates would not be practical.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Asymmetric Cryptography | Uses separate public and private keys. |
| Public Key | Shared openly with anyone. |
| Private Key | Kept secret by the owner. |
| RSA | Public key algorithm used for encryption and digital signatures. |
| Diffie-Hellman | Key exchange algorithm that establishes a shared secret. |
| Modular Arithmetic | Arithmetic performed using a modulus. |
| Prime Number | A number divisible only by 1 and itself. |
| Euler's Totient | Mathematical function used in RSA key generation. |
| Hybrid Cryptography | Combines public key and symmetric cryptography. |
| Key Exchange | Securely establishing a shared secret. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the introductory references.
3. Explore RSA interactively.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**RSA Encryption**

https://www.youtube.com/@Computerphile

Search:

- RSA
- Public Key Cryptography

Focus

- Public keys
- Private keys
- Why RSA works

Estimated Time: 20 minutes

---

### 2. Computerphile

**Diffie-Hellman Key Exchange**

https://www.youtube.com/@Computerphile

Search:

- Diffie-Hellman

Focus

- Shared secrets
- Key exchange
- Secure communication

Estimated Time: 15 minutes

---

### 3. Khan Academy

**Modular Arithmetic**

https://www.khanacademy.org/computing/computer-science/cryptography

Focus

- Clock arithmetic
- Modulus
- Building intuition

Estimated Time: 20 minutes

---

## 📖 Read

### NIST Cryptographic Standards

https://csrc.nist.gov

Read

- Public Key Cryptography Overview
- Key Establishment Concepts

Do not worry about the mathematical proofs.

---

## 🧪 Explore

### CryptoHack

https://cryptohack.org

Recommended Topics

- RSA
- Diffie-Hellman
- Modular Arithmetic

---

# 🤖 AI Tutor Prompts

## Why Public Key Cryptography?

```text
You are an expert cryptography professor.

Assume I understand AES and HMAC.

Explain why symmetric encryption alone cannot secure the Internet.

Do not discuss mathematics until I understand the key distribution problem.
```

---

## Learn RSA

```text
Teach RSA from the beginning.

Assume I know only basic algebra.

Explain:

- prime numbers
- modular arithmetic
- public keys
- private keys

Use very small numbers.

Show every calculation.

Never skip intermediate reasoning.
```

---

## Learn Diffie-Hellman

```text
Teach Diffie-Hellman using very small numbers.

Show every calculation performed by Alice.

Show every calculation performed by Bob.

Show what Eve observes.

Explain why Eve cannot calculate the shared secret.
```

---

## Compare RSA and Diffie-Hellman

```text
Create a comparison table explaining

- purpose
- strengths
- weaknesses
- performance
- real-world uses

Then explain why HTTPS often uses both.
```

---

## Quiz Me

```text
Ask me ten questions about RSA and Diffie-Hellman.

Only ask one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose Alice wants to communicate securely with Bob.

Bob publishes his **public key**.

Alice downloads Bob's public key and uses it to encrypt a temporary secret.

Only Bob's **private key** can decrypt that secret.

Both computers now share the same AES key.

The remainder of the conversation uses AES because symmetric encryption is much faster than RSA.

This combination is called **hybrid cryptography**.

---

# 💻 Python Exercise

Using Python,

Write a program that

- generates an RSA key pair
- encrypts a short message
- decrypts the message

Bonus Challenge

Use Python's cryptography library to perform a Diffie-Hellman key exchange.

---

# 🧩 Practice Problems

## Easy

Why can't everyone simply share one secret AES key?

---

## Medium

Explain why RSA is much slower than AES.

---

## Challenge

A website encrypts every byte of every HTTPS session using only RSA.

Explain why this would be inefficient.

How does hybrid cryptography solve this problem?

---

# 🛡 Think Like an Attacker

Consider these questions.

- What happens if a private key is stolen?
- Why is randomness critical when generating RSA keys?
- Why are short RSA keys dangerous?
- Why doesn't Diffie-Hellman authenticate the participants?

---

# ⚠ Common Mistakes

❌ RSA replaces AES.

✔ RSA and AES solve different problems.

---

❌ Public keys must remain secret.

✔ Public keys are designed to be shared openly.

---

❌ Diffie-Hellman encrypts messages.

✔ Diffie-Hellman establishes a shared secret.

---

❌ RSA is used to encrypt large files.

✔ RSA is typically used to exchange symmetric keys.

Large amounts of data are encrypted using AES.

---

# 🌎 Real World Connections

Public key cryptography is used in

- HTTPS
- SSH
- VPNs
- Secure email
- Software updates
- Digital signatures
- Certificate Authorities

Almost every secure Internet connection begins with public key cryptography before switching to symmetric encryption.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- Why was public key cryptography invented?
- What problem does RSA solve?
- What problem does Diffie-Hellman solve?
- What is the difference between a public key and a private key?
- Why is modular arithmetic important?
- Why are prime numbers important?
- Why is RSA slower than AES?
- What is hybrid cryptography?
- Why is Diffie-Hellman vulnerable to a man-in-the-middle attack?
- Why does HTTPS use both asymmetric and symmetric cryptography?

---

# 🚀 Looking Ahead

Next week you'll learn about **Public Key Infrastructure (PKI)** and **digital certificates**.

You'll discover how browsers know they are communicating with the real bank instead of an attacker and why Certificate Authorities are essential to Internet security.
