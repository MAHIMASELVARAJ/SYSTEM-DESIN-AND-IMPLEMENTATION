**Case Study 5 — Cutting Off a Hacked Sensor Before It Damages Equipment at [Illustrative: "Northbridge Manufacturing"]**

**Executive Summary**

A manufacturing plant connecting its industrial sensors and actuators to the cloud for
monitoring faces a serious risk: a compromised device could send a dangerous command to
physical machinery. This case study proposes an edge-based system that detects abnormal
device behavior in real time and automatically isolates the compromised device from the
control network before its command can reach the equipment.

**The Problem Statement**

Industrial IoT and operational technology (OT) devices — sensors, valves, actuators — are
increasingly connected to cloud dashboards for monitoring and management. This connectivity
creates a new attack surface: if an attacker compromises a device's cloud connection, they
could issue commands the device has never issued before, potentially causing physical damage
or a safety incident, not just a data breach. Cloud-based monitoring alone is often too slow
to prevent harm, since a command sent from a compromised device can reach physical equipment
before a distant cloud service even finishes analyzing it.

**The Solution**

An edge gateway, physically close to the devices themselves, continuously compares each
device's current behavior against its established normal pattern — the type of readings it
sends, the commands it's authorized to issue, and its typical operating ranges. When a device
does something it has never done before, or something physically dangerous given the current
process state, the system scores the risk and, for high-risk cases, immediately disconnects
that specific device from the control network at the edge — before its command can reach the
physical machinery — while notifying operators through the cloud dashboard in parallel.

**The Implementation**

Deploy an edge gateway close to the physical devices to minimize detection-to-action latency.

Build a behavioral baseline for each device type (normal signal ranges, command vocabulary, timing patterns).

Build an anomaly detection engine comparing live signals against each device's baseline.

Build a physical-risk scorer that weighs anomalies by their potential real-world consequence, not just statistical rarity.

Connect high-risk anomalies to an automatic network segmentation action at the edge gateway, isolating the device immediately.

Feed all events to a cloud dashboard for operator visibility and incident logging.

**Results (Target outcomes to validate during prototyping)**

Target: isolate a compromised device within a defined short window (e.g. under 500 milliseconds) of an anomalous command being issued, tested in a simulated OT environment.

Target: zero anomalous commands reaching a simulated physical actuator in red-team test scenarios, compared to a baseline with cloud-only (non-edge) detection.

Target: acceptable false-isolation rate on normal but rare events (e.g. planned maintenance mode) — needs real testing to calibrate correctly.

**Conclusion / Takeaway**

In industrial settings, detecting a threat isn't enough if the response is too slow to stop
physical harm. Putting the detection and the automatic isolation action at the edge, close to
the device itself, is what turns this into a genuinely protective system rather than just an
alerting one.
