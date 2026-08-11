# Documentation Retention Protocol

**Status:** Permanent operating norm  
**Effective:** 2026-08-11

This protocol implements **Standing Order SO-004 — Knowledge Preservation and Information Lifecycle Policy**. If the two documents conflict, SO-004 governs.

## Purpose

Zupp1 documentation is an institutional asset. Completed reports, research notes, strategic assessments, operating standards, decision frameworks, mission records, and other durable work products must remain retrievable after the immediate conversation or task ends.

## Canonical workflow

Every durable Zupp1 document created by an officer or automated system must follow this retention chain:

1. **Create:** Produce the working document with an accurate title, date, mission or subject identifier when applicable, and explicit evidence limitations.
2. **Archive in GitHub:** Commit the document to the appropriate directory in the canonical `zupp1admin/zupp1-scotty` repository.
3. **Preserve provenance:** Use a descriptive commit message. Retain source links, status labels, intelligence gaps, and validation limitations inside the document.
4. **Log in Slack:** Post a concise record in `#ro-documents` identifying the document, its purpose, repository location, status, and any material intelligence gaps.
5. **Update rather than duplicate:** When a document evolves, update its canonical path whenever practical. Use Git history as the version record.

## Repository routing

- **Research:** Intelligence reports, strategic assessments, research notes, measurement frameworks, mission queues, and research archives.
- **Operations-Manual:** Permanent operating rules, protocols, roles, and decision doctrine.
- **Engineering:** Technical implementation standards and engineering documentation.
- **Engineering mission reports:** XO audits, intervention registers, runtime reviews, verification evidence, rollback context, and cross-platform engineering mission closures belong in `Engineering/Mission-Reports/YYYY/` and must be linked from its index.
- **Customer-Experience:** Customer-service architecture, policies, and support doctrine.
- **Bridge-Logs:** Durable operational records from Ro, Spock, and Scotty.
- **Captain-Logs:** Major decisions, milestones, and founding history.
- **Philosophy:** Enduring cultural principles and company identity.
- **Poetry:** Authorized literary work retained as part of Zupp1's cultural archive.

Specialized project repositories may remain the canonical location for their own code and domain documentation. Their durable strategic context should still be indexed or summarized in the institutional repository when it materially affects Zupp1.

## Slack ledger standard

Each archival message should state:

- document title;
- status, such as complete, provisional, superseded, or validation deferred;
- one-sentence purpose or principal finding;
- GitHub link or commit;
- material intelligence gaps or operational limitations;
- whether bridge attention is required.

Slack is the activity ledger. GitHub is the canonical institutional archive.

## Exclusions

Do not commit:

- passwords, tokens, API keys, cookies, or credentials;
- private customer data or unnecessary personal information;
- raw exports containing sensitive operational data;
- temporary build artifacts, caches, or duplicate generated files;
- unverified claims presented as facts.

When source material is sensitive, archive a sanitized summary and document the restriction.

## Responsibility

This protocol applies by default and does not require repeated authorization. The officer creating or materially revising a document is responsible for completing the GitHub archive and Slack ledger steps before reporting the work as finished.

Commander One maintains the engineering-document route and its mission-report index. New durable engineering reports must be archived as part of mission closure unless blocked by unavailable access or unresolved confidentiality review.

If an archival system is unavailable, preserve the document locally, label the retention step as pending, report the blockage, and complete the archive when access returns.
