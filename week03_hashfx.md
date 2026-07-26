# Week 3 Study Guide
## Cryptographic Hash Functions

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐☆☆☆ (Beginning to Intermediate)

---

# 📖 Overview

Last week you learned how AES protects confidential information by encrypting it.

This week you'll study cryptographic hash functions, which solve an entirely different problem.

A hash function does **not** encrypt information.

Instead, it creates a unique digital fingerprint that allows us to verify whether information has changed.

Hash functions are used everywhere, including:

- Password storage
- Software downloads
- Git
- Digital signatures
- Blockchain
- File integrity verification

By the end of this week you'll understand why hash functions are one of the most important building blocks in cybersecurity.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain what a cryptographic hash function is.
- Describe the properties of a secure hash function.
- Explain why hashing is one way.
- Compare encryption and hashing.
- Describe collision resistance.
- Explain the birthday paradox.
- Describe SHA-256 at a high level.
- Explain how hashes verify file integrity.

---

# 🧠 Why This Matters

Suppose you download Linux, Python, or Wireshark from the Internet.

How do you know the file hasn't been modified?

How does Git detect that a file changed?

How does your operating system verify updates?

The answer is cryptographic hash functions.

Instead of comparing entire files, computers compare small digital fingerprints.

If even one bit changes, the hash changes dramatically.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Hash Function | Produces a fixed length fingerprint from any input. |
| Digest | The output of a hash function. |
| SHA-256 | A widely used cryptographic hash function. |
| Collision | Two different inputs producing the same hash. |
| Collision Resistance | Difficulty of finding collisions. |
| Avalanche Effect | Small input changes create completely different outputs. |
| Preimage Resistance | Difficult to recover the original input from a hash. |
| Second Preimage Resistance | Difficult to find another input with the same hash. |
| Salt | Random data added before hashing passwords. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the introductory references.
3. Explore hashing interactively.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**Hashing Algorithms and SHA-256**

https://www.youtube.com/@Computerphile

Search:

- SHA-256
- Cryptographic Hash Functions

Focus

- One-way functions
- Avalanche effect
- Integrity

Estimated Time: 20 minutes

---

### 2. Computerphile

**Password Hashing**

https://www.youtube.com/@Computerphile

Search:

- Password Hashing

Focus

- Why passwords are hashed
- Salting
- Offline attacks

Estimated Time: 15 minutes

---

### 3. Practical Networking

**Hashing vs Encryption**

https://www.youtube.com/@PracticalNetworking

Focus

- When to hash
- When to encrypt
- Real-world applications

Estimated Time: 15 minutes

---

## 📖 Read

### NIST Secure Hash Standard

https://csrc.nist.gov/publications/detail/fips/180/4/final

Read

- Introduction
- Purpose of SHA

Do not worry about the mathematical details.

---

## 🧪 Explore

### CryptoHack

https://cryptohack.org

Recommended Topics

- Hash Functions
- SHA-256
- Collisions

---

# 🤖 AI Tutor Prompts

## Understand Hashing

```text
You are an expert cryptography professor.

Assume I understand AES but know nothing about hash functions.

Explain why hashing exists.

Compare hashing and encryption using several real-world examples.

Do not discuss mathematics until I understand the purpose of hashing.
```

---

## Learn SHA-256

```text
Teach SHA-256 from the beginning.

Explain:

- message blocks
- padding
- compression
- avalanche effect

Use a very small example.

Do not skip intermediate reasoning.
```

---

## Understand Collisions

```text
Explain collision resistance using simple examples.

Then explain why the birthday paradox makes collisions more likely than most people expect.

Use visual examples instead of equations.
```

---

## Quiz Me

```text
Ask me ten questions about cryptographic hash functions.

Only ask one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose the file

```
report.pdf
```

produces

```
9f86d081884c7d659...
```

Now suppose one letter changes.

The new hash becomes

```
34d0ab1f9e8b55...
```

Although the files look nearly identical, their hashes are completely different.

This is called the **avalanche effect**.

---

# 💻 Python Exercise

Write a Python program that

- accepts a filename
- calculates its SHA-256 hash
- displays the hash

Bonus Challenge

Compare two files and determine whether they are identical by comparing their hashes.

---

# 🧩 Practice Problems

## Easy

Why can't a hash be decrypted?

---

## Medium

Explain why downloading
