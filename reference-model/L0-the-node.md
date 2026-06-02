# Plektis Reference Model: Level 0 - The Node

**Document type:** Foundational Architecture
**Version:** 0.1.0
**Date:** 2026-06-02
**Author:** Krish Jogia (with Claude)
**Status:** Stable. Ready for peer review.
**Parent document:** See L0 README (reference-model/README.md)

---

## Purpose

This document defines the Level 0 architecture of the Plektis protocol. It establishes the system boundary, identifies the core components and external entities, and specifies the flows that cross the boundary. This is the foundational architecture from which all other layers, products, and protocols derive.

In architecture terms: Level 0 is the context diagram. It answers the question: **what is the node, and what does it interact with?**

---

## 1. The System: The Node

The node is the atomic unit of the Plektis. It is a single integrated system comprising one human operator (the driver) and one or more AI agents (the machine), operating together to produce strategic, architectural, and transactional outcomes that neither could achieve independently.

The node is not a human using a tool. It is not an AI acting autonomously. It is a fused system with shared context, complementary capabilities, and coordinated decision-making. The quality of the node's output depends on the quality of the integration between its components, not on the individual capability of either one.

**Lineage:** The concept of a "node" as the atomic unit of human-AI collaboration has prior art. Mohammed et al. (2012, "A Nodal Approach to Modeling Human-Agents Collaboration," International Journal of Computer Applications) defined a node as "a human actor, one or more agents, and their combined functions to represent a collective intelligent entity." Kasparov's centaur model (1998, Advanced Chess) established the foundational metaphor: a weak human + machine + better process beats a strong computer alone. DARPA's ACE program validated the hierarchical model where humans handle strategy and AI handles tactics - structurally identical to the driver/agent split. This reference model builds on these foundations, formalizing the node for business architecture and strategy contexts with specific interaction protocols, escalation triggers, and a defined cognitive cycle (SenRef).

### 1.1 Ontological Status

The node is an ontological claim, not a metaphor. It defines a new entity class in the ontology of professional practice: a fused cognitive system that is irreducible to its components. The node is not a human who uses AI tools (that's augmentation). It is not an AI that replaces a human (that's automation). It is a distinct system with its own capabilities, protocols, and lifecycle that emerge from the integration of human and machine cognition.

This distinction matters because it determines how the node is designed, governed, and measured. An "augmented human" is measured by human productivity metrics. An "automated process" is measured by throughput and error rate. A node is measured by the quality of its integrated output - the strategic, architectural, and transactional outcomes that the fused system produces. The interaction layer (Section 3.3) is not overhead. It is the mechanism through which the node's emergent capability is produced.

Existing ontologies in this space provide partial coverage. BIZBOK defines entities for business architecture (capabilities, value streams, information concepts). TOGAF's ArchiMate defines entities for enterprise architecture (application components, business processes, technology nodes). NATO's HATOM (Human AI-Teaming Ontology Model) defines entities for human-AI team structure in military contexts. Plektis extends this ontological landscape by defining the node as a first-class entity for professional practice, with the SenRef cycle as its cognition model, skill files as its knowledge encoding, and the interaction layer as its operating protocol.

### 1.2 System Boundary

The node boundary encapsulates:

- The **driver** (human operator)
- The **machine** (AI agent ensemble)
- The **interaction layer** (protocols, handoffs, escalation triggers, shared context)
- The **working memory** (living artifacts, skill files, knowledge graphs, conversation history)

Everything outside this boundary is an external entity. The node receives inputs from and delivers outputs to these external entities, but the internal orchestration of how the driver and machine collaborate is the protocol's domain.

---

## 2. External Entities

The node operates within a context defined by the following external entities:

### 2.1 Client Environment

The organization or individual that engages the node. This includes:

- **Principals:** Founders, board members, family office leaders, C-suite executives. The humans who commission the work and make final decisions.
- **Stakeholders:** Broader organizational actors affected by or contributing to the engagement - management teams, functional leads, portfolio company operators.
- **Organizational context:** Strategy, culture, governance structures, existing capabilities, political dynamics. The terrain the node operates within.

### 2.2 Data Environment

The information landscape the machine draws from:

- **Client data:** Financial statements, organizational charts, process documentation, system inventories, historical performance. Provided by the client or sourced during the engagement.
- **Market data:** Industry intelligence, competitive landscapes, transaction databases, regulatory filings, macroeconomic indicators. Sourced through research, subscriptions, or agent-driven collection.
- **Domain knowledge:** The codified expertise embedded in skill files, knowledge graphs, and reference architectures. This is the protocol's own intellectual capital.

### 2.3 Regulatory and Compliance Environment

The legal and regulatory constraints governing the engagement:

- **Jurisdictional requirements:** Securities regulation, privacy law (PIPEDA, GDPR), professional standards, fiduciary obligations.
- **Confidentiality obligations:** NDA terms, client privilege, information barriers.
- **Professional standards:** Industry codes of conduct, ethical guidelines, duty of care.

The regulatory environment defines the boundaries within which the node may operate. It is the primary source of **mandatory human-in-the-loop escalation triggers** - decisions that the machine may prepare but the driver must authorize.

### 2.4 External Forces

Dynamic conditions that stress, challenge, or inform the node's work:

- **Market shifts:** Economic cycles, interest rate changes, commodity prices, supply chain disruptions.
- **Competitive moves:** Acquisitions, new market entrants, technology disruptions, regulatory changes affecting competitors.
- **Political and geopolitical dynamics:** Policy changes, trade tensions, political transitions.
- **Technology evolution:** New AI capabilities, platform changes, tool availability.

External forces are inputs the node must sense and respond to. The machine excels at monitoring and pattern-detecting across these forces. The driver excels at interpreting their strategic implications.

---

## 3. Core Components

### 3.1 The Driver (Human Operator)

The driver is the human component of the node. The driver brings capabilities that the machine cannot replicate:

- **Strategic judgment under ambiguity.** The ability to make high-stakes decisions when data is incomplete, conflicting, or absent. This includes knowing when to act, when to wait, and when the question itself is wrong.
- **Stakeholder navigation.** Reading rooms, managing politics, building trust, persuading boards, calibrating communication to audience. The emotional and relational intelligence that determines whether good analysis actually gets implemented.
- **Ethical reasoning.** Applying moral judgment to complex situations where rules and guidelines are insufficient. Knowing when a technically correct recommendation is the wrong one.
- **Creative synthesis.** Connecting disparate domains, seeing patterns across unrelated fields, generating novel strategic options that no dataset would suggest.
- **Authority and accountability.** The driver signs off. The driver is accountable for outcomes. The driver carries professional and legal responsibility. This is structural, not delegable.

**What the driver does not do:** Routine data processing, exhaustive document review, repetitive pattern matching across large datasets, maintaining real-time awareness across dozens of data streams, drafting and formatting at volume. These are machine capabilities.

### 3.2 The Machine (AI Agent Ensemble)

The machine is the AI component of the node. It may consist of a single agent or multiple coordinated agents (multi-agent orchestration). The machine brings capabilities that the driver cannot match - but those capabilities are not a flat list. They are organized around a fundamental cognitive cycle that defines how the machine operates.

#### 3.2.1 The SenRef Cycle: Sense → Model → Decide → Reflect

Every task the machine performs moves through a four-phase operating loop. This cycle is the machine's cognition model - the foundational pattern that every capability, every agent, every skill file, and every marketplace module instantiates. Understanding SenRef is understanding how the machine side of the node thinks.

```
    ┌──────────┐
    │  SENSE   │ ← Ingest, monitor, detect, extract
    └────┬─────┘
         │
         ▼
    ┌──────────┐
    │  MODEL   │ ← Structure, map, simulate, scenario
    └────┬─────┘
         │
         ▼
    ┌──────────┐
    │  DECIDE  │ ← Score, qualify, recommend, prioritize
    └────┬─────┘
         │
         ▼
    ┌──────────┐
    │ REFLECT  │ ← Evaluate, update, refine, learn
    └────┬─────┘
         │
         ├──────→ (feeds back into SENSE)
         │
         └──────→ [SHARED CONTEXT] (persists to working memory)
```

**Lineage and Positioning**

SenRef is not a novel cognitive cycle. It is a purposeful synthesis of established frameworks, adapted specifically for machine cognition within a human-AI teaming context. The four-phase pattern (sense → process → decide → feedback) is the most fundamental pattern in cognitive science. SenRef's contribution is not the loop itself but three specific design choices that differentiate it from its predecessors.

The primary intellectual ancestors:

| Framework | Author / Date | How SenRef Relates | Citation |
|---|---|---|---|
| **OODA Loop** | John Boyd, ~1986 | Observe→Sense, Orient→Model, Decide→Decide, Act→(absent). SenRef replaces Act with Reflect, making it a cognition-only loop. The machine thinks but does not act - action is a human prerogative. | Mandatory |
| **Active Inference** | Karl Friston, ~2009 | The Reflect phase operationalizes what Friston formalizes mathematically: prediction error updating to improve the internal model. SenRef's Reflect is Active Inference applied to a machine agent. | Mandatory |
| **Intelligence-Design-Choice** | Herbert Simon, 1960 | Intelligence→Sense, Design→Model, Choice→Decide. Simon's foundational decision-making model, adapted for machine cognition. | Mandatory |
| **ReAct** | Yao et al., 2022 | The dominant LLM agent paradigm. Thought→Model+Decide, Observation→Sense+Reflect. SenRef makes the phases explicit where ReAct conflates them. | Mandatory |
| **BDI Agent Model** | Bratman/Rao/Georgeff, 1987 | Perceive→Sense, Desire→Model, Intention→Decide, Belief Revision→Reflect. The classical agent architecture that SenRef echoes for a new context. | Recommended |
| **Reflexion** | Shinn et al., 2023 | Actor→Decide, Evaluator→Reflect, Self-Reflection→Reflect, Episodic Memory→persistence. The closest match in agentic AI. SenRef's Reflect phase and persistence model parallel Reflexion's verbal reinforcement architecture. | Recommended |
| **Cynefin** | Dave Snowden, 1999 | Sense→Sense, Categorize/Analyze→Model+Decide. Informs how the machine approaches different problem domains. | For completeness |
| **PDCA** | Deming/Shewhart, 1950s | Plan→Model+Decide, Check→Reflect. The industrial quality cycle. | For completeness |
| **Kolb's Learning Cycle** | David Kolb, 1984 | Experience→Sense, Reflective Observation→Reflect, Abstract Conceptualization→Model. | For completeness |

**What is defensibly original in SenRef:**

1. **Replacing Act with Reflect.** OODA ends with Act. PDCA ends with Act. SenRef ends with Reflect. This makes SenRef a cognition-only loop: the machine senses, models, decides, and reflects - but it does not act. Action crosses the human-in-the-loop escalation boundary. The machine proposes. The driver disposes. This is a philosophical design choice with architectural consequences: the Decide → Reflect transition is the escalation gateway.

2. **Positioning as machine cognition within a broader operating system.** OODA was designed for human decision-making in combat. PDCA was designed for industrial quality control. ReAct was designed for LLM reasoning chains. SenRef is designed specifically as the internal cognition model of the machine component within a human-AI node. It does not stand alone - it operates within the interaction layer (Section 3.3), governed by escalation triggers, handoff protocols, and shared context.

3. **Explicit persistence as an architectural requirement.** The arrow from Reflect to Shared Context is not incidental. The Reflect phase produces outputs (updated assumptions, refined skill files, evaluated outcomes) that must persist in working memory (Section 3.3.5) for the next Sense phase to consume. This closes the loop architecturally as well as cognitively. The persistence model is part of the cycle, not an afterthought.

**Phase 1: SENSE**

The machine ingests information from the external environment and the node's working memory. This is the input processing layer - where raw data becomes structured awareness.

Capabilities in this phase:

- **Data ingestion and extraction.** Processing financial statements, organizational documents, market reports, regulatory filings. Transforming unstructured content into structured, queryable information.
- **Multi-source monitoring.** Simultaneously tracking market signals, news feeds, regulatory changes, competitive moves, and data streams. Detecting patterns and anomalies that a human scanning sequentially would miss.
- **Signal detection.** Identifying indicators that match predefined taxonomies - capability maturity thresholds, strategic alignment gaps, competitive positioning shifts, operational risk patterns. A domain intelligence skill file configures which signals the machine watches for.
- **Context loading.** Reading and integrating skill files, engagement history, living artifacts, and knowledge graphs at the start of a session. Reconstructing the node's state from persistent working memory.

**Escalation mapping:** Sense is largely autonomous. The machine collects and structures without needing driver authorization. Exception: if the machine detects information that triggers a Tier 2 escalation (anomalies, contradictions, stakeholder sensitivities), it flags before proceeding.

**Phase 2: MODEL**

The machine structures, organizes, and simulates. It builds representations of reality that the driver can inspect, interrogate, and steer. This is where raw awareness becomes usable intelligence.

Capabilities in this phase:

- **Knowledge graph construction.** Building and maintaining structured representations of entities and relationships - market maps, capability taxonomies, organizational structures, portfolio configurations. Graph-native over tabular (Operating Principle #5).
- **Scenario simulation.** Modelling alternative futures, portfolio configurations, deal outcomes, and strategic pathways. Running sensitivity analyses, stress tests, and what-if explorations across multiple variables simultaneously.
- **Pattern synthesis.** Connecting signals from the Sense phase into coherent narratives - market trends, competitive dynamics, capability gaps, value chain dependencies. Seeing the whole system rather than its isolated parts.
- **Architecture generation.** Building capability maps, value stream models, operating model blueprints, and integration architectures. Rapid prototyping of structural designs at a speed that keeps pace with strategic thinking.

**Escalation mapping:** Model is largely autonomous for construction. The driver defines the parameters ("model three transformation scenarios for the supply chain capability domain") and the machine builds. Tier 2 escalation if the model produces results that conflict with the working thesis or reveal unexpected dynamics.

**Phase 3: DECIDE**

The machine narrows options toward action. It scores, qualifies, ranks, and recommends. This is the phase where the machine's output becomes directly actionable - and where escalation triggers are most active.

Capabilities in this phase:

- **Scoring and qualification.** Applying decision frameworks to structured options - capability maturity assessments, strategic alignment scores, investment prioritisation matrices, gap severity rankings.
- **Prioritization.** Ordering opportunities, risks, or tasks by impact, urgency, feasibility, or strategic fit. Producing ranked lists that the driver can act on immediately.
- **Recommendation generation.** Synthesizing analysis into clear, actionable recommendations with supporting evidence, confidence levels, and identified risks. The machine proposes. The driver disposes.
- **Draft production.** Generating engagement deliverables - architecture reports, board presentations, capability assessment summaries, transformation roadmaps, investment cases. Producing complete first drafts that the driver refines rather than builds from scratch.

**Escalation mapping:** This is where escalation triggers concentrate. The machine can score and recommend autonomously, but:
- Tier 1 (mandatory) for any recommendation involving capital commitment, legal obligation, or irreversible strategic action.
- Tier 2 (advisory) for any situation with multiple valid options where the choice depends on values, risk appetite, or political dynamics.
- The machine must always communicate confidence level in the Decide phase (Operating Principle #4: confidence-aware throughout).

**Phase 4: REFLECT**

The machine evaluates outcomes, updates its assumptions, and refines its own capabilities. This is the learning phase - where the protocol gets smarter over time.

Capabilities in this phase:

- **Outcome evaluation.** Comparing predictions against actuals. Did the capability investment produce the expected maturity improvement? Did the modelled transformation scenario materialise? Did the operating model redesign achieve its target state?
- **Assumption updating.** Revising the working thesis, market maps, and scoring parameters based on new evidence. The living artifacts in working memory are updated to reflect what was learned.
- **Skill file refinement.** Proposing updates to skill files based on engagement experience. New quality rules discovered in practice, refined assessment scoring based on observed outcomes, updated methodology steps based on engagement feedback. The formal protocol for skill file evolution will be specified in Level 1, Section 6.4.
- **Meta-analysis.** Evaluating the node's own performance - where did the SenRef cycle work well? Where did it break down? Which phases need more driver oversight, and which can be further automated?

**Escalation mapping:** Reflect is largely autonomous for internal learning. Tier 3 (informational) when proposing skill file updates. The driver reviews and approves refinements before they become canonical.

**Persistence:** Reflect-phase outputs (updated assumptions, revised scoring parameters, proposed skill file refinements, evaluated outcomes) persist to Shared Context (Section 3.3.1) via the working memory persistence model (Section 3.3.5). This is the architectural closure of the SenRef loop: Reflect produces, working memory stores, and the next Sense phase reads. Without this persistence path, the node starts every cycle from scratch. With it, the node accumulates institutional knowledge across iterations and engagements.

#### 3.2.2 SenRef as Application Architecture

Every domain application that runs on the protocol is a specific configuration of the SenRef cycle. A business architecture engagement maps directly:

| Engagement Phase | Primary SenRef Phase | Secondary Phases |
|---|---|---|
| **Discovery** (stakeholder context, document ingestion, current state assessment) | SENSE (data ingestion, signal detection) | MODEL (initial structuring) |
| **Architecture** (capability modelling, value stream mapping, PPIT analysis) | MODEL (knowledge graph construction, architecture generation) | SENSE (ongoing data gathering), DECIDE (maturity scoring) |
| **Assessment** (gap analysis, investment prioritisation, roadmap design) | DECIDE (scoring, qualification, recommendation) | MODEL (scenario simulation), REFLECT (assumption validation) |
| **Delivery** (stakeholder-calibrated outputs, roadmap refinement, methodology evolution) | REFLECT (outcome evaluation, skill file refinement) | DECIDE (deliverable production) |

This mapping is not incidental. It demonstrates that SenRef is the underlying grammar that domain-specific applications express. A different domain - healthcare transformation, public sector modernisation, technology platform design - would produce different phase compositions, but they would all be built from the same four phases.

#### 3.2.3 What the Machine Does Not Do

The SenRef cycle has a clear boundary. The machine does not:

- Make irreversible decisions without driver authorization (Decide phase is escalation-gated).
- Navigate political dynamics between stakeholders (this is driver capability, not machine cognition).
- Carry professional or legal liability (authority and accountability remain with the driver).
- Exercise moral judgment (ethical reasoning sits outside the SenRef cycle entirely).
- Read a room (stakeholder navigation is a driver-only capability).

These boundaries are structural. They define where the SenRef cycle stops and the driver takes over. The escalation triggers (Section 3.3.4) are the enforcement mechanism.

### 3.3 The Interaction Layer

The interaction layer is the protocol stack that governs how the driver and machine work together. This is where the protocol lives. Without it, you have a person and a tool. With it, you have a node.

The interaction layer consists of:

#### 3.3.1 Shared Context

The working memory that both the driver and machine can access and contribute to:

- **Skill files (.md):** Machine-readable encodings of domain expertise, engagement methodologies, role definitions, and quality standards. These define what the machine knows how to do and how it should do it.
- **Living artifacts:** Documents, models, analyses, and visualizations that evolve throughout an engagement. The investment thesis, the capability map, the scenario model - these are not deliverables produced at the end. They are shared working objects updated continuously.
- **Conversation history and memory:** The accumulated context of the driver-machine interaction. What has been discussed, decided, deferred, and discarded. This is the institutional memory of the node.
- **Knowledge graphs:** Structured representations of entities, relationships, and hierarchies relevant to the engagement. Market maps, capability taxonomies, organizational structures, portfolio configurations.

#### 3.3.2 Handoff Protocols

The rules governing when and how work transfers between the driver and the machine:

- **Driver-to-machine handoffs:** The driver defines the objective, provides context and constraints, and delegates execution. The machine produces drafts, analyses, models, or recommendations. The handoff must include clear scope, quality criteria, and any constraints or sensitivities the machine should respect.
- **Machine-to-driver handoffs:** The machine delivers output and flags items requiring human judgment. This includes uncertainties, anomalies, edge cases, and decisions that exceed the machine's authorized scope. The handoff must include a confidence assessment and a clear articulation of what the machine could and could not resolve.

For coordination between multiple agents within the machine, see Section 3.3.3.

#### 3.3.3 Multi-Agent Coordination

When the machine consists of multiple AI agents, the node operates in a distinct mode that requires its own coordination grammar. This is a first-class concept in the protocol, not a variant of driver-machine handoffs.

**The Architect-Implementer Pattern:**

The primary multi-agent pattern observed in practice is a two-agent configuration:

- **The Architect Agent** (e.g., Claude in architecture and presentation builds) - responsible for design decisions, quality standards, architectural consistency, and review. Sets the "what" and "why."
- **The Implementer Agent** (e.g., a second AI agent in the same builds) - responsible for code generation, build execution, and rapid production. Executes the "how."

The driver oversees the coordination but does not micromanage inter-agent task allocation. The driver's role is to set objectives, resolve ambiguities the agents escalate, and approve outputs that cross escalation thresholds.

**Coordination Artifacts:**

Multi-agent coordination requires explicit shared artifacts that maintain coherence between agents:

- **WORKBOARD.md:** A kanban-style task tracker that both agents read and update. Defines what's in progress, what's blocked, what's done, and what's next. The single source of truth for inter-agent work allocation.
- **HANDOFF_LOG.md:** A timestamped record of what was passed between agents - what was requested, what was delivered, what was flagged for review. This provides an auditable trail of the collaboration and enables the driver to understand the sequence of decisions without being present for every step.
- **Review and verification protocols:** Structured quality gates where one agent reviews another's output against defined criteria. The `/review` and `/verify` protocols encode this as executable instructions: review checks design intent and architectural consistency. Verify checks functional correctness and completeness.

**Why this matters at Level 0:**

Multi-agent coordination is not an implementation detail. It is a fundamental operating mode of the node that affects how work is structured, how quality is maintained, and how the driver maintains oversight. Any Layer 4 product or Layer 3 marketplace module that involves multiple agents must follow this coordination grammar to remain compatible with the protocol.

#### 3.3.4 Escalation Triggers

Mandatory points at which the machine must escalate to the driver for human authorization. These are **hardcoded into the protocol** and cannot be overridden by any agent or module:

**Tier 1 - Mandatory escalation (irreversible impact):**
- Any action that commits capital, signs agreements, or creates legal obligations.
- Any communication sent to external parties (clients, counterparties, regulators, boards).
- Any recommendation that would trigger an irreversible strategic decision (asset sale, market exit, organizational restructuring).
- Any situation where the machine detects it is operating outside its training distribution or confidence threshold.

**Tier 2 - Advisory escalation (significant impact):**
- Anomalies or contradictions in data that could change the engagement's direction.
- Findings that conflict with the working thesis or established assumptions.
- Situations where multiple valid strategic options exist and the choice depends on values, risk appetite, or political considerations the machine cannot assess.
- Stakeholder sensitivities detected in communications or documents.

**Tier 3 - Informational escalation (awareness):**
- Routine status updates on long-running tasks.
- New data that confirms or marginally updates existing analyses.
- Completed deliverables ready for driver review.

#### 3.3.5 Working Memory Persistence

The shared context described in Section 3.3.1 raises a critical architectural question: **what survives?** Specifically, what persists across sessions, across engagements, and across agents? This is a design decision, not an implementation detail, and it must be addressed at Level 0 because it determines how every Layer 4 product handles state.

**The Persistence Spectrum:**

| Persistence Level | What Survives | Current Implementation | Architectural Implication |
|---|---|---|---|
| **Ephemeral** | Nothing. State exists only within the current session. | Conversation context in Claude/Gemini. In-memory graph state in prototype applications. | Fast, lightweight, but requires full reconstruction at the start of each session. Suitable for exploratory analysis, prototyping, and single-session tasks. |
| **Session-persistent** | State survives within a single engagement but not across engagements. | Claude project memory. Working documents within a project folder. | Enables continuity within a multi-session engagement. The node can pick up where it left off. Requires explicit session context loading. |
| **Engagement-persistent** | State survives the full lifecycle of an engagement and is available for reference afterward. | `.md` files in working directories. SQLite or equivalent databases for structured data. Skill file versions. | The engagement becomes a permanent asset. Living artifacts (capability maps, assessment results, roadmaps) continue to evolve. This is the minimum persistence level for Layer 5 deployments. |
| **Cross-engagement persistent** | State survives across multiple engagements and accumulates as institutional knowledge. | Skill files that evolve through practice (e.g., v1 to v3+ through iterative engagement feedback). Reference architectures. Methodology documentation. | The protocol gets smarter over time. Patterns, methodologies, and domain knowledge compound across deployments. This is how the reference model improves. |

**The `.md` File as the Persistence Layer:**

In current practice, the `.md` file is the de facto persistence mechanism for the protocol. Skill files, strategy briefs, handoff logs, and workboards all persist as plain text files. This is a strength: `.md` files are portable, versionable, human-readable, machine-readable, and tool-agnostic. They work across Claude, Gemini, Claude Code, GitHub, and any future AI platform.

However, not all state belongs in `.md` files. Graph state (entity relationships, capability hierarchies, portfolio configurations) benefits from structured persistence - databases, graph stores, or serialized graph formats. The choice of SQLite + Prisma for this layer is an example of structured persistence for complex relational data.

**Architectural Decision:**

The protocol supports a hybrid persistence model:

- **`.md` files** are the canonical persistence layer for expertise, methodology, protocols, and narrative state (skill files, strategy documents, engagement logs, handoff records). These are the "source of truth" for what the node knows and how it operates.
- **Structured data stores** (databases, graph files, serialized state) are the persistence layer for entity-rich, relationship-heavy, or computationally intensive state (capability maps, portfolio configurations, market graphs, financial models). The specific technology is a Layer 4 product decision, but the principle is: if it has entities and relationships, it needs structured persistence.
- **Ephemeral state** is acceptable for exploratory, single-session work. But any output that informs a decision, feeds a living artifact, or contributes to institutional knowledge must be persisted before the session ends.

#### 3.3.6 Feedback Loops

The mechanisms by which the node learns and improves:

- **Intra-engagement learning:** The driver corrects the machine's outputs, refines skill files, adjusts interaction patterns. The machine's performance improves within the engagement as context accumulates.
- **Cross-engagement learning:** Patterns, methodologies, and skill file refinements from one engagement feed into the protocol for future deployments. The node gets better with each deployment because the skill files encode what was learned.
- **Skill file evolution:** Skill files are living artifacts. They are versioned, refined through iterative feedback, and improved based on real-world application. A mature skill file - refined through multiple engagements with iterative feedback - is the exemplar of this pattern. The process by which a skill file evolves from v1 to v3+ through real engagement feedback is a core mechanism of the protocol. It will be specified as a formal protocol in Level 1, Section 6.4 (Skill File Architecture).

---

## 4. Flows Across the System Boundary

### 4.1 Inputs to the Node

| Input | Source | Consumed By |
|---|---|---|
| Engagement mandate / problem statement | Client environment (principals) | Driver (interprets), Machine (contextualizes) |
| Client data (financials, documents, systems) | Client environment | Machine (processes), Driver (validates) |
| Market intelligence | Data environment | Machine (monitors, synthesizes), Driver (interprets strategically) |
| Stakeholder dynamics and political context | Client environment | Driver (reads, navigates) |
| Regulatory constraints | Regulatory environment | Both (machine checks compliance, driver exercises judgment) |
| External forces (market shifts, competitive moves) | External forces | Machine (detects, models), Driver (assesses implications) |
| Feedback on deliverables | Client environment (stakeholders) | Both (machine incorporates, driver recalibrates) |

### 4.2 Outputs from the Node

| Output | Produced By | Delivered To |
|---|---|---|
| Strategic recommendations | Both (machine drafts, driver validates and refines) | Client environment (principals, board) |
| Architecture artifacts (capability maps, value streams, operating models) | Machine (builds), Driver (reviews, calibrates to audience) | Client environment (stakeholders) |
| Living thesis / investment thesis | Both (machine maintains, driver steers) | Client environment (principals, CIO, CSO) |
| Scenario models and simulations | Machine (builds), Driver (defines parameters, interprets) | Client environment (decision-makers) |
| Deal qualification and pipeline intelligence | Both (machine scores, driver judges) | Client environment (M&A team, principals) |
| Engagement documentation | Machine (drafts), Driver (approves) | Client environment, regulatory environment |
| Refined skill files and methodology | Both (emerged from practice) | Plektis (Layer 1 / Layer 2 - feeds back into the platform) |

---

## 5. Operating Principles

The following principles govern how the node operates. They are architectural decisions, not preferences.

1. **The driver decides. The machine prepares.** The machine may recommend, model, draft, and analyze. It does not decide. Every output with strategic, financial, or legal consequence requires driver authorization.

2. **Iterative over waterfall.** The node works in tight loops. Draft, review, refine, extend. Long autonomous runs without driver checkpoints degrade output quality and risk compounding errors.

3. **Decoupled over monolithic.** Skill files, agents, and modules are designed to be independent and composable. A change to the market mapping agent should not break the scoring agent. The protocol supports plug-and-play at every level.

4. **Confidence-aware throughout.** The machine must communicate its confidence level in any output. High confidence on data synthesis. Low confidence on strategic inference. This allows the driver to calibrate how much review and judgment to apply.

5. **Graph-native over tabular.** Relationships between entities (companies, capabilities, markets, people) are first-class objects, not flat rows in a spreadsheet. The protocol thinks in networks and dependencies, not lists.

6. **Agentic over procedural.** The machine operates with agency within its authorized scope, making tactical decisions about how to execute tasks rather than following rigid step-by-step instructions. The driver sets the objective. The machine determines the path.

7. **Transferable by design.** Every engagement, skill file, and protocol must be documented clearly enough that another qualified driver can take over operations. The protocol does not depend on tacit knowledge that lives only in Krish's head.

---

## 6. What Level 1 Will Define

Level 1 decomposes the node into its functional subsystems. The planned decomposition (pending review of this Level 0):

- **6.1 Driver Capability Model:** What the human operator needs to know and do, organized by competency domain.
- **6.2 Machine Capability Model:** What the AI agent ensemble can do, organized by function (analysis, synthesis, monitoring, generation, coordination).
- **6.3 Interaction Protocol Specification:** Detailed handoff, escalation, and feedback loop protocols with message formats and quality gates.
- **6.4 Skill File Architecture:** The standard structure, versioning convention, and lifecycle for `.md` skill files - the protocol's core encoding format.
- **6.5 Application Mounting Protocol:** How domain-specific applications (capability assessment, operating model design, strategy execution) mount onto the protocol and access its services.
- **6.6 Multi-Agent Coordination Grammar:** The protocol for orchestrating multiple AI agents within a single node, including the architect-implementer pattern, handoff logs, and review/verify cycles.
- **6.7 Ecosystem Integration Protocol:** How Plektis integrates the evolving agentic ecosystem - runtimes, tools, encodings, and coordination standards - through additive Integration Profiles, keeping the core stable as the field moves.

---

## Version History

| Version | Date       | Summary |
|---------|------------|---------|
| 0.1.0   | 2026-06-02 | Initial public release. |
