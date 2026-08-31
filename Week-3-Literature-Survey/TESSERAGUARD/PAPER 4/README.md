# Paper 4 — AI-Driven Anomaly Detection in Cloud-Native Microservices: The Night's Watch Algorithm

**Project:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

**Source:** Applied Sciences, MDPI, 2025

**Paper:** https://www.mdpi.com/2076-3417/15/23/12762

## What the Existing Solution Is

An unsupervised anomaly detection algorithm for cloud-native microservices.

It integrates multi-source data and temporal features without requiring labeled training data or fixed thresholds.

The approach achieves up to **92% precision in real-time detection**.

## Which Part Is Used in the Proposed Solution

The **unsupervised, threshold-free scoring approach**.

TesseraGuard's aggregation-risk inference engine adopts this style of scoring so it does not need pre-labeled examples of "this combination is an attack."

Such examples are rarely available for novel attack patterns.

## How It Is Useful

Attack combinations in TesseraGuard's threat model are highly varied and context-specific.

Therefore, a technique that does not require labeled examples of every possible bad combination is essential.

This paper's published precision numbers also give TesseraGuard a concrete benchmark to test against during evaluation.
