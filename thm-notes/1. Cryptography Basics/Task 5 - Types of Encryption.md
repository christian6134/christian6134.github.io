# Task 5 - Types of Encryption

## Learning Objectives
- Understand the two main types of encryption: symmetric and asymmetric
- Learn symmetric encryption characteristics and examples
- Master asymmetric encryption principles and applications
- Compare performance and security characteristics
- Identify appropriate encryption types for different scenarios

## Overview
Modern cryptography uses two primary types of encryption: symmetric and asymmetric. Understanding the differences, advantages, and use cases of each type is essential for implementing effective cryptographic systems and choosing appropriate security solutions.

### Two Main Types of Encryption

**Primary Categories**
- **Symmetric Encryption**: Same key for encryption and decryption
- **Asymmetric Encryption**: Different keys for encryption and decryption
- Each type has distinct characteristics and applications
- Often used together in hybrid systems

### Symmetric Encryption

**Definition**
- **Uses the same key to encrypt and decrypt data**
- Also known as **symmetric cryptography**
- Called **private key cryptography**
- Key must be kept secret for security

**Key Characteristics**
- **Same Key**: Single key used for both operations
- **Key Secrecy**: Keeping the key secret is essential
- **Secure Channel**: Communicating key requires secure communication channel
- **Fast Performance**: Efficient for bulk data encryption

**Symmetric Encryption Examples**

**Data Encryption Standard (DES)**
- Adopted in 1977
- Uses 56-bit key
- **Broken in less than 24 hours** → led to 3DES
- Deprecated due to insufficient security

**Triple DES (3DES)**
- DES applied three times
- Key size = 168 bits
- More secure than original DES
- Replaced by AES in modern systems

**Advanced Encryption Standard (AES)**
- Adopted in 2001
- Key sizes: 128, 192, or 256 bits
- Current standard for symmetric encryption
- Widely used in modern applications

### Asymmetric Encryption

**Definition**
- **Uses a pair of keys**: one to encrypt (public), one to decrypt (private)
- Also called **public key cryptography**
- Different keys for encryption and decryption operations
- Based on mathematical relationships between keys

**Key Characteristics**
- **Public Key**: Used for encryption, can be shared openly
- **Private Key**: Used for decryption, must remain secret
- **Mathematical Problems**: Based on problems easy to compute in one direction but difficult to reverse
- **Slower Performance**: More computationally intensive than symmetric

**Asymmetric Encryption Examples**
- **RSA**: Rivest-Shamir-Adleman algorithm
- **Diffie-Hellman**: Key exchange protocol
- **Elliptic Curve Cryptography (ECC)**: Modern alternative to RSA

**Key Sizes**
- **RSA**: 2048-bit, 3072-bit, and 4096-bit keys
- **ECC**: Smaller keys with equivalent security
- **Larger Keys**: Required for mathematical security

### Encryption Process Comparison

**Symmetric Encryption Process**
1. Generate single secret key
2. Share key securely with recipient
3. Encrypt data with secret key
4. Decrypt data with same secret key

**Asymmetric Encryption Process**
1. Generate key pair (public and private)
2. Share public key openly
3. Encrypt data with public key
4. Decrypt data with private key

### Performance Characteristics

**Symmetric Encryption**
- **Faster**: Efficient algorithms and smaller keys
- **Lower Resource Usage**: Less computational overhead
- **Bulk Data**: Suitable for large amounts of data
- **Stream Processing**: Can encrypt data in real-time

**Asymmetric Encryption**
- **Slower**: More complex mathematical operations
- **Higher Resource Usage**: Greater computational requirements
- **Key Exchange**: Ideal for secure key distribution
- **Digital Signatures**: Enables authentication and non-repudiation

### Practical Applications

**Symmetric Encryption Use Cases**
- **Bulk Data Encryption**: Files, databases, disk encryption
- **Stream Encryption**: Real-time communication
- **Session Keys**: Temporary keys for communication
- **Performance-Critical Applications**: High-speed data processing

**Asymmetric Encryption Use Cases**
- **Key Exchange**: Secure distribution of symmetric keys
- **Digital Signatures**: Authentication and integrity verification
- **Certificate Authorities**: PKI infrastructure
- **Secure Email**: PGP and S/MIME implementations

### Hybrid Systems

**Combining Both Types**
- Use asymmetric encryption for key exchange
- Use symmetric encryption for bulk data
- Best of both approaches
- Common in modern cryptographic protocols

**Example: TLS/SSL**
1. Asymmetric encryption establishes secure connection
2. Symmetric keys exchanged securely
3. Bulk data encrypted with symmetric keys
4. Combines security and performance

## Best Practices
- Use symmetric encryption for bulk data and performance-critical applications
- Use asymmetric encryption for key exchange and digital signatures
- Implement hybrid systems for optimal security and performance
- Choose appropriate key sizes for security requirements
- Stay updated with cryptographic standards and recommendations