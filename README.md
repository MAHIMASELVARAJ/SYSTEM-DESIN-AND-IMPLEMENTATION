# Cybersecurity & Digital Trust – Design Thinking Project

## Overview

This repository documents a **design-thinking and research-driven project** focused on identifying and designing solutions for real-world problems in **Cybersecurity and Digital Trust**.

The project follows a structured progression from real-world problem identification to case-study evaluation, project selection, literature survey, and high-level system design.

### Project Journey

**Design Thinking → Problem Identification → 5 Case Studies → Evaluation → 2 Selected Projects → Literature Survey → High-Level Design**

---

# 🎯 Why Cybersecurity & Digital Trust?

Modern digital environments increasingly depend on cloud applications, APIs, IoT/OT devices, distributed systems, and continuously changing system behavior.

This creates cybersecurity challenges where detecting an individual suspicious event may not be sufficient. Security systems may also need to understand patterns across multiple actions and respond automatically when a dangerous condition is identified.

Therefore, the project focuses on cybersecurity problems that have:

- Real-world security impact
- Clear technical problems
- Research opportunities
- Practical feasibility
- Scope for innovative system design
- Cloud deployment potential
- Potential for future prototype development
- Potential for further novelty and patent analysis

---

# 🔎 Week 1 – Cybersecurity Case Study Exploration

The first stage of the project focused on identifying and analyzing **five cybersecurity case studies**.

Each case study was examined based on:

- Problem clarity
- Existing limitations
- Proposed solution
- Implementation approach
- Target outcomes
- Technical significance
- Research and innovation potential

The five proposed case studies were:

### Case Study 1
**Cross-Tenant Ransomware Detection & Isolation**

Focus:
Detecting correlated ransomware activity across multiple cloud tenants and automatically isolating the affected storage segment.

### Case Study 2
**Post-Quantum Key Migration Orchestrator**

Focus:
Safely migrating cryptographic keys across multiple cloud environments while maintaining service availability.

### Case Study 3
**Real-Time Deepfake Detection Gateway**

Focus:
Detecting synthetic audio/video during live communication and intervening directly in the media pipeline.

### Case Study 4
**API Aggregation-Inference Attack Detection**

Focus:
Detecting attacks where individually authorized API requests combine over time to produce an unauthorized or dangerous outcome.

### Case Study 5
**OT/IoT Anomaly-Driven Auto-Isolation**

Focus:
Detecting abnormal behavior in industrial IoT/OT devices and automatically isolating a compromised device before its dangerous command reaches physical equipment.

### Week 1 Status

- [x] Identify cybersecurity problem domain
- [x] Develop 5 cybersecurity case studies
- [x] Define problem statements
- [x] Propose solutions
- [x] Define implementation approaches
- [x] Define target outcomes
- [x] Analyze research and innovation potential

📁 **Week 1 Case Studies**

`Week-1-Case-Studies/`

---

# 📊 Week 2 – Case Study Evaluation & Project Selection

The five case studies were evaluated using six criteria:

| Criterion | What it Measures |
|---|---|
| Problem Clarity | Whether the problem is specific enough to research and build against |
| Feasibility | Whether a realistic prototype can be developed within the project timeline |
| Literature Availability | Availability of sufficient recent research for literature analysis |
| Novelty Headroom | Whether an initial review suggests that a meaningful technical gap may remain |
| Patentability Potential | Potential for a concrete technical contribution or technical effect |
| Real-World Impact | Significance of the cybersecurity problem if left unsolved |

Each criterion was scored from **1 to 5**, giving a maximum score of **30**.

## Evaluation Results

| Case Study | Problem Clarity | Feasibility | Literature | Novelty | Patentability | Impact | **Total /30** |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1 — Cross-Tenant Ransomware Detection & Isolation | 5 | 4 | 5 | 2 | 4 | 4 | **24** |
| 2 — Post-Quantum Key Migration Orchestrator | 4 | 3 | 4 | 3 | 4 | 5 | **23** |
| 3 — Real-Time Deepfake Detection Gateway | 4 | 3 | 3 | 3 | 4 | 5 | **22** |
| 4 — API Aggregation-Inference Attack Detection | 5 | 4 | 4 | 5 | 4 | 4 | **26** |
| 5 — OT/IoT Anomaly-Driven Auto-Isolation | 4 | 4 | 4 | 4 | 5 | 5 | **26** |

The two highest-scoring case studies were **Case Study 4** and **Case Study 5**.

Therefore, these two projects were selected for further literature research and high-level system design.

---

# 🛡️ Selected Project 1 – TesseraGuard

## Aggregation-Aware API Threat Detection & Enforcement Gateway

**Origin:** Case Study 4 — API Aggregation-Inference Attack Detection

**Score:** 26/30

---

## Problem

Modern cloud applications use multiple microservices that communicate through APIs.

Traditional security controls commonly evaluate API requests individually.

For example:

API Request 1 → Authorized → ALLOW
API Request 2 → Authorized → ALLOW
API Request 3 → Authorized → ALLOW
API Request 4 → Authorized → ALLOW

Although every individual request may be authorized, a sequence of such requests can collectively result in excessive data access or another unauthorized outcome.

The problem addressed by TesseraGuard is therefore the detection of dangerous combinations of individually authorized API calls.

## Proposed Solution

TesseraGuard is designed as an aggregation-aware API threat detection and enforcement gateway.

Instead of evaluating only the current API request, the system maintains a history of actions associated with an identity and analyzes how multiple calls combine over time.

**The system considers factors such as:**

Caller identity
Session information
API calls
Data accessed
Data volume
Rate of accumulation
Combination of actions

The system then determines whether the accumulated activity represents a risky combination.

The enforcement decision can be:

## ALLOW → THROTTLE → BLOCK

# 🏭 Selected Project 2 – ReflexGuard
Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Origin:** Case Study 5 — OT/IoT Anomaly-Driven Auto-Isolation

**Score:** 26/30

## Problem

Industrial IoT and OT environments contain sensors and actuators that interact with physical equipment.

A compromised device may behave differently from its established normal behavior and potentially issue a dangerous command to physical machinery.

Cloud-only monitoring may not react quickly enough when immediate action is required.

The problem addressed by ReflexGuard is therefore the detection of abnormal device behavior and automatic isolation at the edge before a dangerous signal reaches the physical equipment.

## Proposed Solution

ReflexGuard uses an edge-based security mechanism positioned close to industrial devices.

The system continuously observes device behavior and compares current activity with the established normal behavior of each device.

**The system considers:**

Normal signal ranges
Command vocabulary
Timing patterns
Device behavior
Anomaly severity
Potential physical consequence

The system can determine:

## ALLOW → ALERT → ISOLATE

When a high-risk anomaly is detected, the affected device is automatically isolated from the control network at the edge.

The cloud dashboard is notified in parallel so that operators can investigate the incident.
