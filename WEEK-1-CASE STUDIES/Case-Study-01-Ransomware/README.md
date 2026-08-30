**Case Study 1 — Stopping Ransomware From Spreading Across Cloud Tenants at [Illustrative: "MeridianCloud Storage"]**

**Executive Summary**

A mid-size multi-tenant cloud storage provider faces a growing risk: ransomware infecting
one customer's storage account can spread sideways into other customers sharing the same
underlying infrastructure. This case study proposes a system that watches storage write
patterns across tenants in real time, detects the specific signature of ransomware spreading
between accounts, and automatically isolates the affected storage segment — before human
responders can even open a ticket.

**The Problem Statement**

Cloud storage providers host many different customers (tenants) on shared infrastructure.
Existing ransomware detection tools typically watch one storage volume at a time, looking
for a single account's files being rapidly encrypted. They are not designed to catch
ransomware jumping from one tenant's storage into another's — a distinct and more
dangerous failure mode, since a single compromised account can put every neighboring tenant
at risk. For a provider hosting hundreds of business customers, even one successful
cross-tenant spread event could mean simultaneous data loss for many companies at once and
serious reputational and legal exposure.

**The Solution**

A cross-tenant correlation engine sits above individual per-tenant monitoring. Instead of
asking "is this one volume being encrypted abnormally fast?", it asks "are multiple tenants
showing correlated, unusual write patterns at the same time, in a way that suggests one
infection spreading between them?" When that cross-tenant signature is detected, the system
doesn't just alert a security analyst — it automatically severs network access to the
affected storage segment and triggers a snapshot rollback, containing the spread within
seconds rather than the hours a manual response would take.

**The Implementation**

Deploy lightweight I/O pattern collectors on each storage node to stream write metadata (not file contents) to a central analysis service.

Build the cross-tenant correlation engine to compare patterns across tenants sharing infrastructure, flagging statistically unusual simultaneous encryption-like activity.

Feed correlated signals into a risk-scoring model trained on known ransomware I/O signatures (rapid rewrite, file renaming, entropy spikes).

Connect the risk score to a policy engine that decides Allow / Alert / Isolate.

Wire the "Isolate" decision directly into the cloud storage control plane so isolation and snapshot rollback happen automatically, without waiting for human approval.

Log every decision for audit and post-incident review.

**Results (Target outcomes to validate during prototyping)**

Target: detect cross-tenant spread within under 60 seconds of the second tenant's infection beginning (to be measured against a simulated multi-tenant test environment).

Target: reduce the number of tenants affected by a single ransomware event from "all tenants on shared infrastructure" to "the originally infected tenant only," in simulated attack scenarios.

Target: keep false-positive isolation events below an agreed threshold (e.g. under 1 per 1,000 legitimate high-write-volume events, such as backups) — this needs real testing data to set correctly.

**Conclusion / Takeaway**
Watching individual storage volumes in isolation misses the specific danger of shared cloud
infrastructure: one infection becoming everyone's problem. Treating cross-tenant correlation
as its own detection layer, tied to an automatic (not just advisory) isolation action, is the
core idea worth prototyping and testing rigorously before claiming it as a finished solution.
