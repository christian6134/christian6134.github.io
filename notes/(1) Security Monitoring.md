# 4.4.1 Security Monitoring

## Learning Objectives
- Understand security monitoring concepts and entry point surveillance
- Explain computing resource monitoring for systems, applications, and infrastructure
- Describe log aggregation, SIEM, and correlation capabilities
- Identify scanning, reporting, archiving, and alerting processes

## Overview
Security monitoring involves comprehensive surveillance of all entry points, real-time reaction to security events, and continuous monitoring of computing resources to maintain security posture and respond to threats effectively.

## Security Monitoring Fundamentals

### Core Concepts
**Entry Point Monitoring:** Monitor all entry points to the network

**Key Functions:**
- **Security Event Reaction** - React to security events in real-time
- **Status Dashboards** - Provide real-time security status
- **Threat Detection** - Detect security threats and anomalies
- **Incident Response** - Support incident response activities

**Monitoring Benefits:**
- **Early Detection** - Detect threats early
- **Rapid Response** - Respond quickly to security events
- **Visibility** - Provide visibility into security posture
- **Compliance** - Meet regulatory compliance requirements

## Monitoring Computing Resources

### Systems Monitoring
**Authentication Monitoring:**
- **Login Monitoring** - Monitor logins from strange places
- **Failed Attempts** - Track failed authentication attempts
- **Unusual Patterns** - Detect unusual login patterns
- **Account Lockouts** - Monitor account lockout events

**Server Monitoring:**
- **Service Activity** - Monitor service activity and status
- **Backup Monitoring** - Monitor backup processes and status
- **Performance Metrics** - Track server performance metrics
- **Resource Utilization** - Monitor resource utilization

### Applications Monitoring
**Availability Monitoring:**
- **Uptime Tracking** - Track application uptime
- **Response Times** - Monitor response times
- **Service Availability** - Monitor service availability
- **Performance Metrics** - Track application performance

**Data Transfer Monitoring:**
- **Data Flow** - Monitor data transfers
- **Volume Analysis** - Analyze data transfer volumes
- **Anomaly Detection** - Detect unusual data transfers
- **Compliance** - Ensure compliance with data policies

**Security Notifications:**
- **Security Events** - Monitor security-related events
- **Access Attempts** - Track access attempts
- **Permission Changes** - Monitor permission changes
- **Configuration Changes** - Track configuration changes

### Infrastructure Monitoring
**Firewall and IPS Reports:**
- **Traffic Analysis** - Analyze firewall traffic
- **Blocked Attempts** - Monitor blocked connection attempts
- **IPS Alerts** - Monitor intrusion prevention alerts
- **Policy Violations** - Track policy violations

**Remote Access Systems:**
- **VPN Monitoring** - Monitor VPN connections
- **Remote Sessions** - Track remote access sessions
- **Authentication Events** - Monitor authentication events
- **Connection Logs** - Maintain connection logs

## Log Aggregation

### SIEM (Security Information and Event Management)
**Centralized Logging:** Consolidate log files to central database

**Log Sources:**
- **Servers** - Server logs and events
- **Firewalls** - Firewall logs and traffic
- **Network Devices** - Network device logs
- **Applications** - Application logs and events

**SIEM Capabilities:**
- **Centralized Reporting** - Generate centralized reports
- **Data Correlation** - Correlate data between diverse systems
- **Real-Time Analysis** - Real-time log analysis
- **Long-Term Storage** - Long-term log storage

**Correlation Benefits:**
- **Threat Detection** - Detect complex threats
- **Pattern Recognition** - Recognize attack patterns
- **Incident Investigation** - Support incident investigation
- **Compliance** - Meet compliance requirements

## Scanning

### Active System Checking
**Purpose:** Actively check systems and devices

**Scanning Targets:**
- **Operating Systems** - Scan OS versions and configurations
- **Installed Applications** - Identify installed applications
- **Anomaly Detection** - Detect system anomalies
- **Configuration Changes** - Track configuration changes

**Scanning Methods:**
- **Automated Scanning** - Use automated scanning tools
- **Manual Verification** - Perform manual verification
- **Scheduled Scans** - Regular scheduled scans
- **On-Demand Scans** - On-demand scanning

## Reporting

### Data Analysis
**Purpose:** Analyze collected data and create actionable reports

**Report Types:**
- **Status Information** - Current security status
- **Trend Analysis** - Security trend analysis
- **Incident Reports** - Incident investigation reports
- **Compliance Reports** - Compliance status reports

**Actionable Reports:**
- **Clear Recommendations** - Provide clear recommendations
- **Priority Levels** - Indicate priority levels
- **Remediation Steps** - Outline remediation steps
- **Follow-up Actions** - Define follow-up actions

## Archiving

### Long-Term Data Access
**Breach Timeline:** Average of 9 months to identify and contain breach

**Critical Requirements:**
- **Data Access** - Access to historical data is critical
- **Long-Term Storage** - Maintain long-term data storage
- **Retrieval Capability** - Quick data retrieval capability
- **Compliance** - Meet data retention requirements

**Archiving Benefits:**
- **Incident Investigation** - Support incident investigation
- **Forensic Analysis** - Enable forensic analysis
- **Compliance** - Meet regulatory requirements
- **Trend Analysis** - Enable long-term trend analysis

## Alerting

### Real-Time Notifications
**Purpose:** Real-time notification of security events

**Alert Types:**
- **Authentication Errors** - Failed authentication attempts
- **Large File Transfers** - Unusual data transfer volumes
- **System Anomalies** - Unusual system behavior
- **Policy Violations** - Security policy violations

**Alert Characteristics:**
- **Real-Time** - Immediate notification
- **Relevant** - Only relevant alerts
- **Actionable** - Provide actionable information
- **Prioritized** - Prioritized by severity

## Alert Response and Remediation

### Quarantine Response
**Foundational Security:** Quarantine the system as foundational security response

**Quarantine Benefits:**
- **Spread Prevention** - Prevent potential security issues from spreading
- **Containment** - Contain security incidents
- **Investigation** - Enable investigation without risk
- **Recovery** - Facilitate recovery processes

### Alert Tuning
**Purpose:** Prevent false positives and false negatives

**Tuning Requirements:**
- **Alert Accuracy** - Alerts should be accurate
- **Relevance** - Alerts should be relevant
- **Actionability** - Alerts should be actionable
- **Timeliness** - Alerts should be timely

**Tuning Process:**
- **Threshold Adjustment** - Adjust alert thresholds
- **Rule Refinement** - Refine alert rules
- **Feedback Integration** - Integrate feedback from analysts
- **Continuous Improvement** - Continuously improve alerting

## Best Practices
- **Comprehensive Coverage** - Monitor all critical systems
- **Real-Time Monitoring** - Implement real-time monitoring
- **Automated Response** - Use automated response where appropriate
- **Regular Tuning** - Regularly tune alerting systems
- **Documentation** - Document all monitoring activities
- **Staff Training** - Train staff on monitoring systems
- **Incident Response** - Integrate with incident response
- **Continuous Improvement** - Continuously improve monitoring