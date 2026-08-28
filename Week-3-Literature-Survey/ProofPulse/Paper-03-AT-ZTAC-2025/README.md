# Paper 03 – AT-ZTAC

## Paper Details

**Title:** A Zero-Trust Access Control Model Based on Attribute and Dynamic Trust Evaluation for Cloud Environments

**Year:** 2025

**Journal:** Symmetry

## 1. Problem Addressed

Cloud users and devices operate in changing environments.

Static access-control rules may not sufficiently reflect changes in:

- User attributes
- Device state
- Context
- Trust level
- Resource sensitivity

The paper addresses dynamic cloud access control using attributes and dynamic trust.

## 2. Existing System

The proposed model combines Attribute-Based Access Control with dynamic trust evaluation within a Zero Trust environment.

Access decisions depend on attributes and changing trust conditions.

## 3. Existing Technologies / Methods

- Zero Trust
- Attribute-Based Access Control
- Dynamic trust evaluation
- Cloud access control
- Policy-based authorization
- User attributes
- Context information

## 4. Existing System Component Relevant to Our Project

ProofPulse will use the concept of combining:

**Attributes + Dynamic Trust + Authorization**

## 5. How It Will Be Used in ProofPulse

ProofPulse will collect attributes from multiple sources.

### User attributes

- Role
- Department
- Account status

### Device attributes

- Device health
- Security posture
- Operating system

### Context attributes

- Location
- Time
- Network

### Action attributes

- Resource sensitivity
- Requested operation

These attributes will be combined with the current trust state.

### Proposed workflow

Attributes
+
Current Trust
+
Requested Action
↓
Policy Engine
↓
Authorization Decision
↓
ALLOW / STEP-UP / BLOCK

## 6. Proposed System Module

**Module:** Attribute and Policy Decision Engine

## 7. Limitation of Existing System

Attribute-based and dynamic-trust authorization provides strong contextual access control, but the proposed ProofPulse direction additionally investigates how previous action sequences can affect future trust states.

## 8. Research Gap

There is an opportunity to investigate stateful trust evaluation where the current trust state changes according to observed actions and their sequence.

## 9. Relevance to ProofPulse

AT-ZTAC provides a direct foundation for ProofPulse's attribute collection and policy decision layer.

## 10. Proposed Contribution

ProofPulse will investigate combining attribute-based authorization with behavioral trust and action-sequence-driven trust transitions.

## Reference

Official article:
https://www.mdpi.com/2073-8994/17/12/2059

PDF:
https://www.mdpi.com/2073-8994/17/12/2059/pdf
