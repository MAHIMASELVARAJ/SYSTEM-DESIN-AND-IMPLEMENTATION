# Paper 05 – Continuous Authentication for Zero-Trust IIoT

## Paper Details

**Title:** A Continuous Authentication Scheme for Zero-Trust Architecture in Industrial Internet of Things

**Year:** 2025

**Authors:** Tao Wan, Buhai Shi, Huan Wang

**Journal:** Alexandria Engineering Journal

## 1. Problem Addressed

In Zero Trust environments, authentication performed only during login is insufficient for protecting long-running sessions.

An authenticated user or device may become compromised after the session begins.

The paper addresses continuous authentication within a Zero Trust IIoT environment.

## 2. Existing System

The proposed scheme continuously verifies users and devices during active sessions.

It incorporates multiple authentication and contextual mechanisms.

The approach includes device authentication, location verification and user authentication.

## 3. Existing Technologies / Methods

- Zero Trust Architecture
- Continuous authentication
- Device authentication
- Location verification
- User authentication
- Session monitoring
- Multi-factor authentication

## 4. Existing System Component Relevant to Our Project

The most important component for ProofPulse is continuous verification during an active session.

Instead of:

Login
↓
Trust

the security process becomes:

Login
↓
Continuous Verification
↓
Trust Update

## 5. How It Will Be Used in ProofPulse

ProofPulse will continuously monitor active sessions.

When a sensitive action is requested, the system will reassess the current trust state.

### Proposed workflow

Login
↓
Session Creation
↓
Action 1 → Monitor
↓
Action 2 → Monitor
↓
Action 3 → Monitor
↓
Sensitive Action
↓
Trust Evaluation
↓
ALLOW / STEP-UP / BLOCK

## 6. Proposed System Module

**Module:** Continuous Session Monitoring Engine

## 7. Limitation of Existing System

The existing work focuses primarily on continuous authentication in an IIoT environment.

ProofPulse is designed for cloud-resource access and investigates how action history can influence the current trust state.

## 8. Research Gap

A cloud-deployable system can investigate action-level and sequence-aware trust evaluation in which the trust state changes according to observed session behavior.

## 9. Relevance to ProofPulse

This paper provides a practical foundation for continuous verification during active sessions.

## 10. Proposed Contribution

ProofPulse will adapt continuous-session verification to cloud environments and investigate stateful trust transitions based on user actions, device context and behavioral signals.

## Reference

Official article:
https://www.sciencedirect.com/science/article/pii/S111001682500300X

DOI:
https://doi.org/10.1016/j.aej.2025.03.012
