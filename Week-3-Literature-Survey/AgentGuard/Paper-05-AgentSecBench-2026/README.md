# Paper 05 – AgentSecBench

## Paper Details

**Title:** AgentSecBench: Measuring Prompt Injection, Privacy Leakage, and Tool-Use Integrity in LLM Agents

**Year:** 2026

**Authors:** Faruk Alpay, Taylan Alpay

## 1. Problem Addressed

AI agents may be vulnerable to prompt injection, privacy leakage and unauthorized tool use.

Traditional evaluation may not sufficiently measure whether the agent's security boundaries remain intact when exposed to malicious instructions.

## 2. Existing System

AgentSecBench provides a benchmark for evaluating security properties of LLM agents.

It focuses on areas such as:

- Prompt injection
- Privacy leakage
- Tool-use integrity
- Capability integrity
- Security boundaries

## 3. Existing Technologies / Methods

- Security benchmarking
- Prompt-injection testing
- Privacy-leakage testing
- Tool-use testing
- Capability-integrity evaluation
- Agent security metrics

## 4. Existing System Component Relevant to Our Project

The main component relevant to AgentGuard is its security evaluation methodology.

The benchmark concepts can be used to construct test cases for evaluating whether AgentGuard successfully prevents unauthorized actions.

## 5. How It Will Be Used in AgentGuard

AgentGuard will be tested against different attack scenarios.

Example:

Prompt Injection
↓
Agent Changes Intended Task
↓
Unauthorized Tool Request
↓
AgentGuard
↓
Policy Evaluation
↓
BLOCK

Another scenario:

Sensitive Data
↓
Agent Attempts External Transfer
↓
Data-Flow Check
↓
BLOCK

## 6. Proposed System Module

**Module:** Security Evaluation and Attack Simulation Module

## 7. Limitation of Existing System

AgentSecBench primarily evaluates the security of agents rather than functioning as the runtime authorization layer that prevents malicious actions.

## 8. Research Gap

There is a need to connect security evaluation with an enforceable runtime boundary that can actively prevent unauthorized agent actions.

## 9. Relevance to AgentGuard

AgentSecBench can provide evaluation scenarios and metrics for measuring the effectiveness of AgentGuard.

## 10. Proposed Contribution

AgentGuard will use benchmark-style attack scenarios to evaluate:

- Prompt-injection resistance
- Unauthorized tool-use prevention
- Privacy protection
- Capability enforcement
- Policy accuracy

## Reference

Paper:
https://arxiv.org/abs/2605.26269

PDF:
https://arxiv.org/pdf/2605.26269

GitHub:
https://github.com/Kalmantic/AgentSecBench
