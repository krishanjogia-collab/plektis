# Plektis

**An open protocol for human-AI teaming.**

Plektis defines a new unit of professional practice: the integrated human-AI node. It specifies how a senior practitioner and AI agents operate as a single system - with shared context, coordinated decision-making, and formal escalation protocols. It provides the cognitive cycle (SenRef), the interaction protocols, and the skill file format for encoding domain expertise as machine-readable instructions. Published domains ship as Deployment Profiles that show the protocol running a domain as a node.

## Charter
This is a human-AI teaming protocol. The methodologies it runs are pluggable - investment thesis development, capability mapping, M&A scenario planning, value stream analysis, operating model design, or any structured professional practice. It is specific enough to be credible, broad enough to not be boxed in by one peak body's definition.

## How Plektis is used

Plektis is bootable. The path from spec to working node:

1. **Assemble a configuration** with the build kit (the [SDK](sdk/README.md)). A configuration is a set of skill files - domain intelligence plus operational playbooks - together with an `AGENTS.md` bootloader that tells an AI agent how to operate as the machine half of a node.
2. **Mount it** via the application mounting protocol ([Section 6.5](reference-model/L1/6.5-application-mounting.md)): provision the toolchain and MCP connections, load the skill files, configure persistence and the escalation profile, and initialise the SenRef cycle.
3. **Run it** - either as a **node** (a human driver working with an AI machine as a single unit) or packaged as **bundled software** (a first-party product or a marketplace module).

See the [Reference Configuration](docs/reference-configuration.md) for a complete worked example.

## Where to start

Plektis is meant to be read in order. The folders sort alphabetically on GitHub, so follow this path rather than the file listing:

1. **This README:** What Plektis is, and how a node is assembled and run.
2. **[Reference Model](reference-model/README.md):** Start with [Level 0](reference-model/L0-the-node.md) for the node and the SenRef cycle, then the Level 1 sections, 6.1 through 6.7, for each subsystem.
3. **[SDK](sdk/README.md):** The skill file format, with a working skill to build from.
4. **[Deployment Profiles](configurations/README.md)** and **[Integration Profiles](integrations/README.md):** What it looks like to run a domain as a node, and how Plektis sits on the wider agentic ecosystem.
5. **[Reference Configuration](docs/reference-configuration.md):** A complete worked node with real tools and agents.
6. **[Glossary](docs/glossary.md)** and **[Related Work](docs/related-work.md)** for reference, and **[AGENTS.md](AGENTS.md)** as the bootloader when you run a node.

## Related Work

Plektis draws on and integrates concepts from across cognitive science, human-AI teaming research, enterprise architecture, and agentic AI:

- **Cognitive cycles:** OODA Loop (Boyd), Active Inference (Friston), Simon's Intelligence-Design-Choice, ReAct (Yao et al.), BDI Agent Model, Reflexion (Shinn et al.)
- **Human-AI teaming:** Kasparov's Centaur model, Mohammed et al.'s Nodal Approach, DARPA ACE/ASIST/XAI, NATO HATOM, Microsoft HAX Toolkit
- **Consulting frameworks:** McKinsey "Agentic Organization" (2025), Deloitte "Superteams" (2020), Accenture "Collaborative Intelligence" (2018)
- **Enterprise architecture:** BIZBOK (Business Architecture Guild), TOGAF (The Open Group), Forrester "Augmented Architect" (2025)
- **Agentic AI ecosystem:** AAIF (MCP, Agent Skills, AGENTS.md), LangGraph, CrewAI, Google ADK
- **Open methodology precedents:** SAFe, Scrum Guide, Wardley Mapping

Plektis aims to complement this body of work by offering an open, implementable specification for practitioners. For the full landscape analysis, see [Related Work](docs/related-work.md).

## Status
v0.1.0 (under active development)

## License
CC BY-SA 4.0

*Created by Krish Jogia*
