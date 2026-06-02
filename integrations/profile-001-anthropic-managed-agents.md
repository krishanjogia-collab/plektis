# Integration Profile 001 - Anthropic Managed Agents

| Field | Value |
|---|---|
| **System** | Anthropic Claude Managed Agents |
| **Locus** | Substrate / runtime (hosted) |
| **Verdict** | Complement (additive; no core change) |
| **Maturity** | Beta (`managed-agents-2026-04-01`); launched 8 April 2026 |
| **Assessed** | 2026-05-31 |

## What it is

A hosted runtime that runs the Claude agent loop on Anthropic's infrastructure - orchestration, sandbox, session state, and credential handling are managed, so a builder needs no harness of their own. It is built around four concepts: **Agent** (model, system prompt, tools, MCP servers, and skills), **Environment** (an Anthropic-managed cloud sandbox or a self-hosted sandbox), **Session** (a stateful, resumable, server-side event log), and **Events** (user turns, tool results, and status, streamed over server-sent events, with the ability to steer or interrupt mid-run).

## Mapping to Plektis primitives

| Plektis primitive | How Managed Agents provides it |
|---|---|
| **Machine and skills** (Section 6.4) | The Agent's `skills` and system prompt load Plektis skill files and the `AGENTS.md` bootloader directly. Managed Agents consumes AAIF Agent Skills, which is the Plektis skill-file format, so no translation is needed. |
| **Environment and toolchain** (Section 6.5) | The managed or self-hosted sandbox provides the Code Execution and Bash capability slots; built-in file, web-search, and fetch tools; and native MCP server connections for the integration pillar. |
| **Session and persistence** (L0 Section 3.3.5) | The durable, resumable, server-side session maps to engagement-persistent working memory. The append-only event log lives outside the model context window and can be fetched in full. |
| **Escalation and human-in-the-loop** (L0 Section 3.3.4) | `steer` and `interrupt` carry Plektis escalation: the driver can pause, redirect, or halt mid-execution. The runtime supplies the mechanism; Plektis supplies the judgement about when a Tier 1 trigger requires it and what the driver is accountable for. |
| **Multi-agent and coordination** (Section 6.6) | Multiple agents and sessions can be composed; coordination follows the Plektis grammar. |

## Caveats

- **Beta.** Primitives and behaviour may change between releases.
- **Data residency and regulated work.** Because sessions store conversation history, sandbox state, and outputs server-side, the hosted offering is not currently positioned for the strictest data-residency or HIPAA-grade requirements. A self-hosted sandbox mitigates this in part. For regulated advisory engagements, confirm the deployment's residency and retention posture.
- **Vendor-specific.** This is a Claude-only runtime. Per the vendor-independence principle (Section 6.5), it is one option among several, not the runtime.

## Pricing (indicative)

Standard Claude token rates plus approximately $0.08 per active session-hour, plus web-search fees. Confirm current pricing with the provider.

## Sources

- Claude Managed Agents overview - platform.claude.com/docs/en/managed-agents/overview (primary).
- "Scaling Managed Agents: decoupling the brain from the runtime" - anthropic.com/engineering/managed-agents (primary).
- Independent corroboration: InfoQ and MindStudio coverage, April 2026.
