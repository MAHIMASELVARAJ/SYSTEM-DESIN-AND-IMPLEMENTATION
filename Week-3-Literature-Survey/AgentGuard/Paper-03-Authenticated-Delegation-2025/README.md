# Paper 03 – Authenticated Delegation and Authorized AI Agents

## Paper Details

**Title:** Authenticated Delegation and Authorized AI Agents

**Year:** 2025

**Authors:** Tobin South et al.

**Affiliation:** MIT Media Lab

## 1. Problem Addressed

AI agents increasingly perform tasks on behalf of humans and may access sensitive resources.

This creates the need to establish:

- Who authorized the agent?
- What task was delegated?
- What resources can the agent access?
- What actions is the agent allowed to perform?
- How can agent activity be audited?

## 2. Existing System

The work investigates authenticated delegation and authorization mechanisms for AI agents.

The system establishes a relationship between a human user and an AI agent and defines the scope of authority delegated to that agent.

## 3. Existing Technologies / Methods

- Agent identity
- Authentication
- Human-to-agent delegation
- Credentials
- Authorization
- Permission scopes
- Accountability
- Auditability

## 4. Existing System Component Relevant to Our Project

The most relevant concept is authenticated delegation.

AgentGuard will use this concept to establish the identity of the agent and determine what authority has been delegated to it by the user.

## 5. How It Will Be Used in AgentGuard

The user will authenticate and initiate a task.

A scoped authorization will then be associated with the agent.

### Proposed workflow

User Authentication
↓
Task Request
↓
Delegation Creation
↓
Agent Identity
↓
Permission Scope
↓
Agent Tool Request
↓
AgentGuard Authorization
↓
ALLOW / VERIFY / BLOCK

## 6. Proposed System Module

**Module:** Agent Identity and Delegation Engine

This module will maintain:

- User identity
- Agent identity
- Delegation information
- Permission scope
- Task purpose
- Expiration or session information

## 7. Limitation of Existing System

Authenticated delegation establishes authorization relationships but does not by itself provide complete runtime monitoring of every action performed by an autonomous agent.

## 8. Research Gap

A runtime security layer is required to continuously verify whether an agent remains within:

- Its delegated purpose
- Its capability scope
- Its resource scope
- Its data-access boundaries

## 9. Relevance to AgentGuard

This paper provides the identity and delegation foundation required before AgentGuard can make purpose-bound authorization decisions.

## 10. Proposed Contribution

AgentGuard will combine authenticated agent delegation with intent alignment, capability verification, data-flow monitoring and runtime tool-sequence analysis.

## Reference

Official publication:
https://www.media.mit.edu/publications/authenticated-delegation-and-authorized-ai-agents/

Preprint:
https://arxiv.org/abs/2501.09674

PDF:
https://arxiv.org/pdf/2501.09674
