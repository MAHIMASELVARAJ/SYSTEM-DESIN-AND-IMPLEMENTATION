# Paper 04 – Continuous Authentication in Zero Trust Architecture

## Paper Details

**Title:** A Systematic Literature Review on Continuous Authentication in Zero Trust Architecture for Business

**Year:** 2025

## 1. Problem Addressed

Traditional authentication normally verifies a user's identity at login.

If an attacker takes control of an authenticated session, the attacker may continue accessing resources without being detected.

The paper reviews continuous authentication techniques designed to continuously verify users during active sessions.

## 2. Existing System

The systematic review examines research approaches for continuous authentication within Zero Trust environments.

It identifies behavioral and contextual information as important inputs for continuous verification.

## 3. Existing Technologies / Methods

- Continuous authentication
- Zero Trust
- Behavioral biometrics
- Machine learning
- Context-aware authentication
- Sensor information
- User behavior analysis

## 4. Existing System Component Relevant to Our Project

The most relevant contribution is the identification of behavioral and contextual signals that can be used to continuously evaluate whether the current session still belongs to the legitimate user.

## 5. How It Will Be Used in ProofPulse

ProofPulse will use suitable behavioral and contextual signals as inputs to its trust engine.

Potential signals include:

- Login patterns
- Access behavior
- Session activity
- Device information
- Location
- Interaction patterns

### Proposed workflow

Active Session
↓
Behavioral Signals
↓
Feature Extraction
↓
Continuous Verification
↓
Trust Update
↓
Policy Decision

## 6. Proposed System Module

**Module:** Behavioral and Continuous Authentication Engine

## 7. Limitation of Existing System

The work is a systematic review of continuous-authentication approaches rather than a complete action-level cloud authorization system.

## 8. Research Gap

A practical cloud system can investigate how continuous authentication signals can be integrated with dynamic authorization and action-level trust evaluation.

## 9. Relevance to ProofPulse

The review provides guidance for selecting appropriate behavioral and contextual signals for ProofPulse.

## 10. Proposed Contribution

ProofPulse will use continuous verification signals as inputs to a stateful trust engine that influences authorization decisions during active sessions.

## Reference

Official article:
https://jisem-journal.com/index.php/journal/article/view/12787

PDF:
https://jisem-journal.com/index.php/journal/article/download/12787/5945/21516
