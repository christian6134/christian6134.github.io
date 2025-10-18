# 2.4.2 Viruses and Worms

## Learning Objectives
- Distinguish between viruses and worms
- Understand different virus types and their characteristics
- Explain fileless malware and its detection challenges

## Overview
Viruses and worms are two primary types of self-replicating malware that differ in their propagation methods and user interaction requirements.

## Viruses
**Characteristics:**
- Require user intervention to execute
- Attach to legitimate programs or files
- Reproduce through file systems or networks
- May cause damage or remain dormant

### Virus Types
- **Program Viruses** - Infect executable files and applications
- **Boot Sector Viruses** - Infect the boot sector of storage devices
- **Script Viruses** - Written in scripting languages (JavaScript, VBScript)
- **Macro Viruses** - Embedded in document macros (Microsoft Office)

### Fileless Viruses
Fileless viruses operate entirely in memory without writing to storage:
- **Stealth Attack** - Avoids traditional file-based detection
- **Memory-Only Operation** - No files installed on the system
- **PowerShell Exploitation** - Uses legitimate system tools
- **RAM-Based Payloads** - Downloads and executes in memory

**Example Attack Flow:**
1. User clicks malicious link
2. Website exploits browser/OS vulnerability
3. Launches PowerShell to download payload
4. Payload executes entirely in RAM

## Worms
**Characteristics:**
- Self-replicating malware
- No user intervention required
- Use networks as transmission medium
- Spread rapidly across connected systems

**Key Differences from Viruses:**
- **Worms:** Self-propagate without user action
- **Viruses:** Require user interaction (clicking, opening files)

## Mitigation Strategies
- **Network Segmentation** - Limit worm spread
- **IDS/IPS Systems** - Detect and block worm traffic
- **Patch Management** - Close vulnerabilities worms exploit
- **Email Filtering** - Block malicious attachments
- **User Training** - Recognize suspicious links and attachments