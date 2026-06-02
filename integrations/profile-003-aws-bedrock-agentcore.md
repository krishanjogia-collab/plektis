# Integration Profile 003 - AWS Bedrock AgentCore

| Field | Value |
|---|---|
| **System** | Amazon Bedrock AgentCore |
| **Locus** | Substrate / runtime (open, model-agnostic) |
| **Verdict** | Complement (additive; no core change) |
| **Maturity** | Generally available (Runtime, Memory, Gateway, Identity, Code Interpreter, Browser, Observability, Evaluations, Policy); Agent Registry and Payments in preview |
| **Assessed** | 2026-05-31 |

## What it is

A serverless, model-agnostic platform for building, running, and governing agents at scale, composed of discrete services: **Runtime** (serverless execution with session isolation, VPC connectivity, bi-directional streaming, workloads up to 8 hours), **Memory** (short- and long-term), **Gateway** (turns APIs and Lambda functions into agent tools), **Identity** (credential vault, OAuth, IAM), **Code Interpreter** and **Browser** (sandboxes), **Observability**, **Evaluations**, **Policy** (real-time tool-call authorisation via Cedar), and an **Agent Registry** (preview) for discovery and governance. It runs CrewAI, LangGraph, LlamaIndex, Google ADK, OpenAI Agents SDK, Strands, and custom frameworks; supports MCP fully and A2A in the runtime; and is model-agnostic (Claude, Gemini, OpenAI, Nova, Llama, Mistral).

## Mapping to Plektis primitives

| Plektis primitive | How AgentCore provides it |
|---|---|
| **Machine and skills** (Section 6.4) | The agent is built in any supported framework; Plektis skill files and the bootloader load as its configuration. AgentCore is the substrate, not the cognition. |
| **Environment and toolchain** (Section 6.5) | Code Interpreter and Browser provide sandboxed Code Execution; Gateway provisions tools; MCP is fully supported for the integration pillar; Identity provides the credential vault. |
| **Session and persistence** (L0 Section 3.3.5) | Runtime session isolation plus the Memory service (short- and long-term, cross-session) map to engagement- and cross-engagement-persistent working memory. |
| **Escalation and human-in-the-loop** (L0 Section 3.3.4) | Policy (Cedar) enforces real-time tool-call authorisation; the Agent Registry adds approval workflows; Payments requires explicit end-user authorisation. These carry Plektis Tier 1 gating at the infrastructure layer; Plektis supplies the professional judgement about when, and what the driver answers for. |
| **Multi-agent and coordination** (Section 6.6) | A2A in the runtime and the Agent Registry support inter-agent discovery and coordination; the Plektis grammar runs on top. |

## Caveats

- **Agent Registry and Payments are in preview.**
- **Strong on regulated work.** HIPAA-eligible, 15 regions including the EU, VPC support, and a broad compliance set - notable where the Anthropic hosted offering is not yet positioned for HIPAA-grade residency. This makes AgentCore a candidate substrate for regulated advisory deployments.
- **Substrate, not doctrine.** AgentCore positions itself as the open, model-agnostic substrate. Plektis runs on it as the professional-practice layer above, one option among several.

## Pricing (indicative)

Consumption-based: active CPU and memory billed per second, no minimums. Confirm current pricing with the provider.

## Sources

- Amazon Bedrock AgentCore FAQs - aws.amazon.com/bedrock/agentcore/faqs/ (primary).
