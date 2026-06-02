# Reference Configuration: A Working Node

This document describes one working implementation of a Plektis node. It is the configuration used by the protocol's author during the development of Plektis itself. It is published as a concrete example, not a prescription. Your configuration will differ based on your tools, preferences, and engagement requirements.

The purpose of showing this is practical: the protocol defines abstract capability slots and coordination patterns. This document shows what those abstractions look like when they are filled with real tools and real workflows.

---

## Driver

One senior practitioner. Background in business architecture, strategy execution, and advisory work. The driver operates across multiple engagement types (capability assessments, operating model design, strategy-to-execution, transformation roadmapping) and uses the node for all of them.

The driver is not a technical specialist. They are a business professional who has learned to operate an AI-augmented workflow. This is the target profile for driver certification.

---

## Machine Ensemble

The machine side of this node is not one AI tool. It is an ensemble of five AI products, each serving a different role. They are coordinated through the protocol's interaction layer (skill files, WORKBOARD.md, HANDOFF_LOG.md) rather than through a single orchestration platform.

### Agent Roles

| Agent | Product | Role in the Node | SenRef Phases |
|---|---|---|---|
| **Strategist** | Claude (Projects/Chat) | Strategy formulation, narrative design, positioning, stakeholder communication. The agent the driver thinks with. Operates in extended conversation with deep context retention. | Sense, Model, Decide |
| **Architect** | Claude Code (terminal) | Technical architecture, specification writing, code architecture, quality review. Produces design specs and reviews implementer output. Does not write implementation code unless explicitly directed. | Model, Decide, Reflect |
| **Implementer** | Google Gemini (AI Studio) | High-volume execution against specs. Code production, file migrations, formatting, bulk operations. Operates against handoff documents with defined acceptance criteria. | Model, Decide |
| **Researcher** | Google Gemini (Deep Research / Chat) | Landscape analysis, competitive research, naming viability, technical investigation. Produces structured research findings. Also used for image generation, mockups, and visual design exploration. | Sense |
| **Grounding Engine** | Google Gemini (via API) | Real-time search grounding for live data enrichment. Powers the Sense phase of products that require external data (e.g., entity discovery and market intelligence enrichment). | Sense |

### Why Multiple Agents

A single AI tool cannot fill every role effectively. Reasoning engines optimised for deep strategic conversation (Claude Projects) are different from tools optimised for code execution (Claude Code), which are different from tools optimised for high-volume production (Gemini). The protocol's agent-agnostic design means each capability slot is filled by whatever tool does it best. The coordination grammar (WORKBOARD.md, HANDOFF_LOG.md, review/verify cycles) provides the connective tissue.

---

## Toolchain Mapping

Each capability slot from the protocol (Section 6.5) is provisioned with a specific tool. The "alternatives" column shows what a practitioner using a different ecosystem would substitute.

| Capability Slot | Tool Used | How It Is Used | Alternatives |
|---|---|---|---|
| **Reasoning Engine** | Claude (Projects/Chat) + Claude Code | Strategic thinking happens in Claude Projects. Technical architecture happens in Claude Code. Both are reasoning engines, differentiated by context and interface. | GPT-4o, Gemini Advanced, Llama (local), any frontier model |
| **Code Execution** | Claude Code | Builds prototypes, runs commands, manages git, executes technical tasks in the terminal. | Cursor, GitHub Copilot, Windsurf, Gemini Code Assist |
| **Implementation Engine** | Google Gemini (via AI Studio) | Executes against specs produced by the architect. High throughput for migrations, formatting, bulk file operations. | Any second AI agent. Could be a second Claude Code instance, Cursor, or a human developer. |
| **Search & Grounding** | Google Gemini (API with search grounding) | Powers entity discovery and enrichment in products that need live data. Web search, news monitoring, entity resolution. | Perplexity API, Tavily, Brave Search API, Bing API |
| **Research & Analysis** | Google Gemini (Deep Research) | Landscape analysis, competitive intelligence, naming viability checks, technical investigation. Produces structured findings documents. | Perplexity, Claude with web search, manual research |
| **Visual Design** | Google Gemini (Chat) | Image generation, UI mockups, visual design exploration, presentation assets. | Midjourney, DALL-E, Figma with AI, Canva |
| **API Gateway** | Google AI Studio | Provides API keys and inference endpoints for products that make model calls (e.g., Gemini Flash for prototype applications that make real-time model calls). | Anthropic Console, OpenAI Platform, AWS Bedrock, Azure OpenAI |
| **Version Control** | GitHub | Source of truth for all code and protocol content. Commit history provides authorship provenance. | GitLab, Bitbucket |
| **Deployment Platform** | Vercel | Hosts prototypes and products. Zero-infrastructure serverless deployment. Accessible from any device including restricted environments. | Netlify, AWS Amplify, Cloudflare Pages, Railway |
| **Persistent Context Store** | `.md` files (local filesystem + GitHub) | Skill files, strategy documents, engagement logs, handoff records. The canonical persistence layer for expertise and methodology. | Any file system. Notion, Obsidian, or any tool that stores markdown. |
| **Structured Data Store** | SQLite + Prisma, graphology.js | Persistent entity-relationship state for applications with complex relational data (capability hierarchies, entity graphs). | Neo4j, PostgreSQL, TigerGraph, DuckDB |

---

## Coordination Model

This node uses the **Architect-Implementer pattern** (Section 6.6) with the driver coordinating between agents.

### Information Flow

```
Driver
  ↓ (mandate, context, constraints)
Strategist (Claude Chat)
  ↓ (strategy decisions, positioning, narrative)
Architect (Claude Code)
  ↓ (specs, handoff briefs, design decisions)
Implementer (Gemini)
  ↓ (built artifacts, delivery notes)
Architect (Claude Code)
  ↓ (/review cycle, fix list)
Implementer (Gemini)
  ↓ (fixes applied)
Architect (Claude Code)
  ↓ (/verify, push to repo)
Driver
  ↓ (approval, next mandate)
```

### Coordination Artifacts

- **WORKBOARD.md** tracks tasks across agents (Backlog → Ready → In Progress → Review → Done)
- **HANDOFF_LOG.md** records what was passed between agents, what was decided, and what was flagged
- **Handoff briefs** (structured `.md` files) provide the implementer with everything needed to execute: objective, scope, acceptance criteria, conventions, review expectations
- **Review documents** record the architect's findings after reviewing implementer output, with specific fix items

### What the Driver Actually Does Day-to-Day

The driver does not type prompts all day. The driver:

1. Sets the engagement objective and loads the relevant skill files
2. Works with the strategist agent on high-level decisions (positioning, narrative, stakeholder communication)
3. Reviews the architect agent's specifications before they go to the implementer
4. Makes judgment calls the machines cannot (political dynamics, ethical boundaries, strategic trade-offs)
5. Reviews deliverables against the quality standards in the loaded skill files
6. Decides what to persist, what to discard, and what to refine
7. Drives the Reflect phase by identifying what worked, what failed, and what should be encoded as a new rule in the skill files

---

## Environment Notes

The protocol works across different environments and security boundaries. Skill files and `.md` coordination artifacts are portable by design - they can move between machines, cloud environments, and organisational contexts without modification. Products deployed on hosting platforms (Vercel, Netlify, etc.) are accessible from any browser, including locked-down corporate environments.

---

## This Is One Configuration

Everything above describes one practitioner's setup. A different practitioner might:

- Use only one AI tool (GPT-4o for everything) instead of an ensemble
- Skip the implementer agent entirely and do all execution themselves
- Use a framework like CrewAI or LangGraph instead of `.md` coordination artifacts
- Deploy on AWS instead of Vercel
- Use Neo4j instead of SQLite
- Run everything on one machine

The protocol does not prescribe any of this. It defines the capability slots that need to be filled, the coordination grammar for multi-agent work, and the interaction protocols between driver and machine. How those are implemented is the practitioner's choice.

The value of showing this reference configuration is not "do what I do." It is "here is the protocol in practice, with real tools on real engagements." This is one practitioner's working setup, not a controlled result. Whether a node beats a skilled practitioner improvising is still the open question.
