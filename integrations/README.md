# Plektis Integration Profile Registry

This directory is the **Integration Profile Registry** defined in [Reference Model Section 6.7](../reference-model/L1/6.7-ecosystem-integration.md). It catalogues how Plektis integrates with external runtimes, tools, and standards across the agentic AI ecosystem.

Each profile maps an external system onto Plektis primitives - skills, toolchain and MCP, session and persistence, escalation and human-in-the-loop, multi-agent and A2A - and records a verdict, caveats, and the primary sources it was verified against. Adding a profile is additive: it never changes the reference model core.

See Section 6.7 for the mechanism: the impact taxonomy, the Watch / Complement / Extend / Revise verdict, and the governance cadence.

## Profiles

| ID | System | Locus | Verdict | Maturity | Profile |
|---|---|---|---|---|---|
| 001 | Anthropic Managed Agents | Substrate / runtime | Complement | Beta | [profile-001](profile-001-anthropic-managed-agents.md) |
| 002 | Google Vertex AI Agent Engine | Substrate / runtime | Complement | Preview | [profile-002](profile-002-google-vertex-agent-engine.md) |
| 003 | AWS Bedrock AgentCore | Substrate / runtime | Complement | GA (Registry and Payments in preview) | [profile-003](profile-003-aws-bedrock-agentcore.md) |

## Watch list (tracked, not yet profiled)

| System | Locus | Note |
|---|---|---|
| OpenAI Agents SDK (hosted harness) | Substrate / runtime | Model-native harness shipped in the open-source SDK; no first-party runtime fee. Profile when an integration is exercised. |
| Agent-to-Agent (A2A) protocol | Connectivity / tools | Emerging inter-agent standard, becoming table stakes across runtimes. Likely a Complement at the connectivity edge. |
| OpenClaw | To assess | Flagged by the driver; classify on assessment. |
| Google "Spark" | To assess | Pre-release; classify when it lands. |

---

*Verdicts and maturities reflect the assessment date recorded in each profile. The ecosystem moves quickly. Profiles are living artifacts and are expected to be revised.*
