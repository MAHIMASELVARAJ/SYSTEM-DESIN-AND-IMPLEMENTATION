# Week 2 — Case Study Evaluation, Selection & Justification

## Overview

Week 2 focuses on evaluating the five cybersecurity case studies proposed during Week 1 and selecting the two strongest projects for detailed research, literature analysis, architecture design, and future prototype development.

The selection was based on six criteria:

1. Problem Clarity
2. Feasibility
3. Literature Availability
4. Novelty Headroom
5. Patentability Potential in India
6. Real-World Impact

Each criterion was scored from 1 to 5, giving a maximum possible score of 30.

The purpose of this evaluation is not to claim that any project is already novel or patentable. Instead, the scoring identifies which projects have the strongest combination of research potential, technical contribution, feasibility, and potential for further prior-art and patent analysis.

---

# 1. Selection Criteria

| Criterion | What it Measures |
|---|---|
| Problem Clarity | Whether the cybersecurity problem is specific enough to research, model, and build against |
| Feasibility | Whether a realistic prototype can be developed within the available project timeline and resources |
| Literature Availability | Whether sufficient recent academic research exists to support a meaningful literature survey |
| Novelty Headroom | Whether an initial prior-art and research review suggests that a meaningful technical gap may remain |
| Patentability Potential (India) | Whether the proposed solution can demonstrate a concrete technical contribution or technical effect rather than only an abstract algorithm or business method |
| Real-World Impact | The potential security and operational consequences of the problem if it remains unsolved |

---

# 2. Evaluation of the Five Case Studies

| Case Study | Problem Clarity | Feasibility | Literature Availability | Novelty Headroom | Patentability Potential | Real-World Impact | Total /30 |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1 — Cross-Tenant Ransomware Detection & Isolation | 5 | 4 | 5 | 2 | 4 | 4 | **24** |
| 2 — Post-Quantum Key Migration Orchestrator | 4 | 3 | 4 | 3 | 4 | 5 | **23** |
| 3 — Real-Time Deepfake Detection Gateway | 4 | 3 | 3 | 3 | 4 | 5 | **22** |
| 4 — API Aggregation-Inference Attack Detection | 5 | 4 | 4 | 5 | 4 | 4 | **26** |
| 5 — OT/IoT Anomaly-Driven Auto-Isolation | 4 | 4 | 4 | 4 | 5 | 5 | **26** |

---

# 3. Comparative Selection Analysis

## Case Study 1 — Cross-Tenant Ransomware Detection & Isolation

**Score: 24/30**

### Strengths

- Clearly defined cloud cybersecurity problem.
- Strong real-world impact because ransomware can cause large-scale data loss.
- Good feasibility for a simulated cloud environment.
- Strong availability of ransomware detection literature.
- Automatic isolation provides a concrete security response.

### Limitation

The main weakness is **novelty headroom**.

An initial prior-art investigation indicated that ransomware detection based on storage I/O behavior, rapid file modification, and automated recovery or snapshot rollback is already a heavily explored and patented area.

The cross-tenant propagation and containment concept may still contain a research gap, but this gap requires deeper independent prior-art investigation.

### Selection Decision

**Not selected.**

Although technically strong, the uncertainty surrounding the novelty of the proposed mechanism makes it less attractive than the two higher-scoring candidates.

---

## Case Study 2 — Post-Quantum Key Migration Orchestrator

**Score: 23/30**

### Strengths

- Addresses an emerging cybersecurity challenge.
- Strong real-world importance for organizations with long-term sensitive data.
- Multi-cloud deployment provides a realistic technical environment.
- Dependency-aware and zero-downtime migration provides a meaningful engineering challenge.
- Strong potential for research involving cryptographic infrastructure and cloud security.

### Limitation

The major concern is **implementation complexity**.

The system would need to interact with multiple cloud key-management systems, cryptographic infrastructure, service dependencies, and potentially HSM environments.

This increases the complexity of developing and validating a convincing prototype within the available project timeline.

### Selection Decision

**Not selected.**

The project remains a strong future research direction, but its current feasibility is lower than the selected projects.

---

## Case Study 3 — Real-Time Deepfake Detection Gateway

**Score: 22/30**

### Strengths

- Addresses a rapidly growing cybersecurity threat.
- High potential real-world impact.
- Real-time detection and intervention provides a technically meaningful direction.
- Cloud media infrastructure provides a realistic deployment environment.

### Limitation

Deepfake detection is already a highly active research area.

Developing a reliable real-time detection system would also require significant work involving:

- Audio processing
- Video processing
- Machine learning models
- Real-time streaming
- Latency optimization
- False-positive reduction

Therefore, both novelty uncertainty and implementation complexity reduce its suitability for the current project.

### Selection Decision

**Not selected.**

The concept is valuable but was ranked below the two selected candidates.

---

# 4. Final Selection

Based on the scoring framework, the two highest-scoring case studies were:

| Rank | Case Study | Score | Decision |
|---|---|---:|---|
| 1 | Case Study 4 — API Aggregation-Inference Attack Detection | **26/30** | **Selected** |
| 1 | Case Study 5 — OT/IoT Anomaly-Driven Auto-Isolation | **26/30** | **Selected** |
| 3 | Case Study 1 — Cross-Tenant Ransomware Detection & Isolation | 24/30 | Not Selected |
| 4 | Case Study 2 — Post-Quantum Key Migration Orchestrator | 23/30 | Not Selected |
| 5 | Case Study 3 — Real-Time Deepfake Detection Gateway | 22/30 | Not Selected |

The two selected projects provide distinct but complementary cybersecurity research directions.

---

# 5. Selected Project 1 — TesseraGuard

## Aggregation-Aware API Threat Detection & Enforcement Gateway

**Origin:** Case Study 4 — API Aggregation-Inference Attack Detection

**Final Score:** 26/30

---

## 5.1 Problem Justification

Modern cloud applications are increasingly built using microservices that communicate through APIs.

Conventional API security controls generally evaluate requests individually.

For example:

API Request 1 → Authorized → ALLOW
API Request 2 → Authorized → ALLOW
API Request 3 → Authorized → ALLOW
API Request 4 → Authorized → ALLOW

Each request may be legitimate when examined independently.

However, an attacker using a compromised identity can deliberately divide a large-scale data extraction into many small operations.

For example:

20 records
    ↓
20 records
    ↓
20 records
    ↓
20 records
    ↓
   ...
    ↓
Large-scale data extraction

The security problem therefore exists at the combination level, rather than at the individual-request level.

**Core Problem**

How can a cloud security system identify when a sequence of individually authorized API operations collectively produces a potentially unauthorized or harmful outcome?

This makes the problem sufficiently specific for research and prototype development.

# 6. Selected Project 2 — ReflexGuard
##Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Origin:** Case Study 5 — OT/IoT Anomaly-Driven Auto-Isolation

**Final Score:** 26/30

## 6.1 Problem Justification

Industrial environments increasingly connect sensors, actuators, controllers, and monitoring systems to networked and cloud-connected infrastructure.

This connectivity creates a cybersecurity risk because compromising a connected device may have consequences beyond information loss.

A compromised device could potentially send an abnormal command to industrial equipment.

For example:

Compromised Industrial Device
            ↓
       Abnormal Command
            ↓
      Industrial Network
            ↓
     Actuator / Equipment
            ↓
   Potential Physical Impact

Traditional security systems may detect the anomaly and generate an alert, but an alert alone may not prevent the command from reaching the equipment.

**Core Problem**

How can an industrial cybersecurity system detect dangerous device behavior and automatically isolate the affected device quickly enough to prevent the abnormal command from reaching the control environment?

This creates a specific cybersecurity problem that can be researched, simulated, and measured.
