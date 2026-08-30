# Project 1 Selected — API Aggregation-Inference Attack Detection

**Full name:** Runtime API Abuse & Business-Logic Attack Detection for Cloud-Native Microservices

**Selected over:** Case Study 1 (Cross-Tenant Ransomware Detection), Case Study 2 (PQC Migration Orchestrator), Case Study 3 (Deepfake Detection Gateway)

## Why this project was selected

### 1. Documented, not assumed, novelty

Most security tools evaluate each API request in isolation — is this one request allowed?

A recent paper on multi-agent authorization (**arXiv 2605.05440, May 2026**) explicitly names the gap this project targets: individually-authorized actions that **combine into an unauthorized outcome**, calling it **"aggregation inference,"** and states it remains largely unsolved.

Finding an explicit statement of an open problem in current research is stronger evidence of novelty headroom than any of the other 4 case studies could offer at this stage.

### 2. Broad applicability

Almost every modern cloud application is built from microservices communicating through APIs, which means this project's problem — and its eventual solution — is relevant far beyond one specific industry.

This makes it easier to demonstrate, evaluate, and justify to a broad audience (faculty, potential adopters, or future collaborators).

### 3. Real, defensible technical effect for India's patent requirements

The enforcement action — **throttling or blocking traffic live at the API gateway** — is a concrete network-layer action, not just a risk score or alert.

Under India's CRI Guidelines (Section 3(k)), this kind of measurable system action is what separates a patentable invention from an unpatentable "algorithm/business method."

### 4. Feasible to prototype within the available timeline

A working prototype can be built using simulated microservices and a standard API gateway (e.g. Kong, AWS API Gateway) without needing specialized hardware or a live production environment — unlike, for example, the OT/IoT project, which benefits from (but doesn't strictly require) physical or simulated industrial devices.

## Known risks to track going into Week 3–4

* The **"aggregation inference"** gap was found in the **multi-agent AI authorization** literature, not the general cloud API security literature — Week 3's literature survey needs to verify the gap holds in the API-security framing specifically, not just assume it transfers.

* The hardest open design question is the exact rule/threshold for **"this combination of otherwise-legitimate calls is dangerous"** — this needs to be defined precisely and tested against realistic legitimate bulk-access traffic (e.g. scheduled reporting jobs) to avoid a high false-positive rate.
