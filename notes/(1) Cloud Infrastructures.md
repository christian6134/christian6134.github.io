# 3.1.1 Cloud Infrastructures

## Learning Objectives
- Understand cloud service models and shared responsibility
- Explain cloud deployment models and their security implications
- Describe cloud security controls and best practices

## Overview
Cloud infrastructures provide scalable computing resources with different service models and deployment options, each requiring specific security considerations and shared responsibility between cloud providers and customers.

## Cloud Responsibility Matrix
![Cloud Responsibility Matrix](Photos/Cloud-Responsibility-Matrix.png)

### Service Models

#### Infrastructure as a Service (IaaS)
**Provider Responsibilities:**
- Physical infrastructure
- Virtualization layer
- Network infrastructure
- Physical security

**Customer Responsibilities:**
- Operating system security
- Application security
- Data security
- Access management
- Network security configuration

#### Platform as a Service (PaaS)
**Provider Responsibilities:**
- Physical infrastructure
- Virtualization layer
- Operating system
- Runtime environment
- Middleware

**Customer Responsibilities:**
- Application security
- Data security
- Access management
- Application configuration

#### Software as a Service (SaaS)
**Provider Responsibilities:**
- Physical infrastructure
- Virtualization layer
- Operating system
- Runtime environment
- Middleware
- Application
- Data security

**Customer Responsibilities:**
- Access management
- User training
- Data classification
- Compliance requirements

## Cloud Deployment Models

### Public Cloud
**Characteristics:**
- Shared infrastructure
- Multi-tenant environment
- Pay-per-use model
- Scalable resources

**Security Considerations:**
- Data isolation
- Network segmentation
- Access controls
- Compliance requirements

### Private Cloud
**Characteristics:**
- Dedicated infrastructure
- Single-tenant environment
- On-premises or hosted
- Full control

**Security Considerations:**
- Physical security
- Network security
- Access management
- Compliance control

### Hybrid Cloud
**Characteristics:**
- Combination of public and private
- Data and application portability
- Flexible deployment
- Risk management

**Security Considerations:**
- Data flow security
- Network connectivity
- Identity management
- Compliance across environments

### Community Cloud
**Characteristics:**
- Shared by specific organizations
- Common compliance requirements
- Cost sharing
- Collaborative security

**Security Considerations:**
- Shared responsibility
- Data segregation
- Access controls
- Compliance alignment

## Cloud Security Controls

### Identity and Access Management
- Multi-factor authentication
- Single sign-on (SSO)
- Role-based access control (RBAC)
- Privileged access management

### Data Protection
- Encryption at rest and in transit
- Data loss prevention (DLP)
- Backup and recovery
- Data classification

### Network Security
- Virtual private networks (VPN)
- Firewall rules
- Network segmentation
- DDoS protection

### Monitoring and Logging
- Security information and event management (SIEM)
- Cloud access security broker (CASB)
- Audit logging
- Threat detection

## Best Practices
- Implement defense in depth
- Regular security assessments
- Continuous monitoring
- Incident response planning
- Compliance management
- Staff training and awareness