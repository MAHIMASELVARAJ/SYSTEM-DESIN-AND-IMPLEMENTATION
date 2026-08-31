# Paper 2 — Anomaly Detection and Root Cause Analysis for Microservice Systems

**Project:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

**Author:** Luan Pham

**Source:** arXiv, June 2026

**Paper:** https://arxiv.org/pdf/2606.09942

## What the Existing Solution Is

A paper that surveys five shared limitations of current microservice anomaly detection methods, and proposes an integrated approach addressing them.

It notably points out that most tools rely on metrics, logs, and traces while API-call-level event data remains underused, and that many require a pre-given service call graph.

## Which Part Is Used in the Proposed Solution

The **event-data framing and the call-sequence collection approach**.

TesseraGuard treats raw API call events, rather than just aggregate metrics or traces, as the primary signal.

It also adopts the idea of constructing a call graph from observed behavior rather than assuming one exists in advance.

## How It Is Useful

It directly supports TesseraGuard's **call sequence collector** module and validates the project's choice to work from raw API-call events rather than higher-level metrics.

It also independently confirms, from a June 2026 paper, that this specific angle is underexplored — strengthening the novelty case for TesseraGuard's approach.
