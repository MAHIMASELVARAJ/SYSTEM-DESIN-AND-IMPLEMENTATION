# 2. ReflexGuard — `README.md`

# ReflexGuard — High-Level Workflow

**Project Title:** ReflexGuard — Edge-Native Anomaly Detection & Automated Isolation for Industrial IoT/OT

## Overview

ReflexGuard is designed as an edge-based cybersecurity workflow for monitoring OT/IoT devices such as sensors and actuators.

The system captures device signals locally in real time, learns the normal range for each device, detects deviations from the established baseline, evaluates the potential harm to equipment or processes, and automatically isolates the device when required.

## High-Level Workflow

OT/IoT Devices
     ↓
Edge Collector
     ↓
Baseline Model
     ↓
Anomaly Engine
     ↓
Risk Scorer
     ↓
Edge Policy
     ↓
Auto-Isolation
     ↓
Ops Dashboard
## System Modules
**1. OT/IoT Devices**

Purpose: Sensors and actuators report or receive data.

The OT/IoT devices form the starting point of the workflow. Sensors and actuators continuously report or receive data.

**2. Edge Collector**

Purpose: Captures signals locally in real time.

The edge collector receives and captures device signals close to the OT/IoT devices, allowing the signals to be monitored locally and in real time.

**3. Baseline Model**

Purpose: Learns the normal range for each device.

The baseline model establishes the normal operating range for individual devices based on their signals and behavior.

**4. Anomaly Engine**

Purpose: Flags deviations from the baseline.

The anomaly engine compares the current device signals against the established baseline and identifies deviations.

**5. Risk Scorer**

Purpose: Weighs potential harm to equipment or the process.

The risk scorer evaluates an identified anomaly based on its potential effect on equipment or the industrial process.

**6. Edge Policy**

Purpose: Decides the required security action.

The edge policy determines whether the device should be:

Allow
Alert
Isolate
**7. Auto-Isolation**

Purpose: Cuts the device off before the signal reaches the equipment.

When isolation is required, the auto-isolation module cuts the device off before its signal can reach the equipment.

This provides the automatic response stage of the ReflexGuard workflow.

**8. Ops Dashboard**

Purpose: Notifies the operator and logs the incident.

The operations dashboard provides operator notification and records the incident for further review.

## Complete Data Flow
1. OT/IoT Devices
   ↓
2. Edge Collector
   ↓
3. Baseline Model
   ↓
4. Anomaly Engine
   ↓
5. Risk Scorer
   ↓
6. Edge Policy
   ↓
7. Auto-Isolation
   ↓
8. Ops Dashboard
## Core Concept

The core workflow of ReflexGuard is:

Capture device signals → Learn normal behavior → Detect deviation → Evaluate potential harm → Apply edge policy → Automatically isolate when required → Notify operator and log incident

The workflow focuses on detecting anomalous device behavior and connecting the detection directly to an automatic isolation action at the edge.

## High-Level Module List
**S.No.	Module	Main Function**

1	OT/IoT Devices	Sensors and actuators report/receive data

2	Edge Collector	Captures signals locally in real time

3	Baseline Model	Learns normal range per device

4	Anomaly Engine	Flags deviation from baseline

5	Risk Scorer	Weighs harm to equipment/process

6	Edge Policy	Decides Allow / Alert / Isolate

7	Auto-Isolation	Cuts device off before signal lands

8	Ops Dashboard	Notifies operator and logs incident

## Expected Security Flow
Device Signal
    ↓
Local Edge Collection
    ↓
Compare With Normal Baseline
    ↓
Detect Anomaly
    ↓
Evaluate Risk to Equipment/Process
    ↓
Policy Decision
    ↓
Allow / Alert / Isolate
    ↓
Notify Operator & Log Incident
## Architecture Direction

The high-level architecture is designed around local, real-time monitoring of OT/IoT devices.

The workflow connects device monitoring, baseline modeling, anomaly detection, risk assessment, edge policy, automatic isolation, and operator notification into one security flow.
