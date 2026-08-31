# Paper 3 — GAL-MAD: Towards Explainable Anomaly Detection in Microservice Applications Using Graph Attention Networks

**Project:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

**Source:** arXiv, April 2025

**Paper:** https://arxiv.org/pdf/2504.00058

## What the Existing Solution Is

A model called **GAL-MAD** that combines Graph Attention Networks with LSTM to detect anomalies in microservices.

It jointly models:

* Which services call which
* How each call behaves over time
* Structural signals
* Temporal and performance signals

The approach is also explainable, meaning it can point to which service and feature drove a flagged anomaly.

## Which Part Is Used in the Proposed Solution

The **graph-attention structural modeling technique and the explainability mechanism**.

TesseraGuard's **aggregation graph builder** module adopts the idea of representing calls as a graph with attention weighting.

The policy decision engine borrows the explainability approach to justify why a specific combination was flagged.

## How It Is Useful

It proves that combining structural, or who-calls-whom, and temporal signals in a single graph-based model works in practice.

This gives TesseraGuard a concrete technique to build its aggregation graph on rather than designing one from scratch.

The explainability piece is directly needed for TesseraGuard's audit and justification requirements.
