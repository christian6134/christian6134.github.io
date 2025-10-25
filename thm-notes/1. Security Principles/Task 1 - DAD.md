# Task 1 - DAD

## Learning Objectives
- Understand the DAD Triad as the opposite of the CIA Triad
- Learn how attacks target confidentiality, integrity, and availability
- Recognize real-world examples of disclosure, alteration, and destruction attacks
- Understand the balance required between security principles

## Overview
The DAD Triad represents the three primary attack vectors against information security systems. While the CIA Triad focuses on protecting confidentiality, integrity, and availability, the DAD Triad identifies how these protections can be compromised through disclosure, alteration, and destruction attacks.

### The DAD Triad Components

#### Disclosure
- **Definition:** The opposite of confidentiality - unauthorized access to sensitive information
- **Impact:** Exposure of confidential data to unauthorized parties
- **Examples:** Data breaches, unauthorized data access, information leakage
- **Real-world Scenario:** Healthcare records stolen and published online, violating patient privacy

#### Alteration
- **Definition:** The opposite of integrity - unauthorized modification of data
- **Impact:** Data corruption, unauthorized changes, loss of data accuracy
- **Examples:** Tampering with financial records, modifying system configurations
- **Real-world Scenario:** Patient medical records altered, potentially leading to incorrect treatment

#### Destruction/Denial
- **Definition:** The opposite of availability - making systems or data inaccessible
- **Impact:** Service disruption, data loss, system unavailability
- **Examples:** Ransomware attacks, DDoS attacks, system crashes
- **Real-world Scenario:** Database systems made unavailable, halting facility operations

### Attack Scenarios

#### Healthcare System Example
- **Disclosure Attack:** Medical records stolen and dumped publicly
  - Result: Healthcare provider incurs losses due to privacy violations
- **Alteration Attack:** Patient records modified maliciously
  - Result: Wrong treatment administered, potentially life-threatening
- **Destruction/Denial Attack:** Database systems made unavailable
  - Result: Facility cannot function, patient records inaccessible

### Security Balance
- **Confidentiality vs. Availability:** Extreme confidentiality measures can restrict legitimate access
- **Integrity vs. Availability:** Strict integrity controls may impact system performance
- **Key Principle:** Effective security requires balancing all three CIA principles
- **Implementation:** Security measures should not be so restrictive that they hinder normal operations

## Best Practices
- **Risk Assessment:** Identify potential DAD attack vectors in your systems
- **Defense in Depth:** Implement multiple layers of protection
- **Regular Monitoring:** Continuously monitor for signs of disclosure, alteration, or destruction
- **Incident Response:** Have plans ready to respond to each type of attack
- **Balance Security:** Ensure security measures don't overly restrict legitimate access