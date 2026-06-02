# Deployment Profile: Portfolio and Transaction Strategy

This sets up a Plektis node to work on portfolio strategy and transactions. It covers what the node mounts, what it runs on, where it has to stop, and what it holds onto.

The deal expertise stays private. The judgment that wins a mandate, and the instruments that score and rank a pipeline, live in a Layer 4 or 5 deployment. This configuration is the wiring. The expertise plugs in behind it.

## What the node is for

One person running a portfolio or a live deal is holding too much at once: a data room, a market, a thesis, three counterparties, a board that wants an answer. This configuration puts the machine on the volume and the recall, and the driver on the judgment and the accountability. Between them they produce work neither could alone, and the structure keeps the machine in its lane.

## How an engagement maps to SenRef

Every phase of a deal runs as one or more turns of the cognitive cycle (L0, Section 3.2). The split between driver and machine holds the whole way through.

| Phase | SenRef | Machine | Driver |
|---|---|---|---|
| Thesis and origination | Sense, Model | reads the market and the portfolio, frames the thesis | decides what belongs, and why |
| Qualification | Decide | ranks candidates through the mounted instrument, states its confidence | makes the go or no-go |
| Diligence | Sense, Model | works the data room, reconciles it, flags what is missing | reads what the gaps mean |
| Structuring and negotiation | Model, Decide | models structures and scenarios, drafts terms | runs the negotiation, reads the room |
| Close and integration | Decide, Reflect | drafts the instruments, saves the state, updates the thesis | authorises, holds the relationship |

## Where the machine stops

This is the protocol's three-tier escalation (L0, Section 3.3.4), set for deal work. A loaded skill or a prompt cannot move these lines.

**Tier 1, the machine stops and waits for the driver.** Any contact with a counterparty, an intermediary, or a target: an approach, an indication, a number. Any commitment of capital or signature on a binding document. Any move that cannot be taken back, like an exit or a public step. Anything that leaves the node for a board, a principal, or a regulator.

**Tier 2, the machine keeps going but flags it.** A score that cuts against the stated thesis. A discrepancy in the data room it cannot resolve, which it raises rather than quietly papering over. A scenario that breaks the thesis.

**Tier 3, the machine just tells you.** Progress on a long read. Drafts ready for review.

The machine reasons right up to the point of action and stops. It models, it scores, it drafts. It does not act. Contacting a counterparty, committing capital, sending something out the door, those stay with the driver, because in this work the accountability for them cannot sit with a tool. That is the difference between a node and an agent let loose on a deal.

## What the node runs on

The node draws these capability slots from the Toolchain Capability Map (Section 6.5):

- reasoning, for framing, scoring, and drafting
- a structured store for the portfolio and its entities, where the relationships are the point, not the rows
- search and grounding for market, competitor, and entity signals
- document processing for the data room
- persistent context for the thesis
- code execution for scenario and valuation models

Each one reaches an outside system through MCP, under the escalation lines above.

## What the node remembers

The thesis is the node's memory, a living document. It says what the portfolio is building toward and what fits, and it changes as the work teaches you. Every Reflect turn updates it. Every Sense turn reads it. The portfolio and its entities sit in the structured store. The node keeps engagement state at minimum (Section 3.3.5), so it picks a months-long process back up where it left off, and a second qualified driver can take it over without rebuilding it from scratch. The judgment that sharpens across engagements goes into the private instruments, not into this public configuration.

## What mounts

- Public: this configuration and the shared vocabulary of the domain.
- Private, in a Layer 4 or 5 deployment: the scored qualification and pipeline instruments, the named portfolio and accountability frameworks, the scenario and competitive-situation playbooks, and the succession-signal taxonomy.
- The bootloader is an AGENTS.md. It loads all of the above, sets the escalation lines, and starts the cycle.

A deployment is this configuration with the private layer mounted and a qualified driver at the helm.
