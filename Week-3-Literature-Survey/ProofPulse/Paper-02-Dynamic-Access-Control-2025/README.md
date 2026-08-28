# Paper 02 – Zero-Trust Based Dynamic Access Control for Cloud Computing

## Paper Details

**Title:** Zero-Trust Based Dynamic Access Control for Cloud Computing

**Year:** 2025

**Authors:** Ri Wang et al.

**Journal:** Cybersecurity

## 1. Problem Addressed

Traditional cloud access-control systems may rely on static rules.

However, the risk associated with a user can change according to behavior and security context.

The paper addresses dynamic access control in cloud environments using Zero Trust concepts.

## 2. Existing System

The existing approach considers user behavior and trust when making dynamic access-control decisions.

The system investigates machine-learning-based behavioral analysis and dynamic policy decisions.

## 3. Existing Technologies / Methods

- Zero Trust
- Dynamic access control
- User behavior analysis
- Trust evaluation
- Machine learning
- LSTM
- DQN
- Cloud authorization

## 4. Existing System Component Relevant to Our Project

The most relevant component is the combination of:

**User Behavior → Trust Evaluation → Dynamic Access Control**

This workflow directly supports ProofPulse.

## 5. How It Will Be Used in ProofPulse

ProofPulse will collect behavioral events during an active session.

Example signals:

- Login behavior
- Resource access
- API calls
- Access frequency
- Device information
- Session activity

These features will contribute to the user's current trust score.

### Proposed workflow

User Activity
↓
Behavior Collection
↓
Feature Extraction
↓
Behavior Analysis
↓
Trust Score
↓
Dynamic Policy
↓
ALLOW / STEP-UP / BLOCK

## 6. Proposed System Module

**Module:** Behavioral Trust Engine

## 7. Limitation of Existing System

The existing approach focuses on dynamic access control and behavioral trust but does not specifically focus on representing sequences of sensitive actions as transitions between trust states.

## 8. Research Gap

A research opportunity exists in examining whether action history and action sequences can be incorporated into trust-state transitions and subsequent assurance requirements.

## 9. Relevance to ProofPulse

This paper provides a technical foundation for ProofPulse's behavior analysis and dynamic trust evaluation.

## 10. Proposed Contribution

ProofPulse will investigate combining behavioral trust with action-level monitoring and stateful trust transitions for cloud resource access.

## Reference

Official article:
https://link.springer.com/article/10.1186/s42400-024-00320-x

DOI:
https://doi.org/10.1186/s42400-024-00320-x
