# TesseraGuard — Literature Survey

**Project Title:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

## Literature Survey

The literature survey for TesseraGuard covers five papers related to aggregation inference, API-call analysis, microservice anomaly detection, graph-based detection, unsupervised anomaly detection, and explainability.

The reviewed papers provide the foundation for understanding existing approaches to API and microservice security and help identify the research gap targeted by TesseraGuard.

## Literature Survey Table

| S.No. | Title of the Paper                                                                                         | Author(s)                                                                          | Published Year | Advantages                                                                                                               | Disadvantages                                                                                                                      |
| ----- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 1     | Authorization Propagation in Multi-Agent AI Systems: Identity Governance as Infrastructure                 | Tallam                                                                             | 2026           | Formally names and defines "aggregation inference"; gives strong theoretical grounding and a citable gap                 | Proposes no working algorithm; scoped only to multi-agent AI delegation, not general API security                                  |
| 2     | Anomaly Detection and Root Cause Analysis for Microservice Systems                                         | Luan Pham                                                                          | 2026           | Identifies API-call event data as an underexplored signal; does not need a pre-given service call graph                  | General anomaly/RCA focus, not authorization-specific; lacks standardized benchmark datasets                                       |
| 3     | GAL-MAD: Towards Explainable Anomaly Detection in Microservice Applications Using Graph Attention Networks | L. Akmeemana, C. Attanayake, H. Faiz, S. Wickramanayake                            | 2025           | Combines structural graph-attention and temporal LSTM signals; produces explainable, feature-level output                | Targets performance/response-time anomalies, not security attacks specifically; needs trace-level instrumentation, adding overhead |
| 4     | AI-Driven Anomaly Detection in Cloud-Native Microservices: The Night's Watch Algorithm                     | Dkmak, Can, Sevinc, Egeli, Baday, Cetintav                                         | 2025           | Unsupervised; no fixed thresholds or labels needed; up to 92% precision and real-time capable                            | Recall varies significantly, up to only 39% depending on training set size; not security-focused                                   |
| 5     | Anomaly Detection and Root-Cause Identification in Microservices: A Survey                                 | Luís M. Barata, Sérgio Sequeira, Eurico Lopes, Pedro R. M. Inácio, Mário M. Freire | 2026           | Comprehensive survey covering 117 studies from 2012–2025; rigorous PRISMA methodology; useful for landscape verification | Survey only; proposes no new technique; does not specifically address aggregation/combination-risk                                 |

## Key Areas Identified

The literature survey identifies the following important areas for TesseraGuard:

* **Aggregation Inference:** Individually authorized actions can combine into an unauthorized outcome.
* **API-Call Analysis:** API-call event data can be used as an important security signal.
* **Call-Sequence Modeling:** API interactions can be collected and analyzed as sequences.
* **Graph-Based Detection:** Structural and temporal relationships between services can be modeled using graphs.
* **Unsupervised Detection:** Anomaly detection can be performed without requiring labeled examples for every attack.
* **Explainability:** Detection decisions can provide understandable information for security operators.

## Literature-to-Project Contribution

The reviewed literature provides the foundation for the proposed TesseraGuard components:

**API Events → Call Sequence → Aggregation Graph → Combination Risk Analysis → Policy Decision → Gateway Enforcement**

The papers provide theoretical grounding and existing techniques for analyzing API events, microservice relationships, anomalies, and explainability.

The central direction of TesseraGuard is to treat a **combination of individually authorized API actions as a security risk**, rather than evaluating every API request independently.

TesseraGuard further focuses on connecting this combination-based risk detection to **live enforcement at the API gateway**, where suspicious activity can be throttled or blocked.

## Research Gap Identified

The literature consistently demonstrates strong capabilities in detection, anomaly analysis, graph modeling, and explainability.

However, the reviewed papers do not directly provide the complete TesseraGuard approach of:

**Combination-Based API Risk Detection + Live API Gateway Enforcement**

This identified gap will be studied further during the subsequent design and implementation stages.

## Conclusion

The five papers provide the research foundation for TesseraGuard and support the development of its aggregation-aware API security approach.

The literature survey will be used for the next stage of the project: **high-level architecture design, module identification, and prototype development.**
