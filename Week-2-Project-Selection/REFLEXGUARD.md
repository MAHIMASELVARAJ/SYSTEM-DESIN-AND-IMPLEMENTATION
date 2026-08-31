# Project 2 Selected — OT/IoT Anomaly-Driven Auto-Isolation

**Full name:** Anomaly-Driven Auto-Isolation for Cloud-Connected IoT/OT (Industrial Control) Devices

**Selected over:** Case Study 1 (Cross-Tenant Ransomware Detection), Case Study 2 (PQC Migration Orchestrator), Case Study 3 (Deepfake Detection Gateway)

## Why this project was selected

### 1. Strongest patentability story of all 5 case studies, specifically for India

India's 2025 Computer-Related Inventions (CRI) Guidelines explicitly list **"real-time monitoring and control"** and **"better control of physical equipment"** as examples of a qualifying technical effect under Section 3(k).

This project's central action — detecting an anomalous control signal and automatically disconnecting the device from the network before its command reaches physical machinery — matches that description almost directly.

This removes much of the ambiguity that makes most software inventions difficult to patent in India.

### 2. High real-world urgency and impact

Protecting industrial control systems and critical infrastructure is a stated national priority in India (see CERT-In and NCIIPC's mandates).

A successful attack here isn't just a data breach — it can cause physical safety incidents.

This gives the project real-world weight beyond an academic exercise.

### 3. Realistic feasibility using existing cloud IoT platforms

A working prototype does not require access to a real factory.

It can be built using cloud IoT platforms (e.g. AWS IoT Core, Azure IoT Hub) with simulated sensors and actuators, making the project buildable and testable within the available timeline while still representing the real architecture.

### 4. Complements Project 1 well

Project 1 (API Aggregation) addresses the **application/API layer** of cloud security.

This project addresses the **physical/OT layer**.

Presenting both together shows breadth across two meaningfully different layers of the cybersecurity stack, rather than two variations on the same idea.

## Known risks to track going into Week 3–4

* General OT/ICS security research is well-established; the literature survey needs to confirm the specific **"cloud-managed, edge-enforced, automatic isolation"** framing is narrower and less covered than OT anomaly detection research in general.

* The exact rule for scoring **"how physically dangerous is this anomaly"** (not just "how statistically unusual is it") is the hardest design decision and needs domain input — a purely statistical anomaly score risks false isolations during legitimate but rare events, like planned maintenance.

* Simulated devices in a prototype will not fully capture the real-time constraints and protocol quirks (e.g. Modbus, OPC-UA) of real industrial equipment — this should be stated clearly as a scope limitation in any writeup.
