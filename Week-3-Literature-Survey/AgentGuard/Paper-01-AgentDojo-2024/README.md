# Paper 01 – AgentDojo

## Paper Details

**Title:** AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents

**Year:** 2024

**Venue:** NeurIPS 2024

**Authors:** Edoardo Debenedetti et al.

## 1. Problem Addressed

LLM-based autonomous agents interact with external tools and untrusted information. Malicious instructions can cause an agent to perform actions that were not intended by the user.

The paper addresses the need for realistic environments to evaluate prompt injection attacks and defenses against tool-using agents.

## 2. Existing System

AgentDojo provides a dynamic environment containing realistic tasks, tools and security scenarios for evaluating LLM agents.

The environment includes prompt-injection attacks and test cases involving tool-using agents.

## 3. Existing Technologies / Methods

- LLM agents
- External tools
- Realistic task environments
- Prompt injection scenarios
- Security test cases
- Agent security evaluation
- Attack success evaluation

## 4. Existing System Component Relevant to Our Project

The main component relevant to AgentGuard is the realistic security testing methodology.

AgentDojo can provide the basis for constructing test scenarios involving:

- Prompt injection
- Unauthorized tool use
- Malicious external instructions
- Agent behavior under attack

## 5. How It Will Be Used in AgentGuard

AgentDojo-style scenarios will be used to evaluate whether AgentGuard can detect and prevent unauthorized agent actions.

### Proposed workflow

Attack Scenario
↓
AI Agent
↓
Malicious / Untrusted Instruction
↓
Tool Request
↓
AgentGuard
↓
ALLOW / VERIFY / BLOCK
↓
Security Evaluation

## 6. Proposed System Module

**Module:** Security Testing and Evaluation Module

## 7. Limitation of Existing System

AgentDojo primarily provides an evaluation environment and benchmark rather than acting as the runtime authorization firewall for enterprise AI agents.

## 8. Research Gap

A runtime mechanism is required to enforce authorization boundaries during actual agent execution.

## 9. Relevance to AgentGuard

AgentDojo provides realistic scenarios and evaluation methodology that can be adapted to validate AgentGuard against prompt injection and unauthorized tool-use attacks.

## 10. Proposed Contribution

AgentGuard will use these security scenarios to evaluate its purpose-bound runtime enforcement mechanism.

## Reference

[Official Paper / PDF](PASTE-LINK-HERE)
