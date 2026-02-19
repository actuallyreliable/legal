+++
layout = "legal"
title = "Security Overview"
description = "How we protect your data and respond to security incidents."
slug = "security"
draft = false
+++

## Introduction

Protecting customer data is one of our most serious obligations. We invest heavily in security not just because our customers depend on it, but because our own sensitive business information lives on the same infrastructure. That shared stake keeps us focused. When we harden our systems, we are protecting ourselves just as much as we are protecting you.

---

## Access Control and Organizational Security

### Personnel

Every employee and contractor at Actually Reliable signs a confidentiality agreement before receiving access to our codebase or any customer data. We do not currently perform background checks on new hires or contractors. Security awareness is part of onboarding and ongoing training at all levels of the organization. Remote server access is available exclusively through our VPN with two-factor authentication enforced, and is restricted to those whose roles require it. All account access is logged by IP address.

### Dedicated Teams

Our Operations and Security teams are jointly responsible for access management, identity systems, network configuration, firewall rules, and log management. Their ongoing responsibilities include:

- Reviewing all code and infrastructure changes against established security guidelines and best practices (including OWASP)
- Building and operating the infrastructure that underpins our Services, including authentication, monitoring, and audit logs
- Designing, testing, and iterating on incident response procedures
- Triaging and responding to security alerts
- Detecting and escalating anomalous activity
- Deploying application-level encryption and tooling to protect customer data from internal exposure

### Audits, Standards, and Compliance

Payment processing is handled by Stripe, which maintains PCI compliance on our behalf. We have not yet completed a SOC audit for our own infrastructure, and we are transparent about that gap.

---

## Data Protection and Privacy

Our full Privacy Policy is available at [actuallyreliable.com/legal/privacy](https://actuallyreliable.com/legal/privacy). The following summarizes our most important data protection practices.

### Data Location

Data centers we utilize are primarily located in the United States. All data is written to multiple disks simultaneously and stored redundantly across multiple physical locations. Customer-uploaded files are distributed across storage systems engineered to eliminate single points of failure.

### Encryption In Transit and At Rest

All data transmitted over public networks is protected using strong encryption via SSL/TLS certificates. Files uploaded to our platform are encrypted at rest using AES-256 with ChaCha20-Poly1305. Each file is encrypted with a unique data encryption key (DEK), which is itself encrypted using our company's master key. Those files are also sliced, replicated, and distributed across geographically separate data centers, connected via private, end-to-end encrypted network links. Data integrity is verified using SHA3-512. Application database records are encrypted at rest by our database provider (PlanetScale) using AES encryption on underlying storage media. All passwords are hashed using Argon2id (memory-hard password hashing) before storage. Off-site backups are encrypted using the same method as files.

### Physical Security

Data centers we utilize are secured by our hosting providers with biometric access controls and continuous interior and exterior video surveillance. Access is restricted to authorized personnel. Around-the-clock on-site security staff provides an additional layer of protection against unauthorized access.

### Law Enforcement Requests

We will not provide your data to law enforcement without a valid court order. We categorically reject requests — from local, state, or federal agencies — that are not accompanied by one. Unless we are legally barred from doing so, we will inform you when such a request is received.

### Data Deletion

Your content becomes inaccessible the moment your Account is cancelled. All content is permanently deleted from our systems within 60 days. Once permanently deleted, this data cannot be recovered.

For more information, see our Privacy Policy at [actuallyreliable.com/legal/privacy](https://actuallyreliable.com/legal/privacy).

---

## Full Redundancy for All Major Systems

The infrastructure at data centers we utilize — power supplies, network connectivity, cooling, and environmental systems — is built for full redundancy. Our architecture is designed so that the failure of multiple servers simultaneously does not take our Services offline.

---

## Regularly Updated Infrastructure

We apply security patches to our software infrastructure on a continuous basis. Our products operate on a dedicated, firewalled network that is actively monitored. Security is never a finished problem, and we work with external security researchers to stay current with emerging threats and techniques.

---

## Billing Information

All payment card transactions are processed using the same level of encryption employed by major financial institutions. Card data is transmitted, stored, and processed exclusively on a PCI-compliant network via our payment processor.

---

## Incident Management and Disaster Recovery

We conduct regular disaster recovery drills that simulate a range of failure and attack scenarios. All databases are backed up regularly, and file backups are created automatically upon upload. Backup integrity is tested on a routine basis. Off-site backups are retained for a maximum of 60 days. Our Operations and Security teams maintain documented procedures for incident response. In the event of an incident, we will contact your Account Owner within 72 hours and remain engaged with you throughout the resolution process.

---

## Constant Monitoring

We maintain a dedicated team responsible for monitoring our infrastructure for suspicious or malicious activity. Internal data access is audited. Any employee found to have accessed Customer Data without authorization will face disciplinary action, up to and including termination and referral for prosecution.

If a security breach does occur, all affected customers will be notified within 72 hours of our becoming aware of it.

---

## Security Response

### We Welcome Your Input

Security is an area where outside perspective matters. If you have spotted something that concerns you, we want to hear about it.

### Reporting Security Problems

**Experiencing an active account attack** — unauthorized login attempts, suspicious activity, or similar — email us immediately at [security@actuallyreliable.com](mailto:security@actuallyreliable.com). We treat these with urgency and typically respond within a few hours to help you address the threat.

**Discovered a security vulnerability?** Send your report to [security@actuallyreliable.com](mailto:security@actuallyreliable.com). Please include a detailed description of the issue, steps to reproduce it, and your assessment of its potential impact. We will acknowledge receipt within 72 hours.

**Other urgent or sensitive security matters** relating to our products or your Account should also be directed to [security@actuallyreliable.com](mailto:security@actuallyreliable.com).

**Non-urgent questions or general inquiries** that are not security-sensitive can be submitted through our [support channel](mailto:support@actuallyreliable.com).

### How We Handle Vulnerability Reports

When you submit a vulnerability report, here is what happens:

- We will acknowledge your report within 72 hours.
- We will triage the report to assess its validity and potential impact.
- We will investigate the issue and determine its scope. We do not disclose vulnerabilities publicly until they have been fully addressed, but we will communicate openly with you throughout the process.
- After the issue is resolved, we will publish a security update that includes attribution and thanks to the researcher who reported it.

Our products are built on widely used frameworks and infrastructure. In some cases, a reported vulnerability may affect a technology maintained by a third party. We will work with any affected parties as needed and keep you updated on progress regardless.

### Our Commitment to Researchers

Finding and disclosing security vulnerabilities responsibly takes real skill and time. We respect the work that security researchers do, and we are committed to treating every report fairly, responding transparently, and working collaboratively toward resolution.

### Other Questions

For security questions not covered above, [contact our support team](mailto:support@actuallyreliable.com).
