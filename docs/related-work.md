# Related Work: Where Plektis Fits in the Landscape

Plektis draws on, integrates, and aims to complement a wide body of existing work across cognitive science, human-AI teaming research, enterprise architecture, agentic AI systems, and consulting thought leadership. This document maps the landscape and positions Plektis within it. It is organized by domain, with each section covering what exists, how Plektis relates to it, and where the differentiation lies.

Plektis is not a replacement for any of the work described here. It is an open protocol that occupies a specific gap: **the formal specification of how a senior human practitioner and AI agents operate as an integrated system**. The frameworks below describe pieces of this picture. Plektis aims to provide the connective tissue.

---

## 1. Cognitive Cycles and Decision Loops

The SenRef cognitive cycle (Sense → Model → Decide → Reflect) is a purposeful synthesis of established cognitive frameworks, adapted specifically for machine cognition within human-AI teaming contexts. It is not a novel invention. It stands on validated foundations while making specific, justified design choices.

### Primary Lineage

**Boyd's OODA Loop** (Observe → Orient → Decide → Act, ~1986) is the most direct ancestor. OODA's four-phase structure maps closely: Observe→Sense, Orient→Model, Decide→Decide, and Act→Reflect. That last pairing is the critical departure: SenRef replaces Act with Reflect, which makes it a cognition-only loop - the machine thinks but does not act. Action is a human prerogative, enforced through escalation triggers at the Decide phase boundary. Boyd's insight that Orient is the most important phase (building and updating mental models) directly informs SenRef's emphasis on the Model phase. OODA is experiencing a significant renaissance in 2024-2026 agentic AI discourse, with NVIDIA, Microsoft, IBM, and Gartner explicitly connecting agentic architectures to OODA-style loops.

**Friston's Active Inference** (~2009) provides the theoretical foundation for the Reflect phase. Active Inference formalizes how biological and artificial systems minimize prediction error by continuously updating their internal generative models. SenRef's Reflect phase operationalizes this principle: after a Decide output, the machine evaluates outcomes against predictions, updates its assumptions, and refines its skill files. The free energy minimization process in Active Inference is what SenRef's Reflect phase enacts in practical terms within an engagement context.

**Simon's Intelligence-Design-Choice Model** (1960) is the decision science foundation. Simon's three phases map to Sense (Intelligence - scanning the environment), Model (Design - generating alternatives), and Decide (Choice - selecting among alternatives). Simon's concept of "bounded rationality" - that decision-makers operate with limited information and cognitive capacity - directly motivates the node architecture: the machine extends the driver's cognitive capacity while the driver provides the judgment that the machine cannot.

**The ReAct Pattern** (Yao et al., Princeton/Google, 2022) is the most relevant precedent in contemporary LLM agent design. ReAct interleaves Thought (reasoning) and Action (tool use) with Observation (environment feedback) in a loop that has become the dominant paradigm in agentic AI. SenRef's relationship to ReAct: both are cognitive loops for AI agents, but ReAct is designed for autonomous tool-using agents while SenRef is designed for the machine side of a human-AI team. ReAct includes Action as a first-class phase. SenRef deliberately excludes it.

### Secondary Lineage

**BDI Agent Architecture** (Bratman, 1987; Rao & Georgeff, 1991) - the Belief-Desire-Intention model from multi-agent systems research. Perceive→Sense, Desire→Model, Intention→Decide, Belief Revision→Reflect. BDI's formal separation of what an agent believes, desires, and intends to do informs SenRef's phase boundaries.

**Reflexion** (Shinn et al., 2023) - the closest match to SenRef's Reflect phase in the LLM agent literature. Reflexion introduces verbal self-reflection as a mechanism for agent learning, with an Actor-Evaluator-Self-Reflection-Memory architecture. Its episodic memory buffer, where agents store linguistic reflections on past failures, parallels the skill file evolution mechanism in Plektis (where engagement learnings are encoded as updated skill files).

**Cynefin Framework** (Snowden, 1999) - Dave Snowden's sense-making framework for complex adaptive systems. Cynefin's domain-specific decision approaches (probe-sense-respond for complex systems, sense-categorize-respond for complicated systems) inform how SenRef adapts across engagement types. In complex domains (most of what Plektis addresses), the sensing comes before the modelling, which aligns with SenRef's phase ordering.

**PDCA / Deming Cycle** (Deming/Shewhart, 1950s) - Plan→Model+Decide, Do→(absent in SenRef), Check→Reflect, Act→(absent). The Deming cycle's emphasis on continuous improvement through feedback loops is embedded in SenRef's Reflect phase and in Plektis's broader skill file evolution mechanism.

**Kolb's Experiential Learning Cycle** (1984) - Experience→Sense, Reflective Observation→Reflect, Abstract Conceptualization→Model, Active Experimentation→Decide. Kolb's insight that learning requires both concrete experience and abstract conceptualization informs the dual nature of skill file evolution: driven by concrete engagement experience (intra-engagement learning) and abstract methodology refinement (cross-engagement learning).

**Haeckel's Sense-and-Respond** (IBM, 1992; *Adaptive Enterprise*, 1999) - the enterprise strategy lineage. Haeckel defined adaptive enterprises as organizations that sense changes in their environment and respond with appropriate action. This "sense and respond" concept is the organizational-level precursor to what SenRef formalizes at the practitioner-AI level. Plektis extends Haeckel's insight from organizational design to the operating model of the individual human-AI unit.

### What SenRef Adds

SenRef's defensible originality lies in three design choices that no prior framework combines:

1. **Cognition-only loop.** Replacing Act with Reflect encodes the architectural assumption that machines propose and humans dispose. This is a philosophical position on human-AI teaming, not a technical choice.
2. **Embedded within a broader operating system.** SenRef is the machine's internal cognition, not a standalone decision framework. It operates inside the interaction layer of the node, with the driver's judgment as the complementary system.
3. **Hardcoded escalation gateway.** The Decide → Reflect transition is where human-in-the-loop escalation triggers activate. No prior cognitive loop formally encodes HITL escalation as an architectural requirement rather than a safety bolt-on.

---

## 2. The Node: Human-AI Teaming Concepts

Plektis defines "the node" as the atomic unit of professional practice: one human driver integrated with one or more AI agents, operating as a single system. This concept has intellectual precursors across chess, defense research, management consulting, and academic computer science.

### The Centaur Model

Garry Kasparov's Advanced Chess concept (1998) is the foundational metaphor. After losing to Deep Blue in 1997, Kasparov proposed that a weak human + machine + better process beats either a strong human or a strong machine alone. This "centaur" model has been the dominant metaphor for human-AI collaboration for over two decades. The Harvard Data Science Review published a formal mathematical framework for centaurs in 2024 ("Effective Generative AI: The Human-Algorithm Centaur"), providing the most rigorous academic formalization to date. Plektis takes the centaur from metaphor to specification: the node is the centaur formalized, with defined protocols, escalation triggers, and a cognitive cycle.

### Academic Prior Art: The Nodal Approach

Mohammed et al. (2012), "A Nodal Approach to Modeling Human-Agents Collaboration" (International Journal of Computer Applications), explicitly defines a "node" as "a human actor, one or more agents, and their combined functions to represent a collective intelligent entity." A 2019 follow-up paper extends the concept. Plektis acknowledges this prior art directly. The conceptual alignment is strong. Plektis adds the operational specification (SenRef, skill files, escalation protocols, persistence architecture) that the academic model identified as necessary but did not provide.

### Defense and Government Research

**DARPA** has invested hundreds of millions across multiple human-machine teaming programs. The most relevant to Plektis include:

- **ACE (Air Combat Evolution)** - a hierarchical framework where humans handle strategy and AI handles tactics. This is structurally identical to the driver/agent split in Plektis and validates the architectural pattern.
- **ASIST (Artificial Social Intelligence for Successful Teams)** - AI systems with Theory of Mind capabilities for understanding human teammates. Relevant to future evolution of the interaction layer.
- **XAI (Explainable AI)** - $40M+ program (2017-2021) focused on making AI decision-making transparent to human operators. Directly relevant to SenRef's confidence-aware principle and the Tier 2 advisory escalation triggers.
- **COMPASS (Collection and Monitoring via Planning for Active Situational Scenarios)** - an AI decision-support tool that extends the OODA loop for military commanders. Demonstrates that cognitive loop adaptation for human-AI teaming is an active area of institutional investment.

**NATO HATOM (Human AI-Teaming Ontology Model)** - published by NATO's Science and Technology Organization. HATOM is a computational ontology for representing human-AI team structure, including autonomy, feedback, and trust dimensions. It is the closest formal ontological precedent for the node concept, though it is defense-specific. Plektis extends the ontological approach to civilian professional practice.

### Consulting Firm Frameworks

Three major consulting frameworks describe the same organizational phenomenon that Plektis formalizes:

**Accenture's "Collaborative Intelligence" / "Missing Middle"** (Wilson & Daugherty, *Human + Machine*, HBR Press, 2018) defined new roles at the human-AI boundary - Trainers, Explainers, and Sustainers. This was the first major consulting framework to describe dedicated human roles in human-AI collaboration. Plektis draws on this by formalizing the "driver" role, but goes further by specifying the interaction protocols and cognitive cycle rather than just naming the roles.

**Deloitte's "Superteams"** (2020 Global Human Capital Trends) describes the organizational unit that Plektis calls the node - humans and AI working together as an integrated team. Deloitte identified the concept. Plektis provides the specification for how the team operates.

**McKinsey's "Agentic Organization"** (2025, QuantumBlack) is the most recent and comprehensive consulting framework, describing organizations as networks of human + AI agent teams operating at near-zero marginal cost. This is the closest conceptual competitor. The differentiation: McKinsey describes the organizational model. Plektis specifies the operating protocol for the individual human-AI unit within that model. McKinsey's framework is proprietary thought leadership. Plektis is an open specification.

### Microsoft's HAX Toolkit

Microsoft's 18 Guidelines for Human-AI Interaction (CHI 2019, Best Paper award) are the industry gold standard for interaction design, organized into four temporal phases: initially, during interaction, when wrong, and over time. Plektis's interaction layer (handoff protocols, escalation triggers, feedback loops) is complementary: HAX defines general UX principles for human-AI interaction. Plektis specifies operational protocols for a specific class of professional human-AI teams.

### The Driver Certification Gap

A significant finding from the landscape research: **no established certification exists for the human half of human-AI teams**. Existing AI certifications focus on building AI (CertNexus CAIP, AWS ML), managing AI infrastructure (NVIDIA NCP), or governing AI (IAPP AIGP). The closest commercial precedents are emerging "AI Operator" training programs, but none provide formal, rigorous certification for operating AI-augmented professional workflows. This gap represents Plektis's most distinctive contribution to the field and a natural extension of the reference model.

---

## 3. Enterprise Architecture and Business Architecture

Plektis is designed to be methodology-agnostic. Business architecture (BIZBOK), enterprise architecture (TOGAF), and any other structured methodology can run on it. This section maps the current state of AI integration in these disciplines and identifies where Plektis sits.

### BIZBOK and the Business Architecture Guild

BIZBOK v15, released April 8, 2026, contains no AI-specific content, working group, or formal guidance on AI integration. The Guild addresses "growing complexity and rapidly evolving ecosystems" but has not published a position paper on AI-augmented business architecture practice. A member presentation at the 2022 Guild Summit discussed capability maps guiding AI transformation, but this was not a formal Guild position.

Plektis does not extend or modify BIZBOK. It operates at a different layer: BIZBOK defines what business architecture is (capabilities, value streams, information maps, business motivation). Plektis defines how the practitioner and AI work together to execute that architecture. A BIZBOK-certified practitioner using Plektis becomes more effective at BIZBOK methodology. The relationship is additive, not competitive.

### TOGAF and The Open Group

TOGAF 10 (April 2022) mentions AI governance in passing with no dedicated AI integration guidance or Architecture Development Method (ADM) phase update. The Open Group has launched a program to develop "open standards for AI professional practice" but this focuses on certifying professionals who architect and train AI models - a different scope from how AI changes architecture practice itself. If The Open Group publishes a TOGAF Series Guide on AI-integrated practice, it would be complementary to Plektis rather than competing with it: TOGAF would define the architecture methodology. Plektis would define the human-AI operating model for executing it.

### Forrester's "Augmented Architect"

Published in April 2025 by Charles Betz and Stephane Vanrechem, Forrester's "Augmented Architect" paradigm describes real-time AI-augmented enterprise architecture with closed-loop systems and specialized AI agents (harvesting agents, dependency agents, conformance agents). Forrester defines four emerging architect roles: Digital Twin Strategist, Enterprise Knowledge Curator, Agentic Governance Champion, plus a process-outcome orientation. Gartner's 2024 Hype Cycle includes "augmented architecture" as a recognized technology trend.

Plektis's relationship to the Augmented Architect vision: Forrester describes the "what" (what AI-augmented architecture looks like). Plektis provides the "how" (the operational specification for making it work). The Augmented Architect is a destination. Plektis is the protocol for getting there.

### EA Tool Vendors

The enterprise architecture tool market has undergone significant consolidation in 2024-2025, with the Bizzdesign + MEGA International + Alfabet merger creating a dominant platform entity. Every major vendor is shipping AI features:

- **SAP LeanIX** (Gartner Magic Quadrant Leader, five consecutive years) - AI copilot (Joule), AI document extraction, agentic AI gateway, MCP server integration
- **Ardoq** - AI Lens for shadow AI governance, read-only MCP gateway, EU AI Act compliance tooling, knowledge-graph-based reasoning
- **Bizzdesign + MEGA + Alfabet** - AI Center of Excellence, relation recommender, multi-agent orchestration capabilities
- **Capsifi** (acquired by Orbus Software, December 2024) - the most business-architecture-focused vendor in the market

All vendors solve "how to use AI within an EA tool." Plektis addresses the fundamentally different question: "how to redesign architecture practice itself for human-AI collaboration." These are complementary, not competitive. Plektis is tool-agnostic by design - its skill files and protocols can be used alongside any of these platforms.

---

## 4. Agentic AI Ecosystem

Plektis exists within a crowded ecosystem of agentic AI frameworks, protocols, and standards. Understanding its position in this stack is essential for practitioners and developers.

### Position in the Agentic AI Stack

The agentic AI stack can be understood in four layers:

1. **Foundation Models + Protocols** - GPT-4o, Claude, Gemini, MCP (Model Context Protocol), A2A (Agent-to-Agent)
2. **Multi-Agent Frameworks** - LangGraph, CrewAI, Google ADK, Microsoft Agent Framework
3. **Orchestration Platforms** - PwC agent OS, Agno AgentOS, AG2
4. **Domain Application** - where Plektis sits

Plektis operates at the domain application layer, encoding professional practice expertise as structured AI agent configurations. It is complementary to, and runs on top of, the frameworks and platforms below. It does not compete with LangGraph, CrewAI, or any orchestration platform. It uses them.

The major providers' managed agent runtimes - Anthropic Managed Agents, AWS Bedrock AgentCore, Google Vertex AI Agent Engine, and the OpenAI Agents SDK harness - are the emerging hosted substrate for this layer. They are converging on a common shape: durable sessions, sandboxed tools, MCP and the emerging A2A protocol, and human-in-the-loop controls. Plektis runs on the category as one option among several. How each maps onto Plektis primitives is catalogued in the Integration Profile Registry, defined in Reference Model Section 6.7 (Ecosystem Integration Protocol).

### Multi-Agent Frameworks

**LangGraph** has the most mature human-in-the-loop primitives among current frameworks, with native interrupt_before/interrupt_after on nodes and state persistence for pause/resume. This aligns well with Plektis's escalation trigger architecture.

**CrewAI's** role/goal/backstory paradigm for agent definition most closely mirrors Plektis's skill file philosophy of role-based team structures.

**Google ADK** provides structured workflow agents (Sequential, Parallel, Loop) as built-in primitives, relevant to Plektis's multi-agent coordination grammar.

**Microsoft's Agent Framework** (successor to AutoGen) and **OpenAI's Agents SDK** (successor to the short-lived Swarm) demonstrate rapid consolidation in this space. Plektis remains framework-agnostic to avoid dependency on any single platform that could be deprecated.

### The Skill File Convergence

A significant validation of Plektis's approach: every major AI coding tool has independently converged on the same pattern of markdown files encoding domain expertise and behavioral rules. CLAUDE.md (Claude Code), .cursorrules (Cursor), AGENTS.md (OpenAI Codex CLI), GEMINI.md (Gemini CLI), copilot-instructions.md (GitHub Copilot), and .windsurfrules (Windsurf) all follow this model.

This convergence validates the core mechanism of Plektis skill files. The differentiation: existing implementations are coding-focused and single-agent. Plektis skill files provide a structured application of this pattern to professional domain expertise across business architecture, strategy execution, operating model design, and advisory practice.

### The Agentic AI Foundation (AAIF)

The Linux Foundation's Agentic AI Foundation, announced in 2026, anchors open governance around Model Context Protocol (MCP), the goose agent framework, and AGENTS.md. The AAIF's Agent Skills standard (SKILL.md format) aligns with Plektis's skill file architecture. Plektis skill files are compatible with the emerging AAIF ecosystem while adding domain-specific structure (YAML frontmatter with SenRef phase mapping, methodology references, and escalation metadata) that the generic standard does not address.

The relationship between MCP and Plektis skill files is complementary: MCP defines how agents connect to external tools and data (active connectivity). Skill files define how agents think and behave within a specific domain context (passive expertise). Both are needed. An agent running Plektis skill files uses MCP to access external systems while following the skill file's methodology and escalation protocols.

### Security Considerations

Research on adversarial attacks against community-sourced agent skills (notably the ClawSafety initiative, which modelled data-exfiltration and prompt-injection attacks via poisoned SKILL.md files across 120 adversarial scenarios) highlights the security implications of open skill file ecosystems. Plektis addresses this through its trust level architecture (first-party, curated, community) and the security constraints defined in the skill file specification.

---

## 5. Open-Source Methodology Precedents

Plektis's open-source approach draws from established precedents for publishing professional methodologies openly.

### SAFe (Scaled Agile Framework)

SAFe publishes its full framework freely at scaledagile.com. It has become the dominant scaled agile methodology with 2M+ professionals trained, demonstrating that open publication of a methodology drives adoption rather than undermining it.

### The Scrum Guide

Published under Creative Commons BY-SA 4.0. Multiple certification bodies have built successful programmes around the same open content, demonstrating that open licensing and professional certification complement each other.

### Wardley Mapping

Simon Wardley's approach - fully open under Creative Commons, adopted by UK government - demonstrates that radical openness can establish authority for an individual practitioner. This is a useful precedent for creator-led open-source methodology projects.

### Plektis's Approach

Plektis publishes its reference model freely under CC BY-SA 4.0. The relationship to existing standards is complementary: BIZBOK defines what business architecture is. TOGAF provides the enterprise architecture methodology. Plektis defines how practitioners and AI work together to execute these methodologies. Each serves a different layer of the same practice.

---

## 6. Summary: Where Plektis Fills the Gap

| Dimension | What Exists | What Plektis Adds |
|---|---|---|
| **Cognitive cycles** | OODA, PDCA, ReAct, Active Inference - general-purpose | SenRef: cognition-only loop designed for machine side of human-AI teams, with escalation gateway |
| **Human-AI teaming** | Centaur metaphor, DARPA programs, consulting thought leadership | Formal, open specification for the operating unit: protocols, skill files, escalation triggers, persistence |
| **Business architecture + AI** | BIZBOK (silent on AI), TOGAF (no AI methodology), vendor features | Methodology-agnostic protocol that any architecture practice can adopt |
| **Agentic AI** | LangGraph, CrewAI, MCP, AAIF - infrastructure for building agents | Domain application layer encoding professional expertise as structured agent configurations |
| **Skill files** | CLAUDE.md, AGENTS.md, .cursorrules - coding-focused | First structured application to professional domain expertise beyond software development |
| **Consulting frameworks** | McKinsey Agentic Organization, Deloitte Superteams, Accenture Missing Middle | Open specification that complements proprietary thought leadership |
| **Driver certification** | No established certification for the human operator of AI-augmented professional workflows | An area Plektis identifies as important and aims to contribute to |

The field of AI-augmented professional practice is evolving rapidly. BIZBOK, TOGAF, and the analyst community will continue to develop their own perspectives on AI integration. Plektis aims to contribute an open, community-owned protocol that complements these efforts and provides practitioners with an implementable specification they can adopt and extend.

---

## References

### Cognitive Cycles
- Boyd, J. (1986). "Patterns of Conflict." Unpublished briefing.
- Friston, K. (2009). "The free-energy principle: a rough guide to the brain." Trends in Cognitive Sciences.
- Simon, H. (1960). "The New Science of Management Decision." Harper & Row.
- Yao, S. et al. (2022). "ReAct: Synergizing Reasoning and Acting in Language Models." arXiv:2210.03629.
- Bratman, M. (1987). "Intention, Plans, and Practical Reason." Harvard University Press.
- Rao, A. & Georgeff, M. (1991). "Modeling rational agents within a BDI-architecture." KR '91.
- Shinn, N. et al. (2023). "Reflexion: Language Agents with Verbal Reinforcement Learning." arXiv:2303.11366.
- Snowden, D. (1999). "Liberating Knowledge." Cynefin Centre.
- Deming, W.E. (1986). "Out of the Crisis." MIT Press.
- Kolb, D. (1984). "Experiential Learning." Prentice Hall.
- Haeckel, S. (1999). "Adaptive Enterprise: Creating and Leading Sense-And-Respond Organizations." Harvard Business School Press.

### Human-AI Teaming
- Mohammed, S. et al. (2012). "A Nodal Approach to Modeling Human-Agents Collaboration." International Journal of Computer Applications, 43(12).
- Kasparov, G. (1998). Advanced Chess concept, first played in Leon, Spain.
- Harvard Data Science Review (2024). "Effective Generative AI: The Human-Algorithm Centaur."
- Wilson, H.J. & Daugherty, P. (2018). "Human + Machine: Reimagining Work in the Age of AI." HBR Press.
- Deloitte (2020). "Global Human Capital Trends: The Social Enterprise at Work." (Superteams concept.)
- McKinsey / QuantumBlack (2025). "The Agentic Organization."
- Amershi, S. et al. (2019). "Guidelines for Human-AI Interaction." CHI 2019.
- DARPA programs: ACE, ASIST, XAI, COMPASS.
- NATO Science and Technology Organization. HATOM (Human AI-Teaming Ontology Model).

### Enterprise Architecture
- Business Architecture Guild. BIZBOK Guide v15 (April 2026).
- The Open Group. TOGAF Standard, Version 10 (April 2022).
- Betz, C. & Vanrechem, S. (2025). "The Augmented Architect: Real-Time Enterprise Architecture In The Age Of AI." Forrester.
- Gartner (2024). Hype Cycle for Enterprise Architecture.

### Agentic AI Ecosystem
- Agentic AI Foundation (AAIF), Linux Foundation (2026). MCP, AGENTS.md, Agent Skills.
- LangChain / LangGraph. langchain.com/langgraph.
- CrewAI. crewai.com.
- Google Agent Development Kit (ADK). google.github.io/adk-docs.
- Microsoft Agent Framework. github.com/microsoft/autogen (evolved).
- ClawSafety adversarial research (2026). Agent skill supply-chain security.
- arXiv (2026). "AI Skills as the Institutional Knowledge Primitive for Agentic Software Development." arXiv:2603.14805.

### Open-Source Strategy
- SAFe (Scaled Agile Framework). scaledagile.com.
- Schwaber, K. & Sutherland, J. (2020). "The Scrum Guide." scrumguides.org.
- Wardley, S. Wardley Mapping. Creative Commons.
