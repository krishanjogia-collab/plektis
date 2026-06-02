---
name: example-domain-intelligence
description: >
  Example skill file demonstrating the domain intelligence format. This is
  a template with placeholder content showing the required structure, frontmatter
  fields, and section layout. Replace with your own domain expertise.
license: CC BY-SA 4.0
compatibility: >
  Works with any AAIF-compatible agent. This is a format demonstration,
  not a functional skill.
metadata:
  plektis-version: "0.1.0"
  plektis-type: domain-intelligence
  plektis-domain: example
  plektis-author: Plektis Project
  plektis-status: active
  plektis-senref-phases: ["sense", "model"]
  plektis-confidence-profile: low
  plektis-trust-level: first-party
  plektis-last-updated: "2026-06-02"
---

# Example Domain Intelligence Skill

## Purpose

This file demonstrates the domain intelligence skill file format. When loaded, a domain intelligence skill calibrates how the agent thinks about a specific domain. It provides persistent context, not step-by-step instructions.

Replace this section with a description of what changes about the agent's behaviour when your skill is loaded.

## Professional Context

Describe the domain this skill covers, who uses it, and in what engagement context. Situate the skill within a real operational environment.

## [Your Domain Knowledge Sections]

This is where the substantive content lives. Organise by the natural structure of your domain. Use tables for structured data (taxonomies, scoring frameworks, signal models). Use subsections for distinct conceptual areas.

A real skill file might have sections like:
- Industry-specific signal taxonomy
- Scoring methodology with defined bands
- Data source quality assessment
- Module-specific framing for different use cases

## Quality Standards

Define the analytical, communication, and ethical standards that govern any output produced while this skill is active.

## Anti-Patterns

List what NOT to do. Number them for easy reference. These should be specific enough that someone could accidentally violate them.

1. Do not present inferred data with the same confidence as verified data.
2. Do not use generic AI-sounding language in deliverables.
3. Do not skip the confidence assessment on any substantive output.
