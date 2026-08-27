Case Study 2 – AgentGuard
Intent-Bound Security Firewall for Autonomous AI Agents
1. Introduction

AI agents are increasingly capable of independently accessing applications, APIs, databases, files and other digital resources. NIST has identified AI-agent identity, authorization, auditing and non-repudiation as emerging security requirements, and its 2026 work specifically highlights the need to adapt traditional cybersecurity controls for autonomous agents.

2. Core Problem

A human may authorize an AI agent to perform a limited task, but the agent may subsequently attempt additional actions that were not explicitly intended.

For example:

User: “Find my electricity bill.”

The agent accesses the electricity account appropriately but then attempts to access the user's banking information.

The problem is:

How can organizations ensure that an autonomous AI agent remains within the boundaries of the human's intended task while executing multiple tool calls?

3. Proposed Solution

AgentGuard is proposed as a cloud security gateway between AI agents and enterprise resources.

Before an agent performs a sensitive operation, AgentGuard evaluates:

Human authorization
Agent identity
Original task
Requested action
Target resource
Permission level
Action sequence
Current security context

The system can Allow, Intercept or Block the action.

4. Proposed Technical Innovation

The project will investigate an Intent-Bound Execution Lineage.

Instead of checking only whether an AI agent possesses permission, the system maintains a machine-readable relationship between:

Human Intent → Agent Plan → Tool Call → Resource → Result

The system detects delegation drift when the sequence of actions gradually moves outside the original authorization boundary.

This is a particularly important area for research, but the novelty must be carefully established because emerging agent-intent and authorization protocols already exist.

5. Cloud Deployment

The system can use an API gateway, AI-agent proxy, intent-analysis service, policy engine, permission manager, event stream, PostgreSQL database, audit service and cloud monitoring platform.

6. Expected Impact

AgentGuard could help enterprises safely deploy autonomous AI agents while reducing unauthorized tool usage, excessive permissions and unintended actions.

7. Case Study Takeaway

The project investigates a new security requirement:

“An AI agent should not only prove who it is; it should continuously prove that its actions remain within the human-authorized purpose.”