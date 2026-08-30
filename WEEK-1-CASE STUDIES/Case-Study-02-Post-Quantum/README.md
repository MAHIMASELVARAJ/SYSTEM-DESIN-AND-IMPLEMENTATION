**Case Study 2 — Migrating Cryptographic Keys to Post-Quantum Standards Without Downtime at [Illustrative: "Aravalli Financial Group"]**

**Executive Summary**

A financial services company operating across three cloud providers needs to migrate its
encryption keys to post-quantum-safe algorithms ahead of the quantum computing threat, but
cannot risk taking any customer-facing service offline during the transition. This case
study proposes an orchestrator that discovers every key across the company's multi-cloud
footprint, plans a safe migration order, and performs the re-keying with zero service
interruption.

**The Problem Statement**

Quantum computers, once sufficiently powerful, will be able to break the encryption
algorithms most organizations rely on today. Governments and standards bodies have already
finalized post-quantum-safe algorithms, and companies handling sensitive data are under
pressure to migrate. The challenge is not choosing new algorithms — it is the operational
complexity of doing so safely. A financial company's encryption keys live scattered across
several different cloud providers' key management systems, each with its own APIs and
conventions. A manual, uncoordinated migration risks locking services out of their own
encrypted data or causing outages during the cutover — both unacceptable for a company
handling financial transactions.

**The Solution**

An orchestration system that first inventories every cryptographic key across all connected
cloud accounts, classifies which are vulnerable to quantum attack, and builds a migration
plan that respects service dependencies (so a shared key isn't rotated while a dependent
service is still using the old one). The actual re-keying step is designed to run both old
and new keys in parallel briefly, so services can validate the new key before the old one is
retired — enabling a rotation with no observable downtime.

**The Implementation**

Build a scanner with read access to each cloud provider's key management service (KMS) to build a full key inventory.

Classify each key by algorithm type, flagging quantum-vulnerable ones.

Build a migration planner that sequences the rotation based on service dependency maps, avoiding any point where a service loses access to a valid key.

Generate new post-quantum keys through each provider's KMS/HSM.

Run a parallel-validity window: new key is issued and confirmed working before the old key is revoked.

Verify compatibility with every dependent service automatically before finalizing.

Log the full migration for compliance and audit purposes.

**Results (Target outcomes to validate during prototyping)**

Target: zero unplanned service downtime during a simulated multi-cloud migration of at least 3 interdependent services.

Target: full key inventory discovery across all connected cloud accounts within a defined time window (to be benchmarked, e.g. under 10 minutes for a mid-size account).

Target: 100% of migrated keys verified working by dependent services before old keys are revoked, in test runs.

**Conclusion / Takeaway**

The hard part of post-quantum migration isn't the cryptography — it's doing the swap safely
across a messy, multi-provider environment without breaking anything. An orchestrator that
treats dependency-aware, zero-downtime rotation as the core engineering problem (not just
"generate new keys") is the part worth building and proving out first.
