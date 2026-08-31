# ReflexGuard — Literature Survey

**Project Title:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

## Literature Survey

The literature survey for ReflexGuard covers five papers related to Industrial IoT/OT security, edge-based intrusion detection, resource-efficient anomaly detection, streaming and unsupervised detection, explainability, and realistic evaluation of industrial security systems.

The reviewed papers provide the foundation for understanding existing approaches to industrial anomaly detection and help identify the research gap targeted by ReflexGuard.

## Literature Survey Table

| S.No. | Title of the Paper                                                                                 | Author(s)                                                                          | Published Year                                    | Advantages                                                                                                                     | Disadvantages                                                                                                                 |
| ----- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| 1     | Trustworthy Adaptive AI for Real-Time Intrusion Detection in Industrial IoT Security               | Al Rawajbeh, Maria Soosai, Ramasamy, Khan                                          | 2025                                              | High accuracy (96.4%), low false positives (2.1%), fast (35ms) on constrained edge hardware; explainable via SHAP              | Detects and alerts only — no automatic enforcement/isolation action; validated only on benchmark datasets, not a real factory |
| 2     | EcoDefender: Energy-Efficient Hybrid Anomaly Detection for IoT Edge Gateways                       | Saeid Jamshidi, Martine Bellaïche, Omar Abdul Wahab                                | 2025                                              | Resource/energy-efficient with low CPU and latency; provides strong theoretical guarantees including stability and convergence | Focused on detection/efficiency trade-off only, not response; may need retraining as traffic evolves                          |
| 3     | Real-Time Adaptive Anomaly Detection in Industrial IoT Environments                                | Mahsa Raeiszadeh, Amin Ebrahimzadeh, Roch H. Glitho, Johan Eker, Raquel A. F. Mini | 2024 (original IEEE TNSM; also on arXiv Jan 2026) | Handles multi-dimensional streaming data with concept-drift adaptation; no labeled retraining needed; approximately 89.71% AUC | No enforcement/isolation action; evaluated through trace-driven simulation, not shown in real industrial deployment           |
| 4     | Explainable Anomaly Detection for Industrial IoT Data Streams                                      | Ana Rita Paupério, Diogo Risca, Afonso Lourenço, Goreti Marreiros, Ricardo Martins | 2026                                              | Uses realistic delayed/absent-label assumptions; interpretable through Partial Dependence Plots and feature importance         | Relies on human-in-the-loop interaction for full effectiveness; no automatic isolation/enforcement action                     |
| 5     | Intrusion Detection Systems in Industrial Control Systems: Landscape, Challenges and Opportunities | Tong Wu, Dawei Zhou, Qingyu Ou, Fang Luo                                           | 2025/2026                                         | Very recent systematic literature review; covers real-industrial-scenario challenges                                           | Review only; proposes no new technique or enforcement mechanism of its own                                                    |

## Key Areas Identified

The literature survey identifies the following important areas for ReflexGuard:

* **Edge-Based Detection:** Security detection can be performed close to industrial devices.
* **Resource-Efficient Detection:** Detection systems must consider limited edge resources.
* **Streaming Detection:** Device behavior can be continuously analyzed as telemetry arrives.
* **Unsupervised Baseline Building:** Normal device behavior can be established without extensive labeled attack data.
* **Concept-Drift Adaptation:** Detection can adapt as device behavior changes over time.
* **Explainability:** Operators can understand why abnormal behavior was detected.
* **Realistic Evaluation:** Industrial detection systems must account for delayed or unavailable ground-truth labels.

## Literature-to-Project Contribution

The reviewed literature provides the foundation for the proposed ReflexGuard components:

**Device Telemetry → Edge Monitoring → Behavioral Baseline → Anomaly Detection → Risk Decision → Automatic Isolation → Cloud Notification**

The papers provide research support for edge-based detection, streaming analysis, resource-efficient anomaly detection, unsupervised learning, explainability, and Industrial IoT/OT security.

The central direction of ReflexGuard is to continuously monitor industrial device behavior at the edge and identify anomalies based on each device's established normal behavior.

ReflexGuard further focuses on connecting anomaly detection to an **automatic edge-level isolation action**, allowing a high-risk device to be disconnected from the control network instead of only generating an alert.

## Research Gap Identified

The literature consistently demonstrates strong capabilities in anomaly detection, edge processing, streaming analysis, explainability, and industrial intrusion detection.

However, the reviewed papers primarily focus on **detection, analysis, or alerting**, rather than connecting anomaly detection directly to **automatic edge-level isolation**.

The identified research direction for ReflexGuard is therefore:

**Edge-Based Anomaly Detection + Automatic Device Isolation**

This gap will be studied further during the subsequent design and implementation stages.

## Conclusion

The five papers provide the research foundation for ReflexGuard and support the development of its edge-native anomaly detection and automated isolation approach.

The literature survey will be used for the next stage of the project: **high-level architecture design, module identification, and prototype development.**
