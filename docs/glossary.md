# Glossary

| Term | Definition | Scope |
|---|---|---|
| **Plektis** | An open protocol for human-AI teaming. The collective name for the reference model, SDK, and community ecosystem. | Everything |
| **Reference Model** | Layer 1. The open-source foundation defining the protocols for human-machine teaming. | Layer 1 |
| **SDK** | Layer 2. Developer tools and scaffolding (skill files, templates) enabling practitioners to configure their own implementations. | Layer 2 |
| **Marketplace** | Layer 3. A curated distribution channel for quality-reviewed modules and features (planned). | Layer 3 |
| **First-Party Products** | Layer 4. Proprietary applications built on top of the protocol. | Layer 4 |
| **Integrated Deployment** | Layer 5. The human-machine node deployed into a client environment with a qualified driver. | Layer 5 |
| **Platform** | Layers 1-3 collectively. The open ecosystem. | Layers 1-3 |
| **Layer vs Level** | Layers are the product stack (Layer 1 Reference Model through Layer 5 Integrated Deployment). Levels are the reference model's own decomposition (Level 0 The Node, Level 1 subsystems). Different axes. | Orientation |
| **Node** | The integrated human-machine unit. One practitioner fused with one or more AI agents, operating as a single system. | Conceptual |
| **Driver** | The qualified human operator who runs the protocol in a live engagement. | Layer 5 |
| **Machine** | The AI component of a node: one or more agents that sense, model, decide, and reflect under the driver's direction. | Conceptual |
| **SenRef** | The cognitive cycle: Sense, Model, Decide, Reflect. Defines how the machine component of the node processes information. Named as a continuum from Sense through Reflect. | Cognitive Cycle |
| **Sense** | Ingesting, monitoring, detecting, and extracting data from external sources and working memory. | Cognitive Phase |
| **Model** | Structuring, mapping, simulating, and building representations of reality. | Cognitive Phase |
| **Decide** | Scoring, qualifying, recommending, prioritising, and drafting deliverables. | Cognitive Phase |
| **Reflect** | Evaluating outcomes, updating assumptions, refining skill files, persisting learnings. | Cognitive Phase |
| **Skill File** | A structured `.md` file that encodes practitioner expertise as machine-readable instructions. Conforms to the AAIF Agent Skills standard. | Technical |
| **Domain Intelligence** | A skill file type that provides persistent context, calibrating how the agent thinks. | Skill File Type |
| **Operational Playbook** | A skill file type that provides executable instructions, defining what the agent does. | Skill File Type |
| **Configuration** | An assembled node: domain intelligence and operational playbook skill files with an AGENTS.md bootloader, ready to run as the machine half of a node. | Technical |
| **Deployment Profile** | The public description of how a node is configured for a domain. Shows what mounts, how the engagement maps to SenRef, where the machine stops, and what stays private. Lives in `configurations/`. | Public artifact |
| **Integration Profile** | The additive artifact that maps an external runtime onto Plektis primitives. Lives in `integrations/`. Adding one never changes the core. | Ecosystem |
| **Application** | A kind of professional work that mounts onto the protocol, such as a capability assessment or a portfolio engagement. Combines public components with a private Layer 4 / Layer 5 layer. | Conceptual |
| **Trust Level** | The provenance classification of a skill file: first-party (authored by the driver), curated (marketplace-reviewed), or community (unverified). | Security |
| **MCP (Model Context Protocol)** | The AAIF standard for connecting AI agents to external tools, data, and systems. The active integration layer that complements skill files (the cognitive layer). | Integration |
| **AAIF (Agentic AI Foundation)** | The Linux Foundation initiative stewarding open standards for agentic AI, including MCP, Agent Skills, and AGENTS.md. | Ecosystem |
| **Agent Skills** | The AAIF standard for SKILL.md files. Defines the universal format for encoding agent behaviour. | Standard |
| **AGENTS.md** | The AAIF standard for repository-level agent initialisation. The bootloader that configures an agent entering a codebase. | Standard |
