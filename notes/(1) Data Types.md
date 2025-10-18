# 3.3.1 Data Types

## Learning Objectives
- Understand different data classifications and their security requirements
- Explain regulated data and compliance requirements
- Describe intellectual property and trade secret protection
- Identify personal and financial information categories

## Overview
Data classification is essential for implementing appropriate security controls and handling procedures. Different data types require varying levels of protection based on their sensitivity, regulatory requirements, and business impact.

## Data Classification Categories

### Regulated Data
**Definition:** Data managed by third parties under government laws and statutes

**Characteristics:**
- **Government Oversight** - Subject to regulatory compliance
- **Third-Party Management** - Managed by external entities
- **Legal Requirements** - Must comply with specific laws
- **Audit Requirements** - Regular compliance audits

**Examples:**
- **Financial Records** - Banking and investment data
- **Healthcare Data** - Medical records and health information
- **Personal Data** - GDPR, CCPA regulated information
- **Government Records** - Public sector data

### Trade Secrets
**Definition:** Organization's secret formulas and proprietary information

**Characteristics:**
- **Unique to Organization** - Often exclusive to specific companies
- **Competitive Advantage** - Provides business value
- **Confidential Nature** - Must remain secret
- **Legal Protection** - Protected under trade secret laws

**Examples:**
- **Manufacturing Processes** - Production methods and techniques
- **Formulas** - Chemical compositions and recipes
- **Business Strategies** - Marketing and operational plans
- **Customer Lists** - Proprietary customer information

### Intellectual Property
**Definition:** Creative works and inventions with copyright and trademark restrictions

**Characteristics:**
- **Public Visibility** - May be publicly visible
- **Legal Protection** - Copyright and trademark restrictions
- **Ownership Rights** - Clear ownership and usage rights
- **Commercial Value** - Can generate revenue

**Examples:**
- **Software Code** - Proprietary software applications
- **Designs** - Product designs and blueprints
- **Brands** - Logos and trademarks
- **Patents** - Inventions and technical innovations

### Legal Information
**Definition:** Court records, documents, and legal professional information

**Characteristics:**
- **Court Records** - Legal proceedings and judgments
- **Attorney Information** - Legal professional details
- **Judge Information** - Judicial system data
- **Legal Documents** - Contracts and legal agreements

**Security Requirements:**
- **Access Control** - Restricted to authorized personnel
- **Audit Trails** - Complete access logging
- **Retention Policies** - Long-term storage requirements
- **Confidentiality** - Attorney-client privilege protection

### Financial Information
**Definition:** Internal company and customer financial details

**Categories:**
- **Internal Financials** - Company financial statements and records
- **Customer Financials** - Client financial information
- **Payment Records** - Transaction and payment data
- **Credit Card Data** - Payment card information
- **Bank Records** - Banking and account information

**Security Requirements:**
- **PCI DSS Compliance** - Payment card industry standards
- **Encryption** - Strong encryption for sensitive data
- **Access Controls** - Strict access management
- **Monitoring** - Continuous security monitoring

## Data Readability Categories

### Human-Readable Data
**Characteristics:**
- **Clear Understanding** - Humans can easily understand the content
- **Obvious Content** - Very clear and obvious information
- **Text-Based** - Typically in text format
- **Direct Interpretation** - No special tools required

**Examples:**
- **Documents** - Word processing files and PDFs
- **Emails** - Text-based communications
- **Reports** - Business and financial reports
- **Logs** - System and application logs

### Non-Human Readable Data
**Characteristics:**
- **Encoded Format** - Not easily understood by humans
- **Binary Data** - Machine-readable format
- **Specialized Formats** - Require specific tools for interpretation
- **Compressed Data** - Reduced size for storage/transmission

**Examples:**
- **Encoded Data** - Base64 or other encoding schemes
- **Barcodes** - Machine-readable product codes
- **Images** - Binary image files
- **Encrypted Data** - Cryptographically protected information

## Data Sensitivity Classifications

### Proprietary Data
**Definition:** Data that is the property of an organization

**Characteristics:**
- **Organizational Ownership** - Belongs to the company
- **Trade Secret Inclusion** - May include trade secrets
- **Unique Value** - Often unique to the organization
- **Competitive Advantage** - Provides business value

### Personal Identifiable Information (PII)
**Definition:** Data that can be used to identify an individual

**Examples:**
- **Name** - Full name and aliases
- **Date of Birth** - Birth date and age
- **Mother's Maiden Name** - Family information
- **Biometric Information** - Fingerprints, facial recognition
- **Social Security Numbers** - Government identification
- **Addresses** - Physical and mailing addresses

### Protected Health Information (PHI)
**Definition:** Health information associated with an individual

**Characteristics:**
- **Health Status** - Medical conditions and diagnoses
- **Healthcare Records** - Medical history and treatments
- **HIPAA Compliance** - Must comply with health privacy laws
- **Sensitive Nature** - Highly personal and confidential

### Classification Levels

#### Sensitive
**Definition:** Intellectual Property, PII, PHI requiring special handling

**Requirements:**
- **Additional Permissions** - Enhanced access controls
- **Specialized Processes** - Different handling procedures
- **Restricted Access** - Limited network access
- **Encryption** - Strong data protection

#### Confidential
**Definition:** Very sensitive data requiring approval to view

**Requirements:**
- **Approval Process** - Must be approved to access
- **High Security** - Maximum security controls
- **Audit Requirements** - Complete access logging
- **Limited Distribution** - Restricted to authorized personnel

#### Public/Unclassified
**Definition:** No restrictions on viewing data

**Characteristics:**
- **Open Access** - Available to anyone
- **No Restrictions** - No access controls required
- **Public Information** - Can be freely shared
- **Minimal Security** - Basic protection only

#### Private/Classified/Restricted
**Definition:** Restricted access, may require non-disclosure agreements

**Requirements:**
- **NDA Requirements** - Non-disclosure agreements
- **Background Checks** - Personnel security clearance
- **Secure Facilities** - Physical security requirements
- **Compartmentalization** - Need-to-know access only

#### Critical
**Definition:** Data that should always be accessible

**Requirements:**
- **High Availability** - Maintain uptime of this data
- **Redundancy** - Multiple copies and backups
- **Disaster Recovery** - Rapid recovery procedures
- **Business Continuity** - Essential for operations

## Best Practices
- **Data Discovery** - Identify all data types in the organization
- **Classification Policies** - Establish clear classification criteria
- **Security Controls** - Implement appropriate controls for each classification
- **Regular Reviews** - Periodic classification reviews and updates
- **Staff Training** - Educate employees on data handling procedures
- **Compliance Management** - Ensure regulatory compliance