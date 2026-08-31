# Paper 2 — EcoDefender: Energy-Efficient Hybrid Anomaly Detection for IoT Edge Gateways

**Project:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Source:** arXiv, 2025

**Paper:** https://arxiv.org/abs/2511.18235

## What the Existing Solution Is

An anomaly detection system built specifically to run at the IoT edge gateway layer.

It uses a hybrid detection approach designed to balance accuracy against the limited compute and power budgets typical of edge hardware.

## Which Part Is Used in the Proposed Solution

The **energy-aware, edge-gateway-native architecture**.

ReflexGuard's **edge gateway signal collector** module is built on this paper's resource-efficiency principles rather than assuming unlimited compute is available at the edge.

## How It Is Useful

It validates ReflexGuard's core architectural decision — putting detection at the edge gateway, not in the cloud.

It also directly addresses a real constraint ReflexGuard will face: industrial edge gateways are often resource-limited.

Therefore, the detection engine needs to be efficient by design, not just accurate.
