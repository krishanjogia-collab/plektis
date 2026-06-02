---
# === AAIF Standard Fields ===
name: "your-skill-name"                    # kebab-case, must match directory name
description: >
  Describe when an agent should load this file. Write as a trigger condition,
  not a summary. Max 1024 characters.
license: CC BY-SA 4.0
compatibility: >
  Designed for [domain] engagements. Works with Claude Code, Gemini,
  and other AAIF-compatible agents.

# === Plektis Extensions (under metadata per AAIF convention) ===
metadata:
  plektis-version: "0.1"                      # start at 0.1 for drafts, 1.0 for production
  plektis-type: domain-intelligence
  plektis-domain: "your-domain"               # e.g. editorial, m-and-a-advisory, succession-planning
  plektis-author: "Your Name"
  plektis-status: draft                       # draft | active | deprecated
  plektis-trust-level: first-party            # first-party | curated | community
  # plektis-senref-phases: ["sense"]            # which cognitive cycle phases this skill configures
  # plektis-confidence-profile: low           # low | medium | high
  # plektis-requires: []                      # skills that must be loaded alongside this one
  # plektis-last-updated: "YYYY-MM-DD"
---

# [Skill Name]

<!-- Replace with the skill's display name. -->

## Purpose

<!-- 2-3 paragraphs. Answer: "When this file is loaded, what changes about
the agent's behaviour?" Be specific about the domain, the calibration effect,
and the types of output this skill governs. -->

## Professional Context

<!-- Domain scope, application context, firm or practice positioning.
Situate the skill within a real operational environment. Who uses this,
in what setting, for what kinds of engagements? -->

## [Domain Knowledge Section 1]

<!-- Name this section per your domain. This is where the substantive
intellectual content lives. Use H3 subsections for decomposition.
Tables are encouraged for structured data. -->

## [Domain Knowledge Section 2]

<!-- Add as many domain knowledge sections as the content requires. -->

## Quality Standards

<!-- Analytical, communication, and ethical standards that govern any output
produced while this skill is active. -->

## Anti-Patterns

<!-- What NOT to do. Named prohibitions, not vague guidelines. Number them. -->

<!-- OPTIONAL SECTIONS BELOW -->

<!-- ## Glossary

| Term | Definition |
|------|-----------|
| Term 1 | Definition |
-->

<!-- ## Version History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 0.1 | YYYY-MM-DD | Your Name | Initial creation |
-->
