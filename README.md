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
# WEEK 3 - 📚 TesseraGuard – Literature Survey

A literature survey was conducted to understand existing research related to anomaly detection, microservice systems, API-call analysis, and aggregation inference.

Five papers were analyzed.
| S.No | Paper                                                                                                      | Author(s)                                                                          | Year | Advantages                                                                                                    | Disadvantages                                                                                                          |
| ---- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---: | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1    | Authorization Propagation in Multi-Agent AI Systems: Identity Governance as Infrastructure                 | Tallam                                                                             | 2026 | Formally names and defines "aggregation inference"; provides theoretical grounding and a citable research gap | Does not propose a working algorithm; scoped to multi-agent AI delegation rather than general API security             |
| 2    | Anomaly Detection and Root Cause Analysis for Microservice Systems                                         | Luan Pham                                                                          | 2026 | Identifies API-call event data as an underexplored signal; does not require a pre-given service call graph    | General anomaly/RCA focus rather than authorization-specific security; lacks standardized benchmark datasets           |
| 3    | GAL-MAD: Towards Explainable Anomaly Detection in Microservice Applications Using Graph Attention Networks | L. Akmeemana, C. Attanayake, H. Faiz, S. Wickramanayake                            | 2025 | Combines structural graph-attention and temporal LSTM signals; provides explainable feature-level output      | Focuses on performance/response-time anomalies rather than security attacks; trace-level instrumentation adds overhead |
| 4    | AI-Driven Anomaly Detection in Cloud-Native Microservices: The Night's Watch Algorithm                     | Dkmak, Can, Sevinc, Egeli, Baday, Cetintav                                         | 2025 | Unsupervised approach; does not require fixed thresholds or labels; real-time capable                         | Recall varies significantly; not specifically security-focused                                                         |
| 5    | Anomaly Detection and Root-Cause Identification in Microservices: A Survey                                 | Luís M. Barata, Sérgio Sequeira, Eurico Lopes, Pedro R. M. Inácio, Mário M. Freire | 2026 | Comprehensive survey covering 117 studies using rigorous PRISMA methodology                                   | Survey only; does not specifically address aggregation/combination-risk detection                                      |
# 📚 ReflexGuard – Literature Survey
A literature survey was conducted to understand existing research related to industrial IoT security, anomaly detection, edge environments, intrusion detection, and industrial control systems.

Five papers were analyzed.
| S.No | Paper                                                                                              | Author(s)                                                                          |      Year | Advantages                                                                                                    | Disadvantages                                                                                                     |
| ---- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------: | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| 1    | Trustworthy Adaptive AI for Real-Time Intrusion Detection in Industrial IoT Security               | Al Rawajbeh, Maria Soosai, Ramasamy, Khan                                          |      2025 | High accuracy, low false positives, fast performance on constrained edge hardware; explainable using SHAP     | Detects and alerts only; no automatic enforcement/isolation; evaluated on benchmark datasets                      |
| 2    | EcoDefender: Energy-Efficient Hybrid Anomaly Detection for IoT Edge Gateways                       | Saeid Jamshidi, Martine Bellaïche, Omar Abdul Wahab                                |      2025 | Resource and energy efficient; low CPU and latency; provides theoretical stability and convergence guarantees | Focuses on detection and efficiency rather than response; may require retraining as traffic evolves               |
| 3    | Real-Time Adaptive Anomaly Detection in Industrial IoT Environments                                | Mahsa Raeiszadeh, Amin Ebrahimzadeh, Roch H. Glitho, Johan Eker, Raquel A. F. Mini |      2024 | Handles multi-dimensional streaming data; adapts to concept drift; does not require labeled retraining        | No enforcement/isolation action; evaluated through trace-driven simulation rather than real industrial deployment |
| 4    | Explainable Anomaly Detection for Industrial IoT Data Streams                                      | Ana Rita Paupério, Diogo Risca, Afonso Lourenço, Goreti Marreiros, Ricardo Martins |      2026 | Considers delayed/absent labels; provides interpretable feature importance and Partial Dependence Plots       | Relies on human-in-the-loop interaction; no automatic isolation/enforcement action                                |
| 5    | Intrusion Detection Systems in Industrial Control Systems: Landscape, Challenges and Opportunities | Tong Wu, Dawei Zhou, Qingyu Ou, Fang Luo                                           | 2025/2026 | Recent systematic literature review covering real industrial scenario challenges                              | Review only; does not propose a new enforcement mechanism                                                         |
# 🏗️ Week 4 – High-Level System Design

After completing the literature survey, high-level architectures were designed for both selected projects.

## TesseraGuard Architecture

┌─────────────────┐

│   API Gateway     │

│ Every API Call    │

└────────┬────────┘

         ↓
┌─────────────────┐
│  Caller Binder  │
│ Caller + Session│
└────────┬────────┘
         ↓
┌─────────────────┐
│  Call Collector │
│ History over    │
│      Time       │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Graph Builder  │
│ Data / Volume / │
│      Speed      │
└────────┬────────┘
         ↓
┌─────────────────┐
│   Risk Engine   │
│ Risky Call      │
│ Combinations    │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Policy Engine  │
│ Allow / Throttle│
│     / Block     │
└────────┬────────┘
         ↓
┌─────────────────┐
│   Enforcement   │
│ Real-Time API   │
│     Control     │
└────────┬────────┘
         ↓
┌─────────────────┐
│    Audit Log    │
│ What & Why      │
└─────────────────┘
## ReflexGuard Architecture
┌─────────────────┐
│   OT/IoT        │
│    Devices      │
│Sensors/Actuators│
└────────┬────────┘
         ↓
┌─────────────────┐
│ Edge Collector  │
│ Local Real-Time │
│ Signal Capture  │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Baseline Model  │
│ Normal Range    │
│   Per Device    │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Anomaly Engine  │
│ Detects         │
│ Deviations      │
└────────┬────────┘
         ↓
┌─────────────────┐
│   Risk Scorer   │
│ Equipment /     │
│ Process Harm    │
└────────┬────────┘
         ↓
┌─────────────────┐
│   Edge Policy   │
│ Allow / Alert / │
│     Isolate     │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Auto-Isolation │
│ Cuts Device Off │
│ Before Signal   │
│     Reaches     │
│    Equipment    │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Ops Dashboard   │
│ Notify Operator │
│ Log Incident    │
└─────────────────┘
