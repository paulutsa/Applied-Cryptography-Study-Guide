# Week 13 Study Guide
## Course Integration and Applied Cryptography

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐⭐⭐ (Advanced)

---

# 📖 Overview

Congratulations!

Over the past twelve weeks you've built a strong foundation in modern cryptography.

You began with classical ciphers and progressed through modern symmetric encryption, hashing, authentication, public key cryptography, digital certificates, TLS, password security, post-quantum cryptography, and blockchain.

This week is different.

Instead of learning another algorithm, you'll combine everything you've learned to analyze complete cybersecurity systems.

You'll practice thinking like a security engineer by selecting appropriate cryptographic tools, evaluating design decisions, identifying weaknesses, and recommending improvements.

This week focuses on applying cryptographic principles to realistic cybersecurity scenarios.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Select appropriate cryptographic algorithms for different applications.
- Explain why no single algorithm solves every security problem.
- Evaluate complete cryptographic systems.
- Identify weaknesses in cryptographic designs.
- Recommend secure implementation strategies.
- Explain how multiple cryptographic technologies work together.
- Analyze cryptographic tradeoffs.
- Apply course concepts to realistic cybersecurity scenarios.

---

# 🧠 Why This Matters

Professional security engineers rarely invent new cryptographic algorithms.

Instead, they answer questions such as

- Which algorithm should we use?
- How should keys be managed?
- Should we encrypt or hash this information?
- How should certificates be validated?
- How should passwords be stored?
- How should we migrate to post-quantum cryptography?

Success depends on selecting and implementing existing cryptographic tools correctly.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Defense in Depth | Multiple independent security controls working together. |
| Hybrid Cryptography | Combining multiple cryptographic algorithms in one system. |
| Threat Model | Analysis of attackers, assets, and risks. |
| Security Architecture | The overall design of a secure system. |
| Risk Assessment | Evaluating threats and vulnerabilities. |
| Cryptographic Agility | The ability to replace algorithms as standards evolve. |
| Confidentiality | Preventing unauthorized disclosure. |
| Integrity | Detecting unauthorized modification. |
| Authentication | Verifying identity. |
| Nonrepudiation | Preventing a sender from denying an action or message. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Review previous study guides.
2. Watch the recommended videos.
3. Read the assigned references.
4. Work through the AI tutor prompts.
5. Complete the capstone design exercise.
6. Solve the practice scenarios.
7. Complete the Self Check before the final exam.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

https://www.youtube.com/@Computerphile

Review topics:

- AES
- RSA
- Hash Functions
- TLS
- Digital Signatures

Estimated Time: 30 minutes

---

### 2. NIST Computer Security Resource Center

https://csrc.nist.gov

Review

- Cryptographic Standards
- Post-Quantum Cryptography
- Key Management

Estimated Time: 30 minutes

---

### 3. OWASP Cheat Sheets

https://cheatsheetseries.owasp.org/

Review

- Cryptographic Storage
- Password Storage
- Secrets Management

Estimated Time: 30 minutes

---

# 🤖 AI Tutor Prompts

## Design a Secure System

```text
You are a senior cybersecurity architect.

Design a secure online banking system.

Explain where each of the following technologies should be used and why.

- AES
- HMAC
- SHA-256
- Argon2
- TLS
- Digital Certificates
- RSA or ML-KEM
- Hardware Security Modules

Justify every design decision.
```

---

## Analyze a Security Architecture

```text
Pretend you are reviewing a company's security architecture.

Identify weaknesses.

Recommend improvements.

Explain every recommendation using concepts learned in Applied Cryptography.
```

---

## Build a Threat Model

```text
Create a threat model for an online shopping website.

Identify

- assets
- attackers
- threats
- cryptographic protections

Explain why each protection was selected.
```

---

## Final Exam Review

```text
Ask me twenty comprehensive questions covering every major topic from this course.

Mix conceptual questions with realistic cybersecurity scenarios.

Only ask one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose you're designing a secure online banking application.

A possible design might include:

| Security Requirement | Recommended Technology |
|----------------------|------------------------|
| Secure communication | TLS 1.3 |
| Data encryption | AES-256-GCM |
| Password storage | Argon2 |
| File integrity | SHA-256 |
| API authentication | HMAC |
| Digital identity | X.509 Certificates |
| Secure key storage | Hardware Security Module |
| Future migration | Hybrid Classical + Post-Quantum Cryptography |

Notice that no single algorithm provides complete security.

Instead, secure systems combine multiple cryptographic technologies.

---

# 💻 Python Exercise

Design a simple secure application architecture.

Create a diagram showing where you would use

- AES
- SHA-256
- Argon2
- TLS
- HMAC
- Digital Certificates

Write a short explanation describing why each technology was selected.

Bonus Challenge

Identify one improvement that prepares the application for future post-quantum migration.

---

# 🧩 Practice Problems

## Easy

Which algorithm would you use to encrypt customer data?

Explain why.

---

## Medium

A company stores passwords using AES.

Explain why this is not recommended.

Recommend a better approach.

---

## Challenge

A healthcare provider needs to

- protect patient records
- authenticate users
- secure communications
- verify software updates
- prepare for future quantum threats

Design a cryptographic architecture using concepts learned throughout the course.

Justify every design decision.

---

# 🛡 Think Like a Security Architect

Consider these questions.

- Which cryptographic technologies solve confidentiality?
- Which provide integrity?
- Which provide authentication?
- Which protect passwords?
- Which establish trust?
- Which manage keys?
- Which technologies require future post-quantum migration?
- How do these technologies work together?

---

# ⚠ Common Mistakes

❌ One cryptographic algorithm solves every security problem.

✔ Secure systems combine multiple cryptographic technologies.

---

❌ The strongest algorithm always produces the most secure system.

✔ Security depends on correct implementation, key management, and system design.

---

❌ Cryptography eliminates all cyber risk.

✔ Cryptography is one important component of a comprehensive cybersecurity strategy.

---

❌ Security design ends after deployment.

✔ Secure systems require monitoring, maintenance, updates, and periodic reassessment.

---

# 🌎 Real World Connections

The concepts you've learned apply directly to

- Banking
- Healthcare
- Government
- Cloud Computing
- Mobile Applications
- Secure Messaging
- Software Development
- Critical Infrastructure
- Artificial Intelligence Systems
- Internet of Things (IoT)

Modern cybersecurity professionals combine these technologies every day to protect systems, users, and data.

---

# ✅ Self Check

Before taking the final exam, make sure you can confidently answer these questions without looking at your notes.

- When should encryption be used?
- When should hashing be used?
- When should HMAC be used?
- When should digital signatures be used?
- Why is TLS important?
- Why are digital certificates necessary?
- Why is key management critical?
- Why are passwords hashed instead of encrypted?
- Why is post-quantum cryptography important?
- How do all of these technologies work together to secure modern systems?

---

# 🎓 Course Reflection

You began this course by learning how simple ciphers protected handwritten messages.

You finish the course understanding how modern cryptographic systems protect global communications, financial transactions, cloud services, software updates, healthcare records, and critical infrastructure.

Cryptography continues to evolve, but the principles you've learned throughout this course provide a strong foundation for future study and professional practice.

Congratulations on completing Applied Cryptography!