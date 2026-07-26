# Week 6 Study Guide
## Public Key Infrastructure (PKI) and Digital Certificates

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐⭐☆ (Intermediate)

---

# 📖 Overview

Last week you learned how public key cryptography allows two strangers to establish secure communications.

However, another important problem remains.

Suppose someone sends you a public key and claims it belongs to your bank.

How do you know the key actually belongs to your bank and not to an attacker pretending to be your bank?

This week you'll learn how Public Key Infrastructure (PKI) solves that problem.

You'll discover how digital certificates, Certificate Authorities (CAs), certificate chains, and browser trust stores work together to establish trust on the Internet.

By the end of this week you'll understand why HTTPS works and how your browser decides whether to trust a website.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the purpose of Public Key Infrastructure (PKI).
- Describe the role of Certificate Authorities (CAs).
- Explain what an X.509 certificate contains.
- Describe certificate chains.
- Explain root, intermediate, and server certificates.
- Explain certificate validation.
- Describe certificate revocation.
- Explain why browsers trust certain Certificate Authorities.

---

# 🧠 Why This Matters

Every time you visit a secure website, your browser performs several security checks before displaying the lock icon.

It verifies:

- The certificate was issued by a trusted Certificate Authority.
- The certificate has not expired.
- The certificate matches the website's domain name.
- The certificate has not been revoked.
- Every certificate in the trust chain is valid.

Without PKI, attackers could easily impersonate banks, online stores, or government websites.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| PKI | Public Key Infrastructure. A framework for managing digital certificates and trust. |
| Certificate | A digital document that binds a public key to an identity. |
| X.509 | The standard format used for digital certificates. |
| Certificate Authority (CA) | A trusted organization that issues certificates. |
| Root Certificate | A self-signed certificate trusted by operating systems and browsers. |
| Intermediate CA | A CA whose certificate is signed by a root CA. |
| Server Certificate | The certificate installed on a website or server. |
| Certificate Chain | The sequence of certificates linking a server certificate to a trusted root. |
| Revocation | Invalidating a certificate before it expires. |
| OCSP | Online Certificate Status Protocol used to check certificate status. |
| CRL | Certificate Revocation List. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the PKI overview.
3. Explore certificates in your browser.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. Practical Networking

**Public Key Infrastructure (PKI)**

https://www.youtube.com/@PracticalNetworking

Search:

- PKI
- Certificate Authority
- Digital Certificates

Focus

- Certificate hierarchy
- Browser trust
- Certificate validation

Estimated Time: 20 minutes

---

### 2. Computerphile

**Digital Certificates**

https://www.youtube.com/@Computerphile

Search:

- Digital Certificates
- Certificate Authorities

Focus

- Why certificates exist
- Trust
- Authentication

Estimated Time: 15 minutes

---

### 3. Practical Networking

**TLS Certificate Validation**

https://www.youtube.com/@PracticalNetworking

Focus

- Certificate chains
- Browser validation
- Root certificates

Estimated Time: 15 minutes

---

## 📖 Read

### NIST Computer Security Resource Center

https://csrc.nist.gov

Read

- Public Key Infrastructure Overview
- Certificate Management Concepts

---

### RFC 5280

Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List Profile

https://www.rfc-editor.org/rfc/rfc5280

Read only the Introduction.

---

## 🧪 Explore

Open your browser.

Visit

https://www.google.com

Click the lock icon.

View the certificate.

Identify:

- Organization
- Issuer
- Expiration Date
- Subject
- Public Key

Repeat the process for another secure website.

---

# 🤖 AI Tutor Prompts

## Why Does PKI Exist?

```text
You are an expert cryptography professor.

Assume I understand RSA and Diffie-Hellman.

Explain why public keys alone are not enough.

Show how an attacker could perform a man-in-the-middle attack if digital certificates did not exist.
```

---

## Learn PKI

```text
Teach Public Key Infrastructure from the beginning.

Explain:

- Root CAs
- Intermediate CAs
- Server certificates
- Certificate chains

Use simple diagrams.

Avoid advanced mathematics.
```

---

## Learn Certificate Validation

```text
Pretend you are Google Chrome.

Walk me through every step Chrome performs before displaying the HTTPS lock icon.

Explain every decision.
```

---

## Quiz Me

```text
Ask me ten questions about PKI.

Only ask one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose you visit

```
https://www.example.com
```

Your browser receives the website's certificate.

It checks:

✔ Is the certificate signed by a trusted Certificate Authority?

✔ Has the certificate expired?

✔ Does the domain name match?

✔ Has the certificate been revoked?

If every check succeeds, the browser trusts the website and proceeds with the secure connection.

---

# 💻 Python Exercise

Using Python's **ssl** library,

Write a program that

- connects to a secure website
- retrieves its certificate
- displays

  - issuer
  - subject
  - expiration date

Bonus Challenge

Display the entire certificate chain.

---

# 🧩 Practice Problems

## Easy

Why can't websites simply create their own certificates?

---

## Medium

Explain why browsers trust root Certificate Authorities.

---

## Challenge

Suppose an attacker creates a fake certificate for your bank.

Explain why modern browsers reject the certificate.

---

# 🛡 Think Like an Attacker

Consider these questions.

- What happens if a Certificate Authority is compromised?
- Why do browsers periodically update their trusted root certificates?
- Why are expired certificates dangerous?
- What happens if certificate validation is disabled?

---

# ⚠ Common Mistakes

❌ HTTPS encrypts traffic without certificates.

✔ HTTPS relies on certificates to establish trust before encryption begins.

---

❌ Every certificate is signed by a root CA.

✔ Most server certificates are signed by intermediate Certificate Authorities.

---

❌ A valid certificate guarantees a website is trustworthy.

✔ It verifies identity, not business practices or intentions.

---

❌ Browsers trust every certificate they receive.

✔ Browsers trust only certificates that chain to trusted root Certificate Authorities.

---

# 🌎 Real World Connections

PKI is used throughout modern computing.

Examples include

- HTTPS
- VPNs
- Smart cards
- Secure email (S/MIME)
- Enterprise authentication
- Software code signing
- Mobile device management
- Secure software updates

Without PKI, secure Internet communication at global scale would not be practical.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- What problem does PKI solve?
- What is a digital certificate?
- What is a Certificate Authority?
- What is an X.509 certificate?
- What is a certificate chain?
- Why are intermediate CAs used?
- What happens during certificate validation?
- Why are certificates revoked?
- Why do browsers trust root certificates?
- Why is PKI essential for HTTPS?

---

# 🚀 Looking Ahead

Next week you'll study **Transport Layer Security (TLS)**.

You'll combine everything you've learned so far to understand how browsers establish secure HTTPS connections using certificates, public key cryptography, symmetric encryption, and authentication to protect data transmitted across the Internet.