# Paper 4 — Explainable Anomaly Detection for Industrial IoT Data Streams

**Project:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Source:** ACM SAC '26, arXiv, 2026

**Paper:** https://arxiv.org/abs/2512.08885

## What the Existing Solution Is

A data-stream anomaly detection method designed for the realistic case where ground-truth labels are delayed or unavailable.

Unlike most methods, which unrealistically assume instant labeled feedback, this approach remains explainable to operators.

## Which Part Is Used in the Proposed Solution

The **delayed/absent-label evaluation approach**.

ReflexGuard's testing and validation methodology adopts this paper's realistic assumption: confirmation of whether a flagged anomaly was a true attack will not arrive immediately, if at all.

## How It Is Useful

This shapes how ReflexGuard should actually be tested.

The system should not be evaluated against an idealized, fully labeled dataset, but under the same delayed-label conditions a real factory deployment would face.

Building this into the evaluation plan early avoids over-optimistic results later.
