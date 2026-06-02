# Integration Profile 002 - Google Vertex AI Agent Engine

| Field | Value |
|---|---|
| **System** | Google Vertex AI Agent Engine (documented under the Gemini Enterprise Agent Platform) |
| **Locus** | Substrate / runtime (hosted) |
| **Verdict** | Complement (additive; no core change) |
| **Maturity** | Preview (subject to Pre-GA Offerings Terms) |
| **Assessed** | 2026-05-31 |

## What it is

A fully managed, serverless runtime for deploying and operating agents without managing infrastructure. It provides managed **Sessions** (continuous conversation state), a **Memory Bank** for persistent long-term memories, dynamic **Code Execution** and computer use in a sandbox, and built-in **observability** (tracing, logging, monitoring). It supports the Agent Development Kit (ADK), LangChain, LangGraph, LlamaIndex, custom agents, and the Agent-to-Agent (A2A) protocol.

## Mapping to Plektis primitives

| Plektis primitive | How Vertex Agent Engine provides it |
|---|---|
| **Machine and skills** (Section 6.4) | Agents are deployed via ADK or a supported framework; Plektis skill files and the bootloader load as the agent's instructions and configuration. |
| **Environment and toolchain** (Section 6.5) | The managed serverless runtime, with dynamic code execution and computer use, provides the Code Execution capability slot. Tool access is provisioned through the framework. MCP support is not stated in the Agent Engine overview reviewed; confirm before relying on it. |
| **Session and persistence** (L0 Section 3.3.5) | Managed Sessions hold conversation state; the Memory Bank provides cross-session long-term persistence, mapping to engagement- and cross-engagement-persistent working memory. IAM Conditions govern access. |
| **Escalation and human-in-the-loop** (L0 Section 3.3.4) | No explicit approval-gate primitive is documented in the overview; escalation is implemented at the framework or application layer on top of the runtime. Confirm the human-in-the-loop mechanism for a given deployment. |
| **Multi-agent and coordination** (Section 6.6) | A2A is supported for inter-agent communication; the Plektis coordination grammar runs on top. |

## Caveats

- **Preview.** Subject to Pre-GA terms. Naming and capabilities are shifting (the product is presented under the Gemini Enterprise Agent Platform).
- **Human-in-the-loop is not first-class in the runtime overview.** Plan to implement escalation gating at the framework layer.
- **MCP not confirmed** in the Agent Engine overview reviewed.
- Google's enterprise platform is generally positioned for strong governance and data residency. Confirm specifics for the engagement's jurisdiction.

## Pricing (indicative)

Consumption / usage-based across runtime, sessions, and memory. Confirm current pricing with the provider.

## Sources

- Vertex AI Agent Engine overview - docs.cloud.google.com/vertex-ai/generative-ai/docs/agent-engine/overview (primary).
