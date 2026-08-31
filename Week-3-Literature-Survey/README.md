# Week 3 — Literature Survey

## Overview

Week 3 focuses on conducting a literature survey for the two projects selected during Week 2:

1. **TesseraGuard** — Aggregation-Aware API Threat Detection & Enforcement Gateway
2. **ReflexGuard** — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

Five papers were reviewed for each project, giving a total of **10 research papers**.

The purpose of the literature survey is to understand existing approaches, identify their advantages and limitations, and determine the research gap that will guide the architecture and implementation of the selected projects.

---

# Project 1 — TesseraGuard

**Full Title:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

## Literature Survey

The TesseraGuard literature survey focuses on aggregation inference, API-call analysis, microservice anomaly detection, graph-based detection, unsupervised anomaly detection, and explainability.

| S.No. | Title of the Paper                                                                                         | Author(s)                                                                          | Published Year | Advantages                                                                                                               | Disadvantages                                                                                                                      |
| ----: | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | -------------: | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
|     1 | Authorization Propagation in Multi-Agent AI Systems: Identity Governance as Infrastructure                 | Tallam                                                                             |           2026 | Formally names and defines "aggregation inference"; gives strong theoretical grounding and a citable gap                 | Proposes no working algorithm; scoped only to multi-agent AI delegation, not general API security                                  |
|     2 | Anomaly Detection and Root Cause Analysis for Microservice Systems                                         | Luan Pham                                                                          |           2026 | Identifies API-call event data as an underexplored signal; does not need a pre-given service call graph                  | General anomaly/RCA focus, not authorization-specific; lacks standardized benchmark datasets                                       |
|     3 | GAL-MAD: Towards Explainable Anomaly Detection in Microservice Applications Using Graph Attention Networks | L. Akmeemana, C. Attanayake, H. Faiz, S. Wickramanayake                            |           2025 | Combines structural graph-attention and temporal LSTM signals; produces explainable, feature-level output                | Targets performance/response-time anomalies, not security attacks specifically; needs trace-level instrumentation, adding overhead |
|     4 | AI-Driven Anomaly Detection in Cloud-Native Microservices: The Night's Watch Algorithm                     | Dkmak, Can, Sevinc, Egeli, Baday, Cetintav                                         |           2025 | Unsupervised; no fixed thresholds or labels needed; up to 92% precision and real-time capable                            | Recall varies significantly, up to only 39% depending on training set size; not security-focused                                   |
|     5 | Anomaly Detection and Root-Cause Identification in Microservices: A Survey                                 | Luís M. Barata, Sérgio Sequeira, Eurico Lopes, Pedro R. M. Inácio, Mário M. Freire |           2026 | Comprehensive survey covering 117 studies from 2012–2025; rigorous PRISMA methodology; useful for landscape verification | Survey only; proposes no new technique; does not specifically address aggregation/combination-risk                                 |

## Research Gap — TesseraGuard

The reviewed literature provides approaches for API-call analysis, microservice anomaly detection, graph modeling, unsupervised detection, and explainability.

However, the reviewed papers do not directly provide the complete TesseraGuard approach of:

**Combination-Based API Risk Detection + Live API Gateway Enforcement**

The central direction of TesseraGuard is to identify when **individually authorized API actions combine into a potentially unauthorized outcome**, and then connect this combination-based risk detection to **live enforcement at the API gateway**.

---

# Project 2 — ReflexGuard

**Full Title:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

## Literature Survey

The ReflexGuard literature survey focuses on Industrial IoT/OT security, edge-based intrusion detection, resource-efficient anomaly detection, streaming data analysis, explainability, and industrial control system security.

| S.No. | Title of the Paper                                                                                 | Author(s)                                                                          |                                    Published Year | Advantages                                                                                                                     | Disadvantages                                                                                                                 |
| ----: | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
|     1 | Trustworthy Adaptive AI for Real-Time Intrusion Detection in Industrial IoT Security               | Al Rawajbeh, Maria Soosai, Ramasamy, Khan                                          |                                              2025 | High accuracy (96.4%), low false positives (2.1%), fast (35ms) on constrained edge hardware; explainable via SHAP              | Detects and alerts only — no automatic enforcement/isolation action; validated only on benchmark datasets, not a real factory |
|     2 | EcoDefender: Energy-Efficient Hybrid Anomaly Detection for IoT Edge Gateways                       | Saeid Jamshidi, Martine Bellaïche, Omar Abdul Wahab                                |                                              2025 | Resource/energy-efficient with low CPU and latency; provides strong theoretical guarantees including stability and convergence | Focused on detection/efficiency trade-off only, not response; may need retraining as traffic evolves                          |
|     3 | Real-Time Adaptive Anomaly Detection in Industrial IoT Environments                                | Mahsa Raeiszadeh, Amin Ebrahimzadeh, Roch H. Glitho, Johan Eker, Raquel A. F. Mini | 2024 (original IEEE TNSM; also on arXiv Jan 2026) | Handles multi-dimensional streaming data with concept-drift adaptation; no labeled retraining needed; approximately 89.71% AUC | No enforcement/isolation action; evaluated through trace-driven simulation, not shown in real industrial deployment           |
|     4 | Explainable Anomaly Detection for Industrial IoT Data Streams                                      | Ana Rita Paupério, Diogo Risca, Afonso Lourenço, Goreti Marreiros, Ricardo Martins |                                              2026 | Uses realistic delayed/absent-label assumptions; interpretable through Partial Dependence Plots and feature importance         | Relies on human-in-the-loop interaction for full effectiveness; no automatic isolation/enforcement action                     |
|     5 | Intrusion Detection Systems in Industrial Control Systems: Landscape, Challenges and Opportunities | Tong Wu, Dawei Zhou, Qingyu Ou, Fang Luo                                           |                                         2025/2026 | Very recent systematic literature review; covers real-industrial-scenario challenges                                           | Review only; proposes no new technique or enforcement mechanism of its own                                                    |

## Research Gap — ReflexGuard

The reviewed literature demonstrates strong capabilities in anomaly detection, edge processing, streaming analysis, explainability, and Industrial IoT/OT security.

However, the reviewed papers primarily focus on **detection, analysis, or alerting**, rather than connecting anomaly detection directly to **automatic edge-level isolation**.

The central direction of ReflexGuard is therefore:

**Edge-Based Anomaly Detection + Automatic Device Isolation**

The proposed approach focuses on detecting abnormal device behavior close to the industrial devices and automatically isolating a high-risk device at the edge rather than relying only on an alert or human response.

---

# Comparative Literature Analysis

| Aspect                     | TesseraGuard                                                                                         | ReflexGuard                                                                      |
| -------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Security Domain            | Cloud-native API and microservice security                                                           | Industrial IoT/OT security                                                       |
| Main Research Area         | API-call aggregation and combination risk                                                            | Industrial device anomaly detection                                              |
| Existing Detection Focus   | API events, microservice anomalies, graph and sequence analysis                                      | Edge anomaly detection, intrusion detection, streaming analysis                  |
| Major Limitation Observed  | Existing approaches do not directly address combination-based API risk with live gateway enforcement | Existing approaches primarily detect or alert without automatic device isolation |
| Proposed Enforcement Point | API Gateway                                                                                          | Edge Gateway                                                                     |
| Proposed Security Action   | Allow / Throttle / Block                                                                             | Allow / Alert / Isolate                                                          |
| Main Research Direction    | Combination-Based API Risk Detection + Live API Gateway Enforcement                                  | Edge-Based Anomaly Detection + Automatic Device Isolation                        |

---

# Overall Research Gap

The literature survey across both projects shows a common pattern:

**Existing research provides strong detection and analysis techniques, but automatic enforcement is not consistently integrated into the detection process.**

For **TesseraGuard**, the identified direction is to connect the detection of combinations of individually authorized API actions with **real-time API gateway enforcement**.

For **ReflexGuard**, the identified direction is to connect industrial device anomaly detection with **automatic edge-level device isolation**.

Therefore, the two projects focus on different cybersecurity layers while following a common security approach:

**Monitor → Analyze → Detect → Decide → Automatically Enforce**

---

# Conclusion

The literature survey of 10 papers provides the research foundation for the two selected projects.

**TesseraGuard** focuses on detecting dangerous combinations of individually authorized API calls and enforcing the resulting security decision at the API gateway.

**ReflexGuard** focuses on detecting anomalous Industrial IoT/OT device behavior and automatically isolating high-risk devices at the edge.

The identified research gaps will be carried forward into **Week 4 — High-Level Architecture Design and Module Identification**.
