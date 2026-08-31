# TesseraGuard — High-Level Workflow

**Project Title:** TesseraGuard — Aggregation-Aware API Threat Detection & Enforcement Gateway

## Overview

TesseraGuard is designed as an API security workflow that analyzes API requests based on the caller, their request history, and the combination of calls made over time.

The system does not evaluate API calls only as individual requests. It collects calls associated with an identity, builds a graph connecting the calls, identifies risky combinations, and applies an enforcement decision in real time.

## High-Level Workflow


API Gateway
     ↓
Caller Binder
     ↓
Call Collector
     ↓
Graph Builder
     ↓
Risk Engine
     ↓
Policy Engine
     ↓
Enforcement
     ↓
Audit Log
## System Modules
**1. API Gateway**

Purpose: Entry point for every API request.

Every API request first passes through the API gateway before moving through the TesseraGuard workflow.

**2. Caller Binder**

Purpose: Tags each request with the caller and session ID.

The caller binder associates an API request with the identity making the request and the corresponding session.

**3. Call Collector**

Purpose: Logs calls per identity over time.

The call collector maintains the history of API calls associated with each identity over a period of time.

**4. Graph Builder**

Purpose: Links calls using information such as data, volume, and speed.

The graph builder connects the collected API calls to represent how individual calls relate to each other over time.

**5. Risk Engine**

Purpose: Flags risky combinations of calls.

The risk engine analyzes the combination of API calls and identifies combinations that may represent risky activity.

This is the central analysis stage of TesseraGuard, where multiple calls are considered together rather than only as isolated requests.

**6. Policy Engine**

Purpose: Sets the security action.

The policy engine determines whether the identified activity should be:

Allow
Throttle
Block
**7. Enforcement**

Purpose: Blocks the identity's calls in real time.

When the policy engine determines that enforcement is required, the enforcement module applies the decision to the identity's API calls in real time.

**8. Audit Log**

Purpose: Logs what happened and why.

The audit log records the activity and the reason for the security decision so that it can be reviewed later.

## Complete Data Flow
1. API Gateway
   ↓
2. Caller Binder
   ↓
3. Call Collector
   ↓
4. Graph Builder
   ↓
5. Risk Engine
   ↓
6. Policy Engine
   ↓
7. Enforcement
   ↓
8. Audit Log
## Core Concept

The core workflow of TesseraGuard is:

Collect API calls → Connect calls over time → Identify risky combinations → Apply a policy → Enforce the decision in real time → Record the event

The workflow focuses on identifying risky combinations of API calls and connecting the risk decision directly to API enforcement.

## High-Level Module List
**S.No.	Module	Main Function**
1	API Gateway	Entry point for every API request
2	Caller Binder	Tags request with caller and session ID
3	Call Collector	Logs calls per identity over time
4	Graph Builder	Links calls using data, volume, and speed
5	Risk Engine	Flags risky combinations of calls
6	Policy Engine	Sets Allow / Throttle / Block
7	Enforcement	Blocks identity's calls in real time
8	Audit Log	Logs what happened and why
## Expected Security Flow
API Request
    ↓
Identify Caller
    ↓
Collect Request History
    ↓
Build Relationship Between Calls
    ↓
Analyze Combination Risk
    ↓
Policy Decision
    ↓
Allow / Throttle / Block
    ↓
Record Decision
## Architecture Direction

The high-level architecture is designed around the principle that API calls should be analyzed in relation to other calls made by the same identity over time.

The workflow therefore connects API monitoring, call relationship modeling, risk analysis, policy decision, and real-time enforcement into one security flow.
