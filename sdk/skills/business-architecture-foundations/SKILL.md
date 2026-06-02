---
name: business-architecture-foundations
description: >
  Foundational domain intelligence for business architecture practice.
  Covers capability mapping, value streams, the Business Motivation Model,
  and PPIT dimensional analysis. Load when working on capability assessments,
  operating model design, strategy-to-execution traceability, or any engagement
  where business architecture concepts are the analytical backbone.
license: CC BY-SA 4.0
compatibility: >
  Works with any AAIF-compatible agent. Draws on publicly available concepts
  from BIZBOK, BMM (OMG), and established EA practice.
metadata:
  plektis-version: "0.1.0"
  plektis-type: domain-intelligence
  plektis-domain: [business-architecture]
  plektis-author: Plektis Project
  plektis-status: active
  plektis-senref-phases: ["sense", "model", "decide"]
  plektis-confidence-profile: medium
  plektis-trust-level: first-party
  plektis-last-updated: "2026-06-02"
---

# Business Architecture Foundations

## Purpose

When this skill is loaded, the agent operates with foundational knowledge of business architecture concepts and vocabulary. It can structure capability maps, decompose value streams, trace strategy to execution through the Business Motivation Model, and assess capabilities against the four PPIT dimensions.

This is a starting point, not a complete methodology. It provides the conceptual vocabulary and structural patterns that a practitioner can extend with their own engagement methodology, sector-specific knowledge, and assessment instruments. Think of it as the grammar of business architecture, not the full language.

## Professional Context

Business architecture is the discipline of mapping an organisation's strategic intent to its operational structure. It answers the question: what does this organisation need to be capable of, and how well does it deliver those capabilities today?

The discipline draws on several established bodies of knowledge, including the Business Architecture Guild's BIZBOK Guide and the Object Management Group's Business Motivation Model (BMM). The concepts in this skill file are drawn from these publicly available frameworks and from general enterprise architecture practice. Practitioners typically adapt these concepts to their specific engagement context, sector, and client needs.

Business architecture is relevant across multiple engagement types: strategy execution, target operating model design, post-acquisition integration, digital transformation, capability-led investment planning, and organisational restructuring.

## Capability Mapping

### What a Capability Is

A business capability describes what an organisation can do, independent of how it does it. Capabilities are expressed as nouns ("Customer Relationship Management," "Financial Reporting," "Supply Chain Planning"), not as activities or processes.

The distinction matters: a capability is stable across organisational changes. The process, technology, and people that deliver a capability may change, but the capability itself persists. This makes capabilities the most useful unit of analysis for strategic planning.

### Capability Hierarchy

Capabilities are organised hierarchically, typically across three to four levels:

| Level | Scope | Example |
|---|---|---|
| **L1** | Enterprise-level grouping. Typically 15-25 across an organisation. | Supply Chain Management |
| **L2** | Functional decomposition of an L1. | Demand Planning, Procurement, Logistics, Warehousing |
| **L3** | Operational detail. The level at which most assessments are conducted. | Route Optimisation, Last-Mile Delivery, Carrier Management |
| **L4** | Granular sub-capabilities. Used selectively for deep-dive analysis. | Carrier Rate Negotiation, Delivery Window Scheduling |

**Naming conventions:** Capabilities should be named as noun phrases that describe what the organisation can do. Avoid verb-led names ("Managing Suppliers" should be "Supplier Management"). Avoid technology-specific names ("SAP Integration" should be "System Integration"). The capability name should make sense regardless of which team, tool, or process currently delivers it.

**Tier classification:** Capabilities are often classified by their strategic role:

| Tier | Description |
|---|---|
| **Strategic** | Directly differentiates the organisation in the market |
| **Operating** | Core to value delivery but not a differentiator |
| **Enabling** | Supports the other tiers (HR, Finance, IT, Legal) |

### Building a Capability Model

When constructing a Business Capability Model (BCM):

1. Start with a reference model for the sector if one is available. Adapting an existing model is faster and more reliable than building from scratch.
2. Validate L1 groupings with senior stakeholders. L1 names set the vocabulary for the entire engagement.
3. Decompose to L3 for capabilities that will be assessed. Decompose to L2 for everything else. Going to L4 everywhere creates an unmanageable model.
4. Cross-check for overlaps and gaps. If two capabilities sound similar, clarify the boundary. If a business function has no capability mapped to it, something is missing.

## Value Streams

### What a Value Stream Is

A value stream is a sequence of activities that delivers value to a stakeholder. Unlike a process (which describes how work flows), a value stream describes why work flows. It answers: what is the end-to-end journey that produces something a stakeholder values?

Value streams are decomposed into **stages**. Each stage has:

- **Entrance criteria:** What must be true before this stage can begin
- **Exit criteria:** What must be true for this stage to be considered complete
- **Value item:** The tangible output or asset produced by this stage

### Mapping Value Streams to Capabilities

The intersection of value streams and capabilities is where business architecture generates its most useful analysis. For each stage of a value stream, ask: which capabilities are engaged to deliver this stage?

This mapping produces **capability instances**: contextualised variants of a capability that are specific to a particular value stream stage. The same L3 capability ("Customer Data Management") may be instanced differently in the "Acquire Customer" value stream versus the "Service Customer" value stream, because the context, data, and performance requirements differ.

## Business Motivation Model (BMM)

### The Strategy-to-Execution Chain

The BMM (defined by the Object Management Group) provides a hierarchy that traces strategic intent down to measurable execution:

```
Vision
  └── Mission
       └── Goals (qualitative desired outcomes)
            └── Objectives (quantitative, measurable targets)
                 └── Strategies (broad approaches to achieve objectives)
                      └── Tactics (specific actions implementing strategies)
                           └── Initiatives (execution plans with timelines, resources)
```

Each level answers a different question:

| Level | Question |
|---|---|
| Vision | What do we aspire to become? |
| Mission | Why do we exist? |
| Goal | What outcomes do we want? |
| Objective | How do we measure progress? |
| Strategy | What approach will we take? |
| Tactic | What specific actions will we pursue? |
| Initiative | What will we build, change, or invest in? |

### Connecting BMM to Capabilities

The power of the BMM is its traceability. Every initiative should trace back to a tactic, which traces to a strategy, which traces to an objective, which traces to a goal. And every initiative should map forward to the capabilities it impacts.

This creates a complete chain: strategic intent → investment decision → capability impact → measurable outcome. If an initiative cannot trace to a strategic objective, it may not be justified. If a strategic objective has no initiatives supporting it, it is aspirational but unexecuted.

**Benefits traceability:** A Benefit connects an initiative to the objective it contributes toward and the KPI that measures it. This closes the loop:

```
Goal → Objective → Strategy → Tactic → Initiative → Capability Impact
                      ↑                                      │
                     KPI                                 [delivers]
                      ↑                                      │
                      └──── measures ──── Benefit ───────────┘
```

## PPIT Dimensional Analysis

### The Four Lenses

Capabilities describe what an organisation can do. The **PPIT dimensions** describe how that capability is delivered:

| Dimension | What It Covers | Key Questions |
|---|---|---|
| **People** | Organisational units, roles, skills, capacity | Who delivers this capability? Do they have the right skills? Is there adequate capacity? |
| **Process** | Business processes, workflows, automation level | How is the work done? Is it documented? What is the automation level? |
| **Information** | Data entities, information flows, data quality | What data does this capability consume and produce? Is the data reliable? |
| **Technology** | Applications, platforms, infrastructure | What systems support this capability? Are they fit for purpose? |

### Assessing Capabilities

A basic capability assessment scores each capability against two primary dimensions:

**Maturity** (how well-developed is the capability today):

| Level | Description |
|---|---|
| 1 - Initial | Ad hoc, inconsistent, dependent on individual knowledge |
| 2 - Developing | Some standardisation, but not consistently applied |
| 3 - Defined | Documented, standardised, consistently applied |
| 4 - Managed | Measured, optimised, data-driven improvement |
| 5 - Leading | Continuous innovation, industry benchmark |

**Strategic importance** (how critical is this capability to the organisation's strategy):

| Level | Description |
|---|---|
| 1 - Commodity | Required to operate but not a differentiator |
| 2 - Supporting | Enables other capabilities but is not directly strategic |
| 3 - Core | Central to value delivery |
| 4 - Differentiating | Creates competitive advantage |
| 5 - Transformative | Enables new business models or market entry |

The intersection of maturity and strategic importance reveals **capability gaps**: high-importance capabilities with low maturity are investment priorities. Low-importance capabilities with high maturity may be over-invested.

### The Operating Model

The operating model is not a single diagram. It is the collective description of how PPIT dimensions are configured against capabilities. When someone asks "show me the operating model," they are asking: for our most important capabilities, who delivers them, through what processes, using what data, on what technology?

A Target Operating Model (TOM) design defines the desired future state across all four PPIT dimensions for a set of capabilities, along with a transformation roadmap to get there.

## Roadmapping and Investment Prioritisation

### From Gaps to Action

Capability assessment reveals gaps. Roadmapping turns gaps into a sequenced plan. The question is not "what needs to improve" (the assessment answers that) but "in what order, over what timeframe, and with what resources."

### Investment Horizons

Initiatives are commonly classified by investment horizon:

| Horizon | Focus | Typical Timeframe |
|---|---|---|
| **Run** | Protect and maintain current capabilities. Fix what is broken. Address compliance and operational risk. | 0-6 months |
| **Grow** | Enhance existing capabilities to improve performance. Build on strengths. Close critical gaps. | 6-18 months |
| **Transform** | Create new capabilities that enable new business models, markets, or operating paradigms. | 12-36 months |

A healthy portfolio balances all three horizons. Over-investing in Run means the organisation maintains but does not improve. Over-investing in Transform without a solid Run foundation means the organisation is building on an unstable base.

### Sequencing Principles

When ordering initiatives into a roadmap:

1. **Dependencies first.** If Initiative B requires the output of Initiative A, A must be sequenced earlier. Map dependencies explicitly.
2. **Foundations before features.** Data quality, integration, and governance capabilities often need to be in place before higher-value capabilities can be improved.
3. **Quick wins create momentum.** Early waves should include at least one high-visibility, achievable initiative that demonstrates value to stakeholders.
4. **Group by transformation wave.** Initiatives that share dependencies, resources, or organisational impact are grouped into waves. Each wave should be independently valuable (not just a stepping stone to the next wave).

### The Roadmap as a Living Artifact

A roadmap is not a Gantt chart that gets approved and filed. It is a living artifact that evolves as the organisation learns. Assessment scores change as initiatives are delivered. New gaps emerge as the strategic context shifts. The roadmap is reviewed and adjusted at regular intervals, informed by the Reflect phase of the SenRef cycle.

## Stakeholder Management

### Why This Matters for Business Architecture

The most rigorous capability model is worthless if the people who need to act on it do not understand it, trust it, or feel ownership of it. Stakeholder management is not a soft skill adjacent to architecture work. It is a core competency that determines whether architecture outputs get implemented or filed.

### Stakeholder Mapping

For any business architecture engagement, identify the key stakeholders and understand their relationship to the work:

| Stakeholder Type | Their Concern | What They Need From You |
|---|---|---|
| **Executive sponsor** | Strategic alignment, ROI, board-ready narrative | Concise summaries, investment cases, progress against strategic objectives |
| **Functional leaders** | Impact on their teams, operational disruption, resource requirements | Honest assessment of current state, clear picture of what changes and when |
| **IT/Technology leaders** | Technical feasibility, system dependencies, integration complexity | Architecture views that map capabilities to applications and data |
| **Programme/project managers** | Scope, timeline, dependencies, resource allocation | Initiative details with sequencing, effort estimates, and dependency maps |
| **Front-line teams** | How their work changes, whether their input was heard | Evidence that assessment findings reflect their reality, not just executive assumptions |

### Calibrating Outputs to Audience

The same analytical content should be presented differently depending on the audience. The underlying architecture is consistent. The presentation adapts.

**For board and executive audiences:**
- Lead with the strategic narrative. What are we trying to achieve and why does this investment make sense?
- Use investment language (ROI, risk reduction, competitive positioning), not architecture language (L3 capabilities, PPIT dimensions, maturity scores)
- Visualise at L1/L2 level. Heatmaps showing where investment is needed, not detailed decomposition trees.

**For operational and technical audiences:**
- Lead with the detail. Show the capability model at L3, the value stream stages, the PPIT assessment results.
- Use architecture language. This audience understands and expects precision.
- Provide drill-down capability. Summaries that link to supporting detail.

**For workshop participants:**
- Lead with questions, not conclusions. Use the architecture as a framework for discussion, not a finished answer.
- Show current state first, invite reaction, then introduce the analysis.
- Capture dissent. If a stakeholder disagrees with an assessment score, that disagreement is data. Record it.

### Managing Resistance

Architecture work often reveals uncomfortable truths: capabilities that are weaker than assumed, investments that are not aligned to strategy, organisational structures that do not support the operating model. Resistance is a natural response.

Principles for navigating it:
- **Present findings as evidence, not judgment.** "The assessment indicates this capability is at maturity level 2" is evidence. "This team is underperforming" is judgment.
- **Acknowledge complexity.** Organisations are complex systems. A low maturity score may reflect under-investment, not incompetence. Frame gaps as investment opportunities, not failures.
- **Connect to the stakeholder's priorities.** A functional leader will engage with a finding if it connects to something they already care about. Disconnected findings feel like criticism.

## Quality Standards

When producing business architecture outputs with this skill loaded:

- **Use capability language, not activity language.** "Supply Chain Management" not "Managing the Supply Chain." Capabilities are nouns.
- **Trace everything.** Every initiative should connect to a strategy. Every assessment should connect to a strategic priority. If the thread breaks, flag it.
- **Distinguish between current state and target state.** Always be explicit about which you are describing. Mixing them in a single artifact creates confusion.
- **Score with evidence.** A maturity score without a rationale is an opinion. Anchor every score to observable evidence (documented processes, system capabilities, team capacity).
- **State your level of decomposition.** If you have only assessed to L2, say so. Do not imply L3 coverage you do not have.

## Anti-Patterns

1. **Naming capabilities as activities.** "Developing Products" should be "Product Development." If the name starts with a verb, rewrite it.
2. **Building a BCM from scratch when a reference model exists.** Adapting a sector reference model is faster and more reliable. Starting from zero invites structural gaps.
3. **Assessing every capability to the same depth.** Not all capabilities warrant L3 decomposition and detailed PPIT analysis. Focus depth on strategically important areas. Use lighter-touch assessment elsewhere.
4. **Treating the capability model as the deliverable.** The model is the analytical backbone. The deliverable is the insight it produces: where are the gaps, what should we invest in, what is the transformation sequence.
5. **Ignoring the information dimension.** People, process, and technology get attention. Information (data quality, data flows, master data management) is consistently under-assessed and is often the root cause of capability underperformance.
6. **Presenting architecture jargon to non-architects.** Board members do not need to know what "L3 capability decomposition" means. Translate into investment language: what we can do, how well we do it, what we need to improve, and what it will cost.
7. **Skipping the BMM traceability chain.** If initiatives are not traceable to strategic objectives, the investment case is weak. If strategic objectives have no supporting initiatives, the strategy is aspirational but unexecuted. Always close the loop.

## Extending This Skill

This foundations skill provides the vocabulary and structural patterns for business architecture. To build a more effective node for your specific practice, consider extending it with:

- **Sector-specific capability reference models** for your industry (healthcare, manufacturing, financial services, etc.)
- **Your firm's assessment instruments** and scoring methodologies
- **Stakeholder calibration patterns** for how you present architecture to different audiences
- **Engagement methodology** defining how you structure and sequence your BA work
- **Cross-domain connections** to adjacent disciplines (M&A integration, digital transformation, data architecture)

These extensions are where practitioners differentiate. The foundations are shared. The application is where value is created.

## Version History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 0.1.0 | 2026-06-02 | Krish Jogia | Initial public release. |
