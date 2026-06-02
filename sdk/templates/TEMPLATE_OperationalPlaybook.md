---
# === AAIF Standard Fields ===
name: "your-skill-name"                    # kebab-case, must match directory name
description: >
  Describe when an agent should load this file. Write as a trigger condition.
  Max 1024 characters.
license: CC BY-SA 4.0
compatibility: >
  Designed for [domain] engagements. Works with Claude Code, Gemini,
  and other AAIF-compatible agents.
allowed-tools: Read Grep Glob             # space-separated, AAIF format

# === Claude Code Extensions (only if applicable) ===
user-invocable: true
argument-hint: "<scope> [options]"
# disable-model-invocation: false

# === Plektis Extensions (under metadata per AAIF convention) ===
metadata:
  plektis-version: "0.1"                      # start at 0.1 for drafts, 1.0 for production
  plektis-type: operational-playbook
  plektis-domain: "your-domain"               # e.g. business-architecture, valuations
  plektis-author: "Your Name"
  plektis-status: draft                       # draft | active | deprecated
  plektis-trust-level: first-party            # first-party | curated | community
  # plektis-senref-phases: ["decide"]           # which cognitive cycle phases this playbook executes
  # plektis-confidence-profile: low           # low | medium | high
  # plektis-role: any                         # architect | implementer | any
  # plektis-requires: []                      # skills that must be loaded alongside
  # plektis-references: []                    # companion files for deep content
  # plektis-last-updated: "YYYY-MM-DD"
---

# [Skill Name]

You are a [role description] performing [task description].

<!-- One-line role sentence. Sets the agent's operating frame. -->

## Scope: $ARGUMENTS

<!-- Required when user-invocable with argument-hint. -->

## Step 1: [First Step Name]

**Objective:** What this step achieves.

**Activities:**
- Activity 1
- Activity 2

**Output:** What this step produces.

**Quality gate:** What to verify before proceeding.

## Step 2: [Second Step Name]

<!-- Continue the workflow. -->

## Output Specification

<!-- Define the expected output format. Use fenced code blocks for templates. -->

## Quality Checklist

<!-- Verification checklist before finalizing output.
- [ ] Item 1
- [ ] Item 2
-->

<!-- OPTIONAL SECTIONS BELOW -->

<!-- ## Practitioner Guidance
- Tip 1
- Tip 2
-->

<!-- ## Version History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 0.1 | YYYY-MM-DD | Your Name | Initial creation |
-->
