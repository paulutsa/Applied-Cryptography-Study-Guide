# Week 7 Study Guide
## Transport Layer Security (TLS)

**Estimated Study Time:** 5 to 7 hours

**Difficulty:** ⭐⭐⭐⭐☆ (Intermediate to Advanced)

---

# 📖 Overview

Over the past six weeks, you've learned about encryption, hashing, authentication, public key cryptography, and digital certificates.

This week you'll bring everything together by studying **Transport Layer Security (TLS)**, the protocol that secures nearly every HTTPS connection on the Internet.

Whenever you log into Canvas, check your bank account, shop online, or send data through a secure website, TLS is working behind the scenes.

Instead of introducing new cryptographic algorithms, TLS combines everything you've already learned into one secure communication protocol.

By the end of this week, you'll understand how browsers establish secure HTTPS connections and why every step of the TLS handshake is necessary.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the purpose of TLS.
- Describe the TLS handshake.
- Explain how certificates are used during TLS.
- Describe key exchange during a TLS session.
- Explain session keys.
- Describe forward secrecy.
- Explain why TLS combines asymmetric and symmetric cryptography.
- Explain the difference between TLS 1.2 and TLS 1.3.

---

# 🧠 Why This Matters

Every secure website begins with a TLS handshake.

During only a few milliseconds, your browser and a remote server must

- verify identities
- establish trust
- negotiate encryption algorithms
- exchange secret keys
- begin encrypted communication

All without previously knowing each other.

TLS makes secure Internet communication possible.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| TLS | Transport Layer Security |
| HTTPS | HTTP running over TLS |
| Handshake | Initial negotiation before encrypted communication begins |
| Session Key | Temporary symmetric encryption key |
| Cipher Suite | Collection of cryptographic algorithms used during TLS |
| Forward Secrecy | Protection of past sessions even if long-term keys are compromised |
| Client Hello | First message sent by the browser |
| Server Hello | Server response selecting encryption parameters |
| Certificate | Server identity information |
| Key Exchange | Establishing a shared secret |
| Finished Message | Verifies both sides derived the same session keys |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the TLS overview.
3. Explore an HTTPS connection.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Practical Networking

**TLS Handshake**

https://www.youtube.com/@PracticalNetworking

Search:

- TLS Handshake
- HTTPS

Focus

- Browser communication
- Certificates
- Session keys

Estimated Time: 20 minutes

---

### 2. Computerphile

**HTTPS Explained**

https://www.youtube.com/@Computerphile

Search

- HTTPS
- TLS

Focus

- Encryption
- Certificates
- Authentication

Estimated Time: 18 minutes

---

### 3. Practical Networking

**TLS 1.3**

https://www.youtube.com/@PracticalNetworking

Focus

- Improvements over TLS 1.2
- Forward secrecy
- Faster connections

Estimated Time: 15 minutes

---

## 📖 Read

### RFC 8446

TLS Version 1.3

https://www.rfc-editor.org/rfc/rfc8446

Read

- Introduction
- Goals
- Handshake Overview

Do not worry about every packet format.

---

## 🧪 Explore

Visit

https://www.ssllabs.com/ssltest/

Analyze a popular website.

Identify

- TLS Version
- Certificate
- Cipher Suites
- Forward Secrecy

---

# 🤖 AI Tutor Prompts

## Understand TLS

```text
You are an expert cryptography professor.

Assume I understand AES, RSA, HMAC, and PKI.

Explain how all of these technologies work together during a TLS handshake.

Use a simple step-by-step example.

Never skip intermediate reasoning.
```

---

## Learn the TLS Handshake

```text
Walk through one TLS 1.3 handshake.

For every packet explain

- who sent it
- why it was sent
- what cryptography is being used
- what information is now known

Continue until encrypted communication begins.
```

---

## Compare TLS 1.2 and TLS 1.3

```text
Create a comparison table.

Explain

- performance
- security
- forward secrecy
- deprecated algorithms
```

---

## Quiz Me

```text
Ask me ten questions about TLS.

Ask only one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose you visit

```
https://utsa.edu
```

The browser sends

```
Client Hello
```

The server responds

```
Server Hello
```

The server sends

- Certificate
- Public Key

The browser verifies the certificate.

A secure key exchange establishes a shared session key.

Both sides now switch to AES encryption.

From this point forward, all application data is encrypted.

---

# 💻 Python Exercise

Using Python,

Connect to a secure HTTPS website.

Display

- TLS version
- Cipher suite
- Certificate issuer
- Certificate expiration date

Bonus Challenge

Compare two different websites and determine which TLS version each supports.

---

# 🧩 Practice Problems

## Easy

Why doesn't HTTPS encrypt data immediately?

---

## Medium

Explain why AES is used after the TLS handshake instead of RSA.

---

## Challenge

Suppose a browser skips certificate validation.

Explain how an attacker could exploit this weakness.

---

# 🛡 Think Like an Attacker

Consider these questions.

- What happens during a man-in-the-middle attack?
- Why is certificate validation critical?
- Why were older TLS versions deprecated?
- Why is forward secrecy important?

---

# ⚠ Common Mistakes

❌ HTTPS is an encryption algorithm.

✔ HTTPS is a protocol built on TLS.

---

❌ RSA encrypts every HTTPS packet.

✔ RSA or Diffie-Hellman establishes keys.

AES encrypts the application data.

---

❌ Certificates encrypt data.

✔ Certificates establish identity.

---

❌ Once a certificate is valid, no other security checks are needed.

✔ Certificate validation is only one part of TLS.

---

# 🌎 Real World Connections

TLS secures

- Banking websites
- Canvas
- Online shopping
- VPN portals
- Secure APIs
- Email servers
- Healthcare systems
- Cloud services

Nearly every secure Internet connection uses TLS.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- What is TLS?
- What happens during the TLS handshake?
- Why are certificates necessary?
- Why does TLS use both asymmetric and symmetric cryptography?
- What is a session key?
- Why is AES used after the handshake?
- What is forward secrecy?
- What is a cipher suite?
- Why was TLS 1.3 introduced?
- How does TLS protect HTTPS traffic?

---

# 🚀 Looking Ahead

Next week you'll study **Key Management and Secure Key Storage**.

You'll learn that even the strongest cryptographic algorithms become ineffective if secret keys are generated, stored, distributed, or destroyed improperly.

You'll explore key lifecycles, hardware security modules (HSMs), key rotation, and best practices for protecting cryptographic keys throughout their lifetime.
