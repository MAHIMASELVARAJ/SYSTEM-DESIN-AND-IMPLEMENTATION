**Case Study 4 — Spotting an Attack Made of Many "Innocent" API Calls at [Illustrative: "Solace Retail Platform"]**

**Executive Summary**

A cloud-native e-commerce platform built from many small microservices is vulnerable to a
subtle attack pattern: a compromised employee account making many individually-authorized
API requests that, combined, add up to a large-scale data exfiltration — without ever
tripping a single-request security check. This case study proposes a system that models
combinations of API calls, not just individual ones, and intervenes at the API gateway when
a dangerous combination is detected.

**The Problem Statement**

Modern applications are built from many microservices talking to each other through APIs.
Security tools typically check each API request in isolation: is this specific request
authorized? But a sophisticated attacker doesn't need an unauthorized request — they can
issue many small, individually-legitimate requests over time that together reveal or extract
far more than any single request should. A compromised login pulling 20 customer records at
a time, repeated dozens of times over a few hours, looks completely normal request-by-request
but adds up to a full data breach. Existing per-request security controls have no way to
catch this pattern.

**The Solution**

A system that tracks the sequence and combination of API calls per identity (user or service
account) over time, builds a live picture of what data and access that identity has
accumulated, and flags when that accumulated picture crosses a risk threshold that no single
request would trigger. When flagged, the system throttles or blocks further requests from
that identity directly at the API gateway — the same checkpoint every request already passes
through — stopping the exfiltration mid-attack rather than only reporting it afterward.

**The Implementation**

Instrument the API gateway to log every request with identity, resource accessed, and data volume/sensitivity.

Build a call sequence collector that maintains a rolling, per-identity history.

Build an aggregation graph modeling how an identity's individual calls combine — total data touched, sensitivity, and rate of accumulation.

Build an inference engine that flags combinations exceeding defined safe-scope thresholds, even when every individual call was authorized.

Connect flagged combinations to a policy engine (Allow / Throttle / Block).

Enforce the decision live at the API gateway.

Log the full sequence and decision for security review.

**Results (Target outcomes to validate during prototyping)**

Target: detect a simulated "many small legitimate-looking requests add up to a breach" attack scenario that a per-request-only baseline system misses.

Target: keep added latency per legitimate API request within an acceptable bound (e.g. under a few milliseconds) so normal traffic isn't noticeably slowed.

Target: define and test an acceptable false-positive rate against realistic legitimate bulk-access patterns (e.g. a scheduled reporting job), since this is the hardest tuning challenge for this project.

**Conclusion / Takeaway**

Individually-authorized actions can still add up to something dangerous — and most security
tools aren't built to notice that. Building the "combination risk" model and tying it to
real, live enforcement at the gateway (not just an alert) is the genuinely new engineering
problem here, and it needs careful testing against real traffic patterns to get the
false-positive rate right.
