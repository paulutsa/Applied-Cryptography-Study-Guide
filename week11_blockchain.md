# Week 11 Study Guide
## Blockchain and Distributed Trust

**Estimated Study Time:** 4 to 6 hours

**Difficulty:** ⭐⭐⭐⭐☆ (Intermediate to Advanced)

---

# 📖 Overview

Throughout this course, you've learned how cryptography protects confidentiality, integrity, authentication, and trust.

This week you'll explore how these same cryptographic tools can be combined to create distributed systems that detect tampering and allow participants to agree on shared information without relying on a central authority.

Blockchain is one example of this idea.

Rather than trusting a single organization to maintain records, blockchain uses cryptographic hashes, digital signatures, Merkle trees, and consensus mechanisms to make unauthorized changes extremely difficult to hide.

By the end of this week, you'll understand how blockchain uses the cryptographic concepts you've already learned and recognize both its strengths and its limitations.

---

# 🎯 Learning Objectives

After completing this study guide, you should be able to:

- Explain the purpose of blockchain.
- Describe how blocks are connected.
- Explain how cryptographic hash functions protect integrity.
- Describe Merkle trees.
- Explain digital signatures in blockchain.
- Compare public and private blockchains.
- Explain consensus at a high level.
- Describe Proof of Work and Proof of Stake.
- Explain why blockchain does not eliminate the need for trust.

---

# 🧠 Why This Matters

Organizations often need multiple parties to maintain shared records.

Examples include:

- Financial transactions
- Supply chain management
- Digital identity
- Healthcare records
- Software transparency
- Asset tracking

Instead of relying on one central database, blockchain allows multiple participants to maintain synchronized copies of the same ledger while making unauthorized modifications easier to detect.

---

# 📖 Vocabulary

| Term | Definition |
|------|------------|
| Blockchain | A distributed ledger made up of linked blocks. |
| Block | A collection of transactions and related metadata. |
| Distributed Ledger | A database shared among multiple participants. |
| Hash Pointer | A hash linking one block to the previous block. |
| Merkle Tree | A tree structure that efficiently verifies data integrity. |
| Consensus | The process participants use to agree on the next valid block. |
| Proof of Work | A consensus mechanism requiring computational work. |
| Proof of Stake | A consensus mechanism based on validator stake. |
| Digital Signature | Verifies the authenticity of transactions. |
| Node | A computer participating in the blockchain network. |

---

# 🛣 Learning Path

Complete the sections in this order.

1. Watch the recommended videos.
2. Read the blockchain overview.
3. Explore a blockchain explorer.
4. Work through the AI tutor prompts.
5. Study the worked example.
6. Complete the Python exercise.
7. Solve the practice problems.
8. Complete the Self Check before taking the weekly quiz.

---

# 📚 Learn

## 🎥 Watch

### 1. 3Blue1Brown

**But How Does Bitcoin Actually Work?**

https://www.youtube.com/watch?v=bBC-nXj3Ng4

Focus

- Blocks
- Hashes
- Digital signatures
- Distributed ledgers

Estimated Time: 26 minutes

---

### 2. Computerphile

https://www.youtube.com/@Computerphile

Search

- Blockchain
- Bitcoin
- Merkle Trees

Focus

- Blockchain structure
- Hash chaining
- Integrity

Estimated Time: 20 minutes

---

### 3. IBM Technology

https://www.youtube.com/@IBMTechnology

Search

- Blockchain Explained

Focus

- Enterprise blockchain
- Real-world applications
- Distributed trust

Estimated Time: 15 minutes

---

## 📖 Read

### NIST Blockchain Overview

https://csrc.nist.gov/pubs/ir/8202/final

Read

- Executive Summary
- Introduction
- Blockchain Components

Do not worry about implementation details.

---

## 🧪 Explore

Visit

https://www.blockchain.com/explorer

Explore several blocks.

Identify

- Block height
- Previous block hash
- Transactions
- Timestamp

Observe how every block references the previous block.

---

# 🤖 AI Tutor Prompts

## Why Blockchain?

```text
You are an expert cybersecurity professor.

Assume I understand AES, SHA-256, RSA, digital signatures, and TLS.

Explain why blockchain was developed.

Focus on the problem it solves before explaining how it works.
```

---

## Learn Blockchain

```text
Teach blockchain from the beginning.

Explain

- blocks
- hashes
- digital signatures
- Merkle trees
- consensus

Use simple examples.

Avoid cryptocurrency discussions unless necessary.
```

---

## Learn Merkle Trees

```text
Teach Merkle trees step by step.

Explain

- leaf nodes
- parent hashes
- root hash

Show why Merkle trees efficiently verify large collections of data.
```

---

## Quiz Me

```text
Ask me ten questions about blockchain.

Ask only one question at a time.

If I answer incorrectly,

- explain why
- reteach the concept
- ask another similar question.
```

---

# ✍ Worked Example

Suppose Block 25 contains

```
Previous Hash

Transactions

Timestamp

Merkle Root
```

The block's hash becomes

```
A83D92...
```

Block 26 stores

```
Previous Hash = A83D92...
```

If someone modifies Block 25,

its hash changes.

Because Block 26 still references the old hash,

the blockchain immediately detects the modification.

---

# 💻 Python Exercise

Write a Python program that

- creates a simple block
- stores
  - timestamp
  - previous hash
  - data
- calculates the block's SHA-256 hash

Bonus Challenge

Create a chain of five blocks.

Observe how changing one block changes every subsequent hash.

---

# 🧩 Practice Problems

## Easy

Why does each block contain the previous block's hash?

---

## Medium

Explain how Merkle trees reduce the amount of data required to verify transactions.

---

## Challenge

Suppose an attacker modifies an old block in a blockchain.

Explain why changing a single block affects every block that follows.

---

# 🛡 Think Like an Attacker

Consider these questions.

- Why would an attacker attempt a 51% attack?
- Why are digital signatures required?
- Why are consensus mechanisms necessary?
- Why doesn't blockchain guarantee that stored information is true?

---

# ⚠ Common Mistakes

❌ Blockchain encrypts every transaction.

✔ Most public blockchains rely primarily on hashes and digital signatures rather than encryption.

---

❌ Blockchain prevents every type of fraud.

✔ Blockchain helps detect unauthorized modifications but cannot verify that the original data was accurate.

---

❌ Blockchain automatically provides privacy.

✔ Many public blockchains are intentionally transparent.

---

❌ Cryptocurrency and blockchain are the same thing.

✔ Cryptocurrency is one application of blockchain technology.

Blockchain has many other uses.

---

# 🌎 Real World Connections

Blockchain technology is used in

- Cryptocurrency
- Supply chain tracking
- Digital identity
- Smart contracts
- Healthcare record management
- Asset tracking
- Software transparency
- Academic credential verification

Not every application requires blockchain, but it can be valuable when multiple organizations need to maintain a shared, tamper-evident record.

---

# ✅ Self Check

Before taking this week's quiz, make sure you can answer these questions without looking at your notes.

- What problem does blockchain solve?
- How are blocks connected?
- Why are cryptographic hashes important?
- What is a Merkle tree?
- Why are digital signatures required?
- What is consensus?
- How does Proof of Work differ from Proof of Stake?
- Why doesn't blockchain eliminate trust?
- Why does changing one block affect the rest of the chain?
- When is blockchain an appropriate solution?

---

# 🚀 Looking Ahead

Next week you'll study **Secure Protocol Design and Applied Cryptography**.

You'll bring together everything you've learned this semester to analyze real-world cryptographic protocols, identify common implementation mistakes, and evaluate how cryptographic building blocks work together to secure modern systems.
