# Paper 3 — Real-Time Adaptive Anomaly Detection in Industrial IoT Environments

**Project:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Source:** arXiv, 2026

**Paper:** https://arxiv.org/abs/2601.03085

## What the Existing Solution Is

An online, unsupervised anomaly detection approach for streaming IIoT telemetry.

It uses stream-based clustering to detect abnormal device behavior as data arrives, without retraining on labeled historical data.

## Which Part Is Used in the Proposed Solution

The **streaming, unsupervised baseline-building technique**.

ReflexGuard's anomaly detection engine adopts this approach to build a **"normal behavior" baseline per device** without needing extensive labeled attack data for every device type.

## How It Is Useful

Real factories rarely have labeled attack data for every sensor or actuator type they deploy.

This paper's streaming, label-free approach is directly applicable to how ReflexGuard learns what **"normal"** looks like for each device.

Its industrial-research funding context, an Ericsson/ENCQOR-5G edge computing chair, adds real infrastructure-level credibility.
