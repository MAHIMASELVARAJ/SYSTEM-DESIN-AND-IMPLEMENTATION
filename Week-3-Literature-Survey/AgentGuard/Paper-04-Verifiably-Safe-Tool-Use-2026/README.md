# Paper 04 – Towards Verifiably Safe Tool Use for LLM Agents

## Paper Details

**Title:** Towards Verifiably Safe Tool Use for LLM Agents

**Year:** 2026

**Venue:** IEEE/ACM ICSE-NIER 2026

**Authors:** Aarya Doshi et al.

## 1. Problem Addressed

LLM agents increasingly interact with external tools and services.

A tool call that appears safe individually can become dangerous when combined with other tool calls or when sensitive information flows between tools.

The paper addresses the need for verifiable safety during agent tool use.

## 2. Existing System

The work investigates mechanisms for controlling and verifying tool usage by LLM agents.

It considers capabilities, information flow and tool execution constraints to improve the safety of agent-tool interactions.

## 3. Existing Technologies / Methods

- Tool-use control
- Capability-based restrictions
- Information-flow control
- Data-flow constraints
- Tool-sequence analysis
- Safety specifications
- Security policies

## 4. Existing System Component Relevant to Our Project

The most relevant components are:

1. Capability control
2. Information-flow restrictions
3. Tool-sequence monitoring

These components can directly contribute to AgentGuard's runtime security layer.

## 5. How It Will Be Used in AgentGuard

Each tool can be registered with its allowed capabilities.

Example:

Tool:
DeleteUser

Capability:
DELETE

Risk:
HIGH

Required Permission:
ADMIN

AgentGuard will verify the capability before execution.

It can also monitor sensitive data movement between tools.

### Proposed workflow

Agent
↓
Tool Request
↓
Capability Check
↓
Data-Flow Check
↓
Tool Sequence Check
↓
Policy Engine
↓
ALLOW / VERIFY / BLOCK

## 6. Proposed System Module

**Module:** Capability and Tool Security Engine

This module will perform:

- Capability verification
- Data-flow verification
- Tool-sequence analysis
- Sensitive-data protection

## 7. Limitation of Existing System

The existing work focuses on safe tool use and verification but does not represent the complete AgentGuard architecture combining user purpose, delegated authority and runtime security decisions.

## 8. Research Gap

A unified mechanism is required to connect:

User Intent
+
Delegated Authority
+
Tool Capability
+
Data Sensitivity
+
Execution Sequence

into one runtime authorization decision.

## 9. Relevance to AgentGuard

This paper provides important technical foundations for enforcing restrictions at the tool-execution level.

## 10. Proposed Contribution

AgentGuard will adapt capability, information-flow and tool-sequence concepts into a unified runtime security firewall for autonomous agents.

## Reference

arXiv:
https://arxiv.org/abs/2601.08012

PDF:
https://arxiv.org/pdf/2601.08012

Conference:
IEEE/ACM ICSE-NIER 2026
