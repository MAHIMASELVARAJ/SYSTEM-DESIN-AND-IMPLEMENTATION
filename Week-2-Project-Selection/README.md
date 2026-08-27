# Week 2 – High-Level Project Selection

## Cybersecurity and Digital Trust

### Objective

The objective of Week 2 is to analyze the five cybersecurity and
digital trust case studies identified during Week 1 and select two
projects for detailed high-level system design.

The projects were evaluated based on:

- Real-world problem significance
- Cybersecurity relevance
- Digital trust contribution
- Technical complexity
- Innovation potential
- Cloud deployment feasibility
- Scalability
- Practical implementation feasibility
- Research potential
- Prior-art landscape
- Potential for developing a differentiated technical mechanism

---

# Evaluation of the Five Case Studies

| Project | Real-World Impact | Design Scope | Cloud Feasibility | Innovation Opportunity | Overall |
|---|---|---|---|---|---|
| ProofPulse | Very High | Very High | Very High | High | Selected |
| AgentGuard | Very High | Very High | Very High | Very High | Selected |
| DeepShield | Very High | High | Very High | Medium | Not Selected |
| DataLeak Sentinel | Very High | High | Very High | Medium | Not Selected |
| TrustBridge | High | High | Very High | Medium | Not Selected |

---

# Selected Project 1 – AgentGuard

## Purpose-Bound Security Firewall for Autonomous AI Agents

### Problem

Autonomous AI agents can interact with APIs, databases, files,
applications and other digital resources.

A user may authorize an AI agent to perform a specific task, but
the agent may execute additional actions that go beyond the
original human intention.

Therefore, there is a need for a security mechanism that can
continuously determine whether each AI-agent action remains
within the boundaries of the original authorization.

### Proposed Solution

AgentGuard is proposed as a cloud-based security control layer
between autonomous AI agents and enterprise resources.

It evaluates:

- Human authorization
- Agent identity
- Original user intent
- Requested action
- Target resource
- Permission scope
- Action sequence
- Data sensitivity
- Current security context

The system can respond with:

**ALLOW / VERIFY / BLOCK**

### High-Level Innovation Direction

The project will investigate a:

**Purpose-Bound Execution Envelope**

The envelope can contain:

- Authorized purpose
- Permitted resources
- Permitted operations
- Data-access limitations
- Transaction limitations
- Time restrictions

Each subsequent AI-agent action is evaluated against this
purpose-bound envelope.

### Core Flow

Human Intent
→ AI Agent
→ AgentGuard
→ Action Verification
→ Policy Decision
→ Allow / Verify / Block
→ Enterprise Resource

### Cloud Deployment

The proposed system can be deployed using:

- Cloud API Gateway
- Agent Security Gateway
- Intent Analysis Service
- Authorization Engine
- Policy Engine
- Risk Engine
- Event Processing
- Database
- Audit Logging
- Security Dashboard

### Why Selected

AgentGuard has strong potential for a high-level cybersecurity
architecture because autonomous AI security is an emerging area.
It also provides significant scope for cloud deployment,
security policies, AI integration, monitoring and research.

### Patent Potential

The overall concept is not claimed as automatically patentable.
The project will require detailed prior-art analysis to identify
a specific technical mechanism that is novel and non-obvious.

The intended research direction is the combination of
purpose-bound authorization with continuous verification of
AI-agent execution and action lineage.

---

# Selected Project 2 – ProofPulse

## Stateful Action-Level Dynamic Trust Verification

### Problem

Traditional authentication establishes the identity of a user,
but an authenticated session may later be compromised or
misused.

An attacker controlling a valid session could perform sensitive
operations such as accessing confidential data, changing
privileges or initiating high-risk transactions.

Therefore, there is a need to determine whether the specific
action being performed should be trusted at that moment.

### Proposed Solution

ProofPulse is proposed as a cloud-based action-level trust
verification platform.

The system evaluates:

- User identity
- Device context
- Location/environment
- Behaviour
- Session history
- Action sensitivity
- Resource sensitivity
- Action sequence

The resulting decision can be:

**ALLOW / VERIFY / BLOCK**

### High-Level Innovation Direction

The project will investigate a:

**Trust Transition Graph**

Instead of evaluating every request as an isolated risk score,
the system represents user activity as a sequence of trust-state
transitions.

Example:

Normal Login
→ Normal Activity
→ New Device
→ Privilege Escalation
→ Sensitive Data Access
→ External Transfer

The accumulated transition pattern can trigger adaptive
verification or temporary action blocking.

### Core Flow

User
→ Application
→ API Gateway
→ Action Capture
→ Trust Transition Engine
→ Policy Decision
→ Allow / Verify / Block
→ Audit & Monitoring

### Cloud Deployment

The proposed system can be deployed using:

- API Gateway
- Authentication Service
- Event Collector
- Behaviour Analytics
- Trust Transition Engine
- Policy Engine
- PostgreSQL
- Redis/Event Streaming
- Audit Service
- Security Dashboard
- Cloud Monitoring

### Why Selected

ProofPulse provides strong scope for a high-level Zero Trust
architecture and can be implemented as a cloud-native security
service.

It addresses the practical problem of authenticated-session
misuse while providing opportunities for behavioural analysis,
adaptive security and real-time decision making.

### Patent Potential

The broad concept of continuous risk-based authentication
already has significant prior art.

Therefore, the project will not claim dynamic trust scoring itself
as novel.

The intended research direction is a stateful trust-transition
mechanism that uses the evolution and relationship of privileged
actions to determine the required assurance level for the next
action.

---

# Why These Two Projects Were Selected

The two selected projects provide complementary approaches to
digital trust.

### AgentGuard

Focuses on:

**Trust in Autonomous AI Actions**

### ProofPulse

Focuses on:

**Trust in Human/User Actions**

Together they form a broader project theme:

> Adaptive Digital Trust for Human and Autonomous Digital Actors

---

# Final Selection

## 1. AgentGuard
**Purpose-Bound Security Firewall for Autonomous AI Agents**

## 2. ProofPulse
**Stateful Action-Level Dynamic Trust Verification**

These two projects will proceed to the next stage of detailed
system design, prior-art analysis, threat modelling and cloud
architecture.

---

## Important Note on Patentability

The selected projects are considered **potential innovation
candidates**, not confirmed patentable inventions.

Before claiming patentability, a detailed search of:

- Existing patents
- Patent applications
- Research publications
- Existing products
- Open-source implementations
- Standards

will be performed.

The final project will focus on a specific technical mechanism
that demonstrates novelty, technical contribution and practical
implementation potential.
