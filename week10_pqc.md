# Week 10 Study Guide
## Post Quantum Cryptography

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐⭐☆ (Intermediate to Advanced)

---

# 📖 Overview

Throughout this course you've learned how modern cryptography protects data using algorithms such as AES, RSA, Diffie-Hellman, SHA-256, and TLS.

Today these algorithms secure nearly every online transaction.

But what happens if computers become dramatically more powerful?

Researchers believe that sufficiently large quantum computers could solve certain mathematical problems much faster than today's computers. This creates a serious challenge for many public key cryptography algorithms currently used on the Internet.

This week you'll learn why quantum computing matters to cybersecurity, which algorithms are vulnerable, and how new post-quantum cryptographic algorithms are being standardized to prepare for the future.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain why quantum computing affects cryptography.
- Describe Shor's Algorithm.
- Describe Grover's Algorithm.
- Explain why RSA and Diffie-Hellman are vulnerable.
- Explain why AES and SHA-256 are less affected.
- Describe Post-Quantum Cryptography (PQC).
- Explain the purpose of ML-KEM (formerly Kyber).
- Explain the purpose of ML-DSA (formerly Dilithium).
- Describe hybrid cryptographic migration strategies.

---

# 🧠 Why This Matters

Many organizations encrypt sensitive information that must remain confidential for decades.

Examples include

- Medical records
- Government documents
- Military communications
- Financial records
- Research data

An attacker could intercept encrypted information today and store it.

If a sufficiently powerful quantum computer becomes available in the future, the attacker might decrypt that information.

This is sometimes called **"Harvest Now, Decrypt Later."**

For this reason, governments and industry are already transitioning toward post-quantum cryptography.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Quantum Computing | A computing model that uses quantum mechanical principles. |
| Qubit | The basic unit of information in a quantum computer. |
| Shor's Algorithm | A quantum algorithm that efficiently factors large integers. |
| Grover's Algorithm | A quantum search algorithm that speeds up brute force searching. |
| Post-Quantum Cryptography (PQC) | Cryptographic algorithms designed to resist quantum attacks. |
| ML-KEM | NIST's standardized key encapsulation mechanism based on lattice cryptography. |
| ML-DSA | NIST's standardized digital signature algorithm based on lattice cryptography. |
| Hybrid Cryptography | Combining classical and post-quantum algorithms during migration. |
| Harvest Now, Decrypt Later | Collecting encrypted data today with the goal of decrypting it in the future. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the NIST overview.
3. Explore current post-quantum standards.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**Quantum Computing and Cryptography**

https://www.youtube.com/@Computerphile

Search

- Quantum Cryptography
- Shor's Algorithm
- Post Quantum Cryptography

Focus

- Why RSA is vulnerable
- Quantum threats
- Future cryptography

Estimated Time: 20 minutes

---

### 2. MinutePhysics

**Quantum Computing**

https://www.youtube.com/@MinutePhysics

Search

- Quantum Computing

Focus

- Qubits
- Superposition
- Why quantum computers are different

Estimated Time: 15 minutes

---

### 3. NIST

**Post-Quantum Cryptography Project**

https://csrc.nist.gov/projects/post-quantum-cryptography

Focus

- Standardization
- ML-KEM
- ML-DSA
- Migration guidance

Estimated Time: 20 minutes

---

## 📖 Read

### NIST Post-Quantum Cryptography Project

https://csrc.nist.gov/projects/post-quantum-cryptography

Read

- Project Overview
- Standardized Algorithms
- Frequently Asked Questions

---

## 🧪 Explore

Visit

https://pqc-forum.org/

Explore current discussions about post-quantum cryptography and algorithm development.

---

# 🤖 AI Tutor Prompts

## Why Does Quantum Computing Matter?

```text
You are an expert cryptography professor.

Assume I understand RSA, AES, and SHA-256.

Explain why quantum computers threaten some cryptographic algorithms but not others.

Avoid advanced physics.

Use simple analogies only when necessary.
```

---

## Learn Shor's Algorithm

```text
Explain Shor's Algorithm at a conceptual level.

Focus on

- factoring
- RSA
- why this algorithm is important

Do not assume any background in quantum mechanics.
```

---

## Compare Classical and Post-Quantum Cryptography

```text
Create a comparison table showing

- RSA
- Diffie-Hellman
- AES
- SHA-256
- ML-KEM
- ML-DSA

Explain which are vulnerable to quantum attacks and why.
```

---

## Quiz Me

```text
Ask me ten questions about post-quantum cryptography.

Ask only one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Today

A browser uses

- TLS
- RSA or Elliptic Curve Cryptography
- AES

Future

The browser may instead use

- TLS
- ML-KEM
- AES

Notice that AES remains part of the secure connection.

The public key algorithm changes, while the symmetric encryption algorithm continues protecting application data.

---

# 💻 Python Exercise

Research Python libraries that support post-quantum cryptography.

Create a short report describing

- available libraries
- supported algorithms
- current limitations

Bonus Challenge

Build a comparison table showing the public key size, ciphertext size, and intended use of ML-KEM and RSA.

---

# 🧩 Practice Problems

## Easy

Why are RSA and Diffie-Hellman vulnerable to sufficiently powerful quantum computers?

---

## Medium

Explain why AES is still considered secure, even in a future with quantum computers.

---

## Challenge

An organization stores classified information that must remain confidential for the next 40 years.

Recommend a migration strategy that reduces future quantum risk.

---

# 🛡 Think Like an Attacker

Consider these questions.

- Why would attackers collect encrypted traffic today?
- What is "Harvest Now, Decrypt Later"?
- Which systems should migrate first?
- Why are hybrid deployments becoming common?

---

# ⚠ Common Mistakes

❌ Quantum computers break every cryptographic algorithm.

✔ They primarily threaten today's public key algorithms.

---

❌ AES becomes useless.

✔ AES remains secure with larger key sizes, although Grover's Algorithm reduces the effective security level.

---

❌ Quantum computers already break RSA on the Internet.

✔ Large-scale cryptographically relevant quantum computers do not currently exist.

---

❌ Post-Quantum Cryptography requires quantum computers.

✔ Post-Quantum Cryptography runs on today's classical computers.

---

# 🌎 Real World Connections

Organizations preparing for post-quantum cryptography include

- NIST
- NSA
- CISA
- Cloud providers
- Financial institutions
- Government agencies
- Healthcare organizations
- Critical infrastructure operators

Many organizations are beginning multi-year migration plans because replacing cryptographic infrastructure takes significant time.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- Why does quantum computing matter to cryptography?
- What does Shor's Algorithm do?
- What does Grover's Algorithm do?
- Why is RSA vulnerable?
- Why is Diffie-Hellman vulnerable?
- Why is AES less affected?
- What is Post-Quantum Cryptography?
- What are ML-KEM and ML-DSA designed to replace?
- What is "Harvest Now, Decrypt Later"?
- Why are hybrid deployments recommended during migration?

---

# 🚀 Looking Ahead

Next week you'll study **Blockchain and Distributed Trust**.

You'll see how cryptographic hash functions, digital signatures, Merkle trees, and consensus mechanisms work together to build distributed systems that can detect tampering and establish trust without relying on a central authority.
