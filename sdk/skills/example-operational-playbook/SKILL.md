---
name: example-operational-playbook
description: >
  Example skill file demonstrating the operational playbook format. This is
  a template with placeholder content showing the required structure, frontmatter
  fields, and section layout. Replace with your own workflow methodology.
license: CC BY-SA 4.0
compatibility: >
  Works with any AAIF-compatible agent. This is a format demonstration,
  not a functional skill.
user-invocable: true
argument-hint: "<example-argument>"
metadata:
  plektis-version: "0.1.0"
  plektis-type: operational-playbook
  plektis-domain: example
  plektis-author: Plektis Project
  plektis-status: active
  plektis-senref-phases: ["decide"]
  plektis-confidence-profile: low
  plektis-trust-level: first-party
  plektis-last-updated: "2026-06-02"
---

# Example Operational Playbook

You are a practitioner executing a structured workflow. This file demonstrates the operational playbook format.

## Scope: $ARGUMENTS

Replace this section with routing logic that determines how the playbook executes based on the arguments provided.

## Step 1: Define the Scope

**Objective:** Establish what this workflow will cover.

**Activities:**
- Activity 1
- Activity 2

**Output:** A scoped definition that constrains the remaining steps.

**Quality gate:** The driver confirms the scope before proceeding.

## Step 2: Execute the Analysis

**Objective:** Produce the core analytical output.

**Activities:**
- Activity 1
- Activity 2

**Output:** The primary deliverable of this workflow.

**Quality gate:** Output matches the quality criteria defined in the driver's handoff.

## Output Specification

Define what the final output looks like. Use a fenced code block to show the structure:

```markdown
# [Deliverable Title]

## Summary
[Key findings]

## Detail
[Supporting analysis]

## Recommendations
[Actionable next steps with confidence levels]
```

## Quality Checklist

- [ ] All scope items addressed
- [ ] Confidence levels stated for any inferred data
- [ ] Output matches the specification template above
- [ ] Escalation triggers checked (Tier 1 and Tier 2 items flagged to driver)
