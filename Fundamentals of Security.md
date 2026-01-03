# 2. Fundamentals of Security

## Core Concepts

- **Information Security**: The strategic discipline focused on protecting data and information from unauthorized access, use, disclosure, alteration, or destruction. The goal is to ensure the business can operate securely and effectively.
    
- **Threat**: Any potential for an undesirable event that could cause harm to a system or organization. Threats can be intentional (e.g., a hacker) or unintentional (e.g., an employee error, a natural disaster).
    
- **Vulnerability**: A weakness or flaw in a system's design, implementation, or operation that could be exploited by a threat. For example, an unpatched software bug is a vulnerability.
    
- **Risk**: The likelihood that a specific threat will exploit a specific vulnerability, and the resulting business impact of that event. Risk = Threat x Vulnerability. Risk Management is the process of identifying, assessing, and mitigating this risk to an acceptable level.
    

## The CIA Triad

The CIA Triad is the foundational model for security policy. These three pillars are the primary goals of any security program.

- **Confidentiality**: Often called secrecy or privacy, this principle means preventing the unauthorized disclosure of information. Data should only be accessible to authorized individuals.
    
    - **Threats**: Eavesdropping, shoulder surfing, social engineering, theft of storage devices.
        
    - **Controls**: Encryption, Access Control Lists (ACLs), data classification.
        
- **Integrity**: The principle of ensuring that data is accurate, complete, and trustworthy. It guarantees that information has not been altered in an unauthorized or undetected manner.
    
    - **Threats**: Unauthorized modification of data, malware corrupting files, data entry errors.
        
    - **Controls**: Hashing (e.g., SHA-256), digital signatures, version control.
        
- **Availability**: The principle that systems, data, and resources are accessible and operational when needed by authorized users.
    
    - **Threats**: Denial-of-Service (DoS) attacks, hardware failures, power outages, natural disasters.
        
    - **Controls**: Redundancy (RAID, server clusters), disaster recovery plans, backups.
        

## Core Security Principles (AAA & Non-Repudiation)

- **Authentication**: The process of verifying a claimed identity. It answers the question, "Are you who you say you are?"
    
    - **Authentication Factors**:
        
        1. **Something you know**: Password, PIN.
            
        2. **Something you have**: Smart card, hardware token, mobile phone.
            
        3. **Something you are**: Biometrics (fingerprint, iris scan).
            
    - **MFA (Multi-Factor Authentication)** requires using two or more _different types_ of factors.
        
- **Authorization**: The process of granting or denying a subject's request to access an object, after successful authentication. It answers the question, "What are you allowed to do?" This is governed by the principle of **least privilege**, where users are given the minimum level of access necessary to perform their job functions.
    
- **Accounting (Auditing)**: The process of tracking and logging a subject's actions on an object. This creates an audit trail that can be used for forensic analysis, compliance, and holding users accountable for their actions.
    
- **Non-repudiation**: The assurance that a specific action occurred and cannot be denied by any party. It provides proof of origin and proof of delivery. Digital signatures are the primary technical control used to achieve non-repudiation, as they link an identity to a specific transaction.
    

## Security Models & Frameworks

- **Security Controls**: The safeguards or countermeasures put in place to avoid, detect, counteract, or minimize security risks.
    
    - **Categories**:
        
        - **Technical (Logical)**: Implemented using technology (e.g., firewalls, IDS, encryption).
            
        - **Managerial (Administrative)**: High-level policies, procedures, and guidelines (e.g., security awareness training, disaster recovery plan).
            
        - **Operational**: Day-to-day procedures executed by people (e.g., reviewing logs, performing backups).
            
        - **Physical**: Tangible measures to protect physical access (e.g., locks, fences, security guards).
            
    - **Types (Functions)**:
        
        - **Preventative**: Proactively stop an incident from occurring (e.g., firewall, security guard).
            
        - **Detective**: Identify that an incident is occurring or has already occurred (e.g., IDS, surveillance camera).
            
        - **Corrective**: Remediate the impact of an incident (e.g., restoring from backups, patching a vulnerability).
            
        - **Deterrent**: Discourage a potential attacker (e.g., warning banners, guard dogs).
            
        - **Compensating**: An alternative control used when a primary control is not feasible.
            
        - **Directive**: A mandatory control that dictates behavior (e.g., an Acceptable Use Policy).
            
- **Zero Trust**: A modern security model built on the philosophy of "never trust, always verify." It assumes that threats exist both inside and outside the traditional network perimeter.
    
    - **Core Tenets**:
        
        1. **Identity Verification**: Authenticate and authorize every access request.
            
        2. **Micro-segmentation**: Break the network into small, isolated zones to limit lateral movement.
            
        3. **Least Privilege Access**: Grant the minimum access required for the task at hand.
            
- **Gap Analysis**: A formal process of comparing an organization's current performance or security posture against a desired future state or industry standard (like NIST or ISO). The output is a "gap" report, which feeds into a **POA&M (Plan of Action and Milestones)** that details the specific tasks, resources, and timelines required to close the identified gaps.