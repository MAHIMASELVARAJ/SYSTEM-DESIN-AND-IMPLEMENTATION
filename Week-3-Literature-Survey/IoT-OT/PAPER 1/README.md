# Paper 1 — Trustworthy Adaptive AI for Real-Time Intrusion Detection in Industrial IoT Security

**Project:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

**Source:** IoT journal, MDPI, 2025

**Paper:** https://doi.org/10.3390/iot6030053

## What the Existing Solution Is

A lightweight, adaptive intrusion detection system for Industrial IoT running an ensemble of online learning models directly on edge devices.

It uses SHAP explainability so operators can understand alert causes.

The paper reports:

* **96.4% accuracy**
* **2.1% false positives**
* **35ms detection time**

on resource-constrained edge hardware.

## Which Part Is Used in the Proposed Solution

The **edge-deployable detection model and its explainability layer**.

ReflexGuard's anomaly detection engine adopts the online-learning-on-constrained-hardware approach.

The policy decision engine adopts SHAP-style explainability for justifying isolation decisions.

## How It Is Useful

This gives ReflexGuard a proven, published performance benchmark — 35ms and 96.4% accuracy — to target on similarly constrained edge hardware.

It also provides a concrete explainability technique so an operator can understand why a device was isolated after the fact.

Its key limitation is that it detects and alerts but does not take an enforcement action.

This is exactly where ReflexGuard's own contribution begins.
