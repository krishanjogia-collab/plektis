# Deployment Profile: Business Architecture

This sets up a Plektis node to do business architecture: mapping a business as its capabilities, value streams, information, and organisation, and keeping those maps current so strategy and execution stay connected. It covers what the node mounts, what it runs on, where it has to stop, and what it holds onto.

Business architecture is the blueprint, not the build. The maps are the shared view that operating-model design, investment cases, and transformation plans are built on. This node produces and maintains the view. The work that consumes it sits in other hands.

The domain knowledge here is public. Business architecture rests on BIZBOK and established practice, so the cognition mounts as an open skill rather than a private instrument. This profile is the wiring. The Business Architecture Foundations skill is the expertise that plugs into it, and the engagement playbooks that sharpen a real deployment stay private at Layer 4 or 5.

## What the node is for

A practitioner mapping a business is holding a lot at once: a capability map, a dozen stakeholder views, the value streams those capabilities enable, a heat map of where the gaps are, a roadmap that has to survive contact with the budget. This profile puts the machine on the modelling and the synthesis, and the driver on the judgment and the stakeholder relationships. Between them they produce work neither could alone, and the structure keeps the machine in its lane.

## How an engagement maps to SenRef

Every phase of an engagement runs as one or more turns of the cognitive cycle (L0, Section 3.2). The split between driver and machine holds the whole way through.

| Phase | SenRef | Machine | Driver |
|---|---|---|---|
| Framing and scope | Sense, Model | reads the strategy, the org, and the existing artifacts, frames the question | sets the mandate and the boundaries |
| Mapping | Model | builds the capability map and the value streams those capabilities enable | confirms what is real and what is aspirational |
| Heat-mapping | Sense, Model, Decide | overlays maturity, performance, and cost, finds the gaps, ranks them | reads what the gaps mean for the business |
| Initiatives and roadmap | Model, Decide | maps the initiatives back to the capabilities and sequences them | makes the trade-off calls |
| Deliverable and handover | Decide, Reflect | drafts the blueprints and the board-ready view, saves the maps, updates them | authorises, owns the stakeholder conversation |

## Where the machine stops

This is the protocol's three-tier escalation (L0, Section 3.3.4), set for architecture work. A loaded skill or a prompt cannot move these lines.

**Tier 1, the machine stops and waits for the driver.** Anything that goes to client stakeholders, a board, or a steering committee. Any recommendation to restructure an organisation or move headcount. Any commitment the client would act on as advice.

**Tier 2, the machine keeps going but flags it.** A heat-map result that cuts against what stakeholders believe about themselves. A finding that contradicts the stated strategy. A roadmap dependency that breaks the sequencing.

**Tier 3, the machine just tells you.** Progress on a long modelling pass. Drafts ready for review.

The machine reasons right up to the point of action and stops. It models, it maps, it drafts. It does not act. Sending a deliverable to a stakeholder, advising a restructure, signing off a roadmap, those stay with the driver, because the professional accountability for them cannot sit with a tool. That is the difference between a node and an agent let loose on a client.

## What the node runs on

The node draws these capability slots from the Toolchain Capability Map (Section 6.5):

- reasoning, for framing, modelling, heat-mapping, and drafting
- a structured store for the capability map, the value streams, and the cross-mappings between them, where the relationships are the point, not the rows
- document processing for the strategy papers, the org charts, and any existing architecture
- persistent context for the engagement state and the decisions behind the maps
- search and grounding for sector and peer benchmarks, when the engagement needs them

Each one reaches an outside system through MCP, under the escalation lines above.

## What the node remembers

The business architecture is the node's memory, a living set of maps. It says what the business does, how well it does it, and where it is heading, and it changes as the work teaches you. Every Reflect turn updates it. Every Sense turn reads it. The node keeps engagement state at minimum (Section 3.3.5), so it picks a multi-month engagement back up where it left off, and a second qualified driver can take it over without rebuilding the maps from scratch.

## What mounts

- Public: this profile, the [Business Architecture Foundations](../sdk/skills/business-architecture-foundations/SKILL.md) skill, and the shared vocabulary of the domain.
- Private, in a Layer 4 or 5 deployment: the engagement playbooks (mapping, heat-mapping, and roadmapping workflows) and the scored instruments that calibrate them.
- The bootloader is an AGENTS.md. It loads all of the above, sets the escalation lines, and starts the cycle.

A deployment is this profile with the foundations skill and the private playbooks mounted and a qualified driver at the helm.
