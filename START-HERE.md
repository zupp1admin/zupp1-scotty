# Start Here: USS Zupp1

Welcome to The Book, Zupp1's canonical institutional memory.

This page is the shortest path to understanding what Zupp1 is, how the crew operates, where current work lives, and how new knowledge should be preserved.

## Five-minute orientation

Read these documents in order:

1. [Mission](Operations-Manual/01-Mission.md): why Zupp1 exists.
2. [Values](Operations-Manual/02-Values.md): the principles that govern behavior.
3. [Decision Doctrine](Operations-Manual/06-Decision-Doctrine.md): how choices should be made.
4. [Standing Orders](Operations-Manual/04-Standing-Orders.md): permanent operating directives.
5. [Mission Status](Operations-Manual/05-Mission-Status.md): current operational context.
6. [Mission Queue](Research/Mission-Queue/Mission-Queue.md): active, queued, completed, and deferred intelligence work.

For the complete file-by-file directory, use the [repository index](README.md).

## Core doctrine

> Toda boa escolha começa com compreensão.

Zupp1 exists to help people make better decisions through understanding. Education is currently a guiding hypothesis, not a proven competitive advantage. It becomes an advantage only after it produces observable customer behavior and, eventually, an identity customers express in their own words.

The operating sequence is:

1. **Hypothesis:** Education creates trust.
2. **Observable behavior:** Visitors demonstrate greater understanding, confidence, engagement, return, purchase, or recommendation.
3. **Identity:** Customers independently describe Zupp1 as a place that explains things and helps them decide.

## Repository map

| Area | Purpose | Start with |
|---|---|---|
| `Operations-Manual/` | Mission, values, command structure, doctrines, protocols, and standing orders | [Mission](Operations-Manual/01-Mission.md) |
| `Research/` | Intelligence reports, strategic assessments, measurement frameworks, and mission control | [Mission Queue](Research/Mission-Queue/Mission-Queue.md) |
| `Engineering/` | Reusable implementation standards and technical decisions | [WordPress Editing Standards](Engineering/WordPress-Editing-Standards.md) |
| `Customer-Experience/` | Atendimento doctrine, workflows, and customer-facing standards | [Central de Atendimentos](Customer-Experience/Central-de-Atendimentos.md) |
| `Bridge-Logs/` | Operational records organized by officer or function | [Bridge Logs index](README.md#bridge-logs) |
| `Captain-Logs/` | Significant leadership decisions, milestones, and context | [Captain's Logs index](README.md#captains-logs) |
| `Philosophy/` | Enduring cultural and strategic principles | [Founding Principles](Philosophy/Founding-Principles.md) |
| `Poetry/` | Creative work that forms part of Zupp1's identity | [Poetry index](README.md#poetry) |

## Choose your route

### Captain or bridge leadership

1. Review [Mission Status](Operations-Manual/05-Mission-Status.md).
2. Review the [Mission Queue](Research/Mission-Queue/Mission-Queue.md).
3. Read the latest relevant research or bridge log.
4. Record significant decisions with their rationale.

### Research and intelligence

1. Read the [Research Protocol](Operations-Manual/07-Research-Protocol.md).
2. Confirm that the work has a decision to improve.
3. Check the [Mission Queue](Research/Mission-Queue/Mission-Queue.md) before beginning.
4. Use the [Mission Report Template](Research/Mission-Report-Template.md) for the deliverable.
5. Separate evidence, reasoning, proposals, and unknowns using the required labels below.
6. Archive completed work and update mission status.

### Engineering

1. Review current standards in `Engineering/`.
2. Preserve the reason behind implementation decisions, not only the final code or configuration.
3. Convert reusable fixes into engineering standards.
4. Record deprecated or superseded practices without erasing historical context.

### Customer experience

1. Begin with the [Customer Service Doctrine](Operations-Manual/09-Customer-Service-Doctrine.md).
2. Review [Central de Atendimentos](Customer-Experience/Central-de-Atendimentos.md).
3. Treat recurring customer confusion as product and knowledge-system evidence.
4. Preserve durable service lessons while excluding unnecessary customer data.

## Required evidence labels

Use these labels whenever evidence, interpretation, and action could be confused:

- **FACT:** Verified information supported by an identified source or direct observation.
- **ASSESSMENT:** Reasoning, interpretation, or judgment derived from available evidence.
- **RECOMMENDATION:** A proposed course of action.
- **INTELLIGENCE GAP:** Information that could not be verified or is not yet known.

Never convert an assumption into a fact merely because it has been archived.

## Knowledge lifecycle

Knowledge moves through this sequence:

1. Idea
2. Discussion
3. Decision
4. Implementation
5. Validation
6. Archive in The Book
7. Future review

Slack is the operational conversation layer. GitHub is the canonical knowledge layer. Important work should be summarized in Slack and preserved here with enough context for a future officer to understand the decision.

The governing policy is [SO-004: Knowledge Preservation and Information Lifecycle](Operations-Manual/11-SO-004-Knowledge-Preservation-and-Information-Lifecycle.md).

## Standard document template

Use only the sections that serve the document. Do not preserve empty headings.

```markdown
# [Document title]

**Status:** Draft / Active / Complete / Deferred / Superseded / Deprecated / Historical Context
**Owner:** [Officer or function]
**Date:** YYYY-MM-DD
**Authority or request:** [Decision, mission, standing order, or requester]

## Purpose

[What question, decision, standard, or operational need does this document address?]

## Context

[What happened, and what must a future reader know?]

## Evidence

**FACT:** [Verified evidence with a source or direct observation.]

**INTELLIGENCE GAP:** [Important information that remains unknown.]

## Assessment

**ASSESSMENT:** [Reasoning, implications, trade-offs, and confidence.]

## Decision or recommendation

**RECOMMENDATION:** [Proposed action, owner, timing, and stopping rule.]

or

**DECISION:** [Approved action, authority, date, and rationale.]

## Implementation or future use

[How should future officers apply, validate, review, or reactivate this knowledge?]

## Related material

- [Relative link to related document]
```

## Preservation checklist

Before archiving, confirm that the document:

- answers what happened and why it mattered;
- preserves the reason behind the decision;
- distinguishes facts from assessments and recommendations;
- labels unverified information as an intelligence gap;
- links to related standards, missions, or evidence;
- records an owner, status, and date when applicable;
- contains no passwords, tokens, financial credentials, or unnecessary personal data;
- leaves Zupp1 more understandable than before.

## Status conventions

- **Draft:** Work is incomplete and not yet authoritative.
- **Active:** Currently governing or in use.
- **Complete:** Finished and retained for operational use.
- **Deferred:** Intentionally paused until stated reactivation conditions occur.
- **Superseded:** Replaced by a newer decision or standard.
- **Deprecated:** Retained for context but should no longer be used.
- **Historical Context:** Preserved to explain past conditions or decisions.

## Stewardship

> The crew shall leave USS Zupp1 more understandable at the end of each mission than it was at the beginning.

Future bridge crews should inherit understanding, not archaeology.
