# Paper 01 – Verify and Trust

## Paper Details

**Title:** Verify and Trust: A Multidimensional Survey of Zero-Trust Security in the Age of IoT

**Year:** 2024

**Authors:** Muhammad Ajmal Azad et al.

**Journal:** Internet of Things

## 1. Problem Addressed

Traditional security models often rely on the assumption that authenticated users and devices can be trusted.

In modern cloud and IoT environments, users, devices, locations and behaviors can change during a session.

The paper examines Zero Trust as an approach where trust must be continuously evaluated.

## 2. Existing System

The work provides a multidimensional view of Zero Trust security.

It considers different factors including:

- User identity
- Device information
- Authentication
- Authorization
- Location
- Behavioral context
- Access control

## 3. Existing Technologies / Methods

- Zero Trust Architecture
- Continuous verification
- Authentication
- Authorization
- Context-aware security
- Device trust
- Behavioral information

## 4. Existing System Component Relevant to Our Project

The main contribution relevant to ProofPulse is the Zero Trust principle of continuously evaluating trust instead of relying only on initial authentication.

## 5. How It Will Be Used in ProofPulse

ProofPulse will use Zero Trust as its foundational security architecture.

### Proposed workflow

User
↓
Authentication
↓
Active Session
↓
Continuous Monitoring
↓
User + Device + Context + Behaviour
↓
Trust Evaluation
↓
Dynamic Authorization
↓
ALLOW / STEP-UP / BLOCK

## 6. Proposed System Module

**Module:** Zero Trust Foundation and Continuous Verification Layer

## 7. Limitation of Existing System

The paper provides a broad Zero Trust perspective rather than a specific action-sequence-based trust transition mechanism.

## 8. Research Gap

A system is required that can translate continuous behavioral and contextual observations into dynamic trust changes for individual actions.

## 9. Relevance to ProofPulse

The paper establishes the fundamental Zero Trust principle on which ProofPulse is designed.

## 10. Proposed Contribution

ProofPulse will extend continuous Zero Trust evaluation toward action-level trust decisions during an active cloud session.

## Reference

Official article:
https://www.sciencedirect.com/science/article/pii/S2542660524001689

Open-access source:
https://www.open-access.bcu.ac.uk/15698/
