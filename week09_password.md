# Week 9 Study Guide
## Password Security and Password Hashing

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐☆☆ (Intermediate)

---

# 📖 Overview

Every day, billions of people log into websites, mobile apps, and cloud services using passwords.

Have you ever wondered how websites store your password without actually knowing it?

The answer is password hashing.

This week you'll learn why passwords should never be stored in plaintext or encrypted using standard encryption algorithms such as AES.

Instead, modern systems use specialized password hashing algorithms that are intentionally slow and resistant to brute force attacks.

You'll also learn why password breaches occur, how attackers crack stolen password databases, and what developers can do to better protect user credentials.

By the end of this week, you'll understand how modern systems securely store passwords and why password security remains one of the most important areas of cybersecurity.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain why passwords should never be stored in plaintext.
- Describe why passwords are hashed instead of encrypted.
- Explain salting and peppering.
- Compare SHA-256 with password hashing algorithms.
- Explain why bcrypt, PBKDF2, scrypt, and Argon2 are designed to be slow.
- Describe brute force and dictionary attacks.
- Explain credential stuffing.
- Describe password management best practices.

---

# 🧠 Why This Matters

Password breaches happen regularly.

When attackers steal a password database, they usually do not obtain the original passwords.

Instead, they obtain password hashes.

Their goal becomes finding passwords that generate the same hash.

Modern password hashing algorithms intentionally make this process slow and expensive.

Good password storage protects users even after a database has been stolen.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Password Hashing | Converting a password into a one-way hash before storage. |
| Salt | Random data added to every password before hashing. |
| Pepper | A secret value stored separately from the password database. |
| bcrypt | Password hashing algorithm designed to resist brute force attacks. |
| PBKDF2 | Password-based key derivation function. |
| scrypt | Memory-intensive password hashing algorithm. |
| Argon2 | Modern password hashing algorithm and winner of the Password Hashing Competition. |
| Rainbow Table | A precomputed table of password hashes. |
| Credential Stuffing | Reusing stolen passwords on multiple websites. |
| Password Manager | Software that securely stores passwords. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the password hashing overview.
3. Explore password security resources.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**Password Hashing**

https://www.youtube.com/@Computerphile

Search

- Password Hashing
- bcrypt
- Argon2

Focus

- Why passwords are hashed
- Salts
- Slow hashing

Estimated Time: 20 minutes

---

### 2. Computerphile

**How Password Cracking Works**

https://www.youtube.com/@Computerphile

Search

- Password Cracking

Focus

- Brute force
- Dictionary attacks
- Rainbow tables

Estimated Time: 18 minutes

---

### 3. OWASP

**Password Storage Cheat Sheet**

https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html

Focus

- Password storage best practices
- Recommended algorithms
- Salting
- Work factors

Estimated Time: 25 minutes

---

## 📖 Read

### NIST SP 800-63B

Digital Identity Guidelines

https://pages.nist.gov/800-63-4/sp800-63b.html

Read

- Password recommendations
- Memorized secrets
- Password length guidance

Do not worry about every implementation detail.

---

## 🧪 Explore

Visit

https://haveibeenpwned.com/

Read about how password breaches occur and why password reuse is dangerous.

Do not enter your passwords into any website.

---

# 🤖 AI Tutor Prompts

## Why Hash Passwords?

```text
You are an expert cybersecurity professor.

Assume I understand SHA-256.

Explain why websites hash passwords instead of encrypting them.

Use several real-world examples.

Do not discuss bcrypt until I understand why password hashing exists.
```

---

## Learn Password Hashing

```text
Teach password hashing from the beginning.

Explain

- salts
- peppers
- work factors
- bcrypt
- PBKDF2
- scrypt
- Argon2

Compare each algorithm using simple language.

Avoid advanced mathematics.
```

---

## Learn Password Attacks

```text
Explain how attackers crack stolen password databases.

Compare

- brute force attacks
- dictionary attacks
- rainbow tables
- credential stuffing

Explain how each attack works and how defenders reduce the risk.
```

---

## Quiz Me

```text
Ask me ten questions about password security.

Ask only one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose a user creates the password

```
CorrectHorseBatteryStaple
```

The website generates a random salt.

```
Salt = A82F4D91
```

The password and salt are combined.

```
CorrectHorseBatteryStaple + A82F4D91
```

The result is hashed using Argon2.

Only the hash and the salt are stored.

The original password is never stored.

When the user logs in again, the same process is repeated and the hashes are compared.

---

# 💻 Python Exercise

Using Python,

Write a program that

- accepts a password
- generates a random salt
- hashes the password using a password hashing library

Display

- the salt
- the password hash

Bonus Challenge

Verify whether a second password matches the stored hash.

---

# 🧩 Practice Problems

## Easy

Why shouldn't websites store plaintext passwords?

---

## Medium

Explain why two users with the same password should still have different stored password hashes.

---

## Challenge

A company stores user passwords using SHA-256 without salts.

Identify the security weaknesses and recommend a better design.

---

# 🛡 Think Like an Attacker

Consider these questions.

- Why are weak passwords attractive targets?
- Why is password reuse dangerous?
- Why do attackers use dictionaries before brute force attacks?
- Why are password managers recommended?

---

# ⚠ Common Mistakes

❌ Passwords should be encrypted.

✔ Passwords should normally be hashed using specialized password hashing algorithms.

---

❌ SHA-256 is the best password hashing algorithm.

✔ General-purpose hash functions are too fast for password storage.

---

❌ Salts keep passwords secret.

✔ Salts make precomputed attacks and identical password hashes much less effective.

---

❌ Complex passwords are always better than long passwords.

✔ Long, unique passwords or passphrases are generally easier to remember and harder to guess.

---

# 🌎 Real World Connections

Password hashing is used by

- Windows
- Linux
- macOS
- Active Directory
- Password managers
- Banking websites
- Cloud applications
- Social media platforms

Modern organizations combine strong password hashing with multi-factor authentication to improve account security.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- Why are passwords hashed instead of encrypted?
- What is a salt?
- What is a pepper?
- Why is Argon2 recommended?
- Why is SHA-256 not ideal for password storage?
- What is a rainbow table?
- What is credential stuffing?
- Why are password managers useful?
- Why should users avoid password reuse?
- Why are slow hashing algorithms considered more secure for passwords?

---

# 🚀 Looking Ahead

Next week you'll study **Post-Quantum Cryptography**.

You'll explore how quantum computers threaten today's public key cryptography and learn how new algorithms are being developed to protect future communications against quantum attacks.
