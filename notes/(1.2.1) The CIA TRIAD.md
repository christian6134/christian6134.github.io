# 1.2.1 CIA Triad

## Learning Objectives
- Understand the three fundamental principles of information security
- Apply CIA Triad concepts to real-world scenarios

## Overview
The CIA Triad represents the three fundamental principles of information security: Confidentiality, Integrity, and Availability. These principles form the foundation of cybersecurity and guide all security measures and controls.

## Combination of Principles
- Fundamentals of Security

![CIA Triad](Photos/CIA-Triad.png)

## Confidentiality
- Prevent disclosure of information to **unauthorized individuals** or systems.
- Certain information should only be known to **certain people**

**Examples:**
- Encryption
- Access controls (restrict access to a certain resource)
- 2FA (need proper authentication credentials)

## Integrity
- Messages can't be modified without detection.
- Data is **stored** and **transferred** as intended
- Any modification to the data would be identified

**Examples:**
- Hashing (Sending Data + Hash) -> Hashing Functions provide integrity
- Digital Signatures (Asymmetrically Encrypted Hash)
- Certificates
  - Combine with a digital signature to verify an individual
- Non-repudiation: Proof of integrity, can be **asserted** to be genuine

## Availability
- Systems / Networks must be up and running
- Information is accessible to authorized users (at your fingertips)
- Redundancy -> Build systems that will always be available

**Examples:**
- Fault Tolerance: System fails? Continues to run
- Patching: Stability, Close Security Holes
