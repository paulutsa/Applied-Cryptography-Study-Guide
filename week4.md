# Week 4 Study Guide
## Message Authentication Codes (MACs) and HMAC

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐☆☆ (Intermediate)

---

# 📖 Overview

Last week you learned that cryptographic hash functions verify whether data has changed.

This week you'll discover an important limitation.

A hash can tell you **that** a message changed, but it cannot tell you **who created it**.

Suppose someone emails you a file along with its SHA-256 hash.

How do you know an attacker didn't simply replace both the file and the hash?

This week you'll learn how Message Authentication Codes (MACs) solve that problem by combining cryptographic hash functions with a shared secret key.

By the end of this week you'll understand why HMAC protects software updates, cloud APIs, banking systems, and many Internet protocols.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the purpose of message authentication.
- Distinguish between integrity and authentication.
- Explain what a Message Authentication Code (MAC) is.
- Describe how HMAC combines a hash function with a secret key.
- Explain why simply hashing a message is insufficient for authentication.
- Describe replay attacks.
- Explain why HMAC is widely used in secure Internet protocols.

---

# 🧠 Why This Matters

Suppose your bank sends your browser a message.

How can your browser verify that the message actually came from the bank?

How does AWS know an API request really came from you?

How does GitHub verify webhook requests?

The answer is often HMAC.

HMAC allows two parties that already share a secret key to verify both the integrity and authenticity of a message.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Authentication | Verifying the identity of the sender. |
| Integrity | Ensuring information has not changed. |
| MAC | Message Authentication Code. |
| HMAC | Hash-based Message Authentication Code. |
| Shared Secret | A key known only by authorized parties. |
| Secret Key | The key used to generate and verify an HMAC. |
| Replay Attack | Reusing a previously valid message. |
| Nonce | A value used only once to prevent replay attacks. |
| API Key | A credential used to identify an application. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the HMAC overview.
3. Explore HMAC interactively.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Computerphile

**HMAC Explained**

https://www.youtube.com/@Computerphile

Search:

- HMAC
- Message Authentication Codes

Focus

- Why hashes alone are insufficient
- Authentication
- Shared secrets

Estimated Time: 15 minutes

---

### 2. Practical Networking

**Authentication vs Encryption**

https://www.youtube.com/@PracticalNetworking

Focus

- Integrity
- Authentication
- Practical examples

Estimated Time: 15 minutes

---

## 📖 Read

### RFC 2104

HMAC: Keyed-Hashing for Message Authentication

https://www.rfc-editor.org/rfc/rfc2104

Read

- Introduction
- Motivation
- Overview

Do not worry about the implementation details.

---

## 🧪 Explore

### CryptoHack

https://cryptohack.org

Recommended Topics

- Hash Functions
- HMAC
- Authentication

---

# 🤖 AI Tutor Prompts

## Why Do We Need HMAC?

```text
You are an expert cryptography professor.

Assume I understand SHA-256.

Explain why hashing alone cannot authenticate a message.

Use several real-world examples before introducing HMAC.
```

---

## Learn HMAC

```text
Explain HMAC from the beginning.

Show how the secret key is combined with the message.

Do not skip intermediate reasoning.

Avoid advanced mathematics.
```

---

## Compare Hashing and HMAC

```text
Create a comparison table showing:

- SHA-256
- HMAC-SHA256

Explain what each protects.

Show when each should be used.
```

---

## Quiz Me

```text
Ask me ten questions about HMAC.

Ask one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question
```

---

# ✍ Worked Example

Suppose Alice and Bob share the secret key

```
SECRET123
```

Alice sends

```
Transfer $100
```

She computes

```
HMAC(secret key + message)
```

Bob receives the message.

Using the same secret key, Bob calculates the HMAC.

If both HMAC values match,

✔ The message has not changed.

✔ The sender knew the shared secret.

---

# 💻 Python Exercise

Using Python's built-in **hmac** library,

Write a program that

- accepts a message
- accepts a secret key
- generates an H