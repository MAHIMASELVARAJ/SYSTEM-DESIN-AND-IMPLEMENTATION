# Paper 02 – The Task Shield

## Paper Details

**Title:** The Task Shield: Enforcing Task Alignment to Defend Against Indirect Prompt Injection in LLM Agents

**Year:** 2025

**Venue:** ACL 2025

**Authors:** Feiran Jia, Tong Wu, Xin Qin, Anna Squicciarini

## 1. Problem Addressed

Autonomous LLM agents can receive information from emails, websites, documents and other external sources. These sources may contain malicious instructions that attempt to change the agent's behavior.

The main problem addressed is indirect prompt injection, where an agent follows malicious instructions that are unrelated to the user's original task.

## 2. Existing System

The Task Shield introduces a task-alignment based defense mechanism.

The system evaluates whether an agent's proposed action is consistent with the user's intended task.

If an action is unrelated to the original task, it can be identified as potentially unsafe.

## 3. Existing Technologies / Methods

- LLM agents
- Task representation
- User-intent representation
- Task alignment
- Indirect prompt injection detection
- Action evaluation
- Security enforcement

## 4. Existing System Component Relevant to Our Project

The most important concept for AgentGuard is task or intent alignment.

The proposed AgentGuard system can use this concept to determine whether an agent's requested action is related to the original purpose provided by the user.

## 5. How It Will Be Used in AgentGuard

The user's request will first be converted into a representation of the intended task.

When the agent requests a tool or resource, AgentGuard will compare the requested action with the original intent.

### Proposed workflow

User Request
↓
Intent Extraction
↓
Purpose Representation
↓
AI Agent
↓
Tool Request
↓
Intent/Action Alignment
↓
Policy Decision
↓
ALLOW / VERIFY / BLOCK

## 6. Proposed System Module

**Module:** Intent Alignment Engine

This module will determine whether the requested agent action is consistent with the original user objective.

## 7. Limitation of Existing System

Task alignment alone does not provide a complete authorization mechanism for all resources, capabilities, sensitive data and tool execution sequences.

## 8. Research Gap

A broader runtime security mechanism is required that combines task alignment with:

- Agent identity
- Permission scope
- Tool capabilities
- Data sensitivity
- Resource authorization
- Execution history

## 9. Relevance to AgentGuard

The Task Shield provides an important foundation for preventing agents from performing actions that are unrelated to the user's original objective.

## 10. Proposed Contribution

AgentGuard will adapt the task-alignment concept and combine it with purpose-bound authorization, capability control, data-flow checking and runtime tool monitoring.

## Reference

Official Paper:
https://aclanthology.org/2025.acl-long.1435/

PDF:
https://aclanthology.org/2025.acl-long.1435.pdf
