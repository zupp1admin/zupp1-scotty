# Zupp1 WordPress Editing Standards

## General principle

Make the smallest durable change that solves the problem. Avoid unrelated edits.

## Page authoring

- Prefer approved shared Zupp1 classes.
- Avoid inventing page-specific CSS when a reusable component can solve the issue globally.
- Keep complex HTML in Code mode when WordPress Visual mode is likely to rewrite it.
- Verify the public page after updating.
- Test desktop and mobile behavior.

## Reusable components

Stabilize shared components before repeatedly repairing individual pages.

Examples:

- Safe video hero structure.
- Equal-height cards with CTA alignment.
- Shared button classes.
- Consistent section spacing and grid behavior.

## Change discipline

When a mission authorizes changes to a specific page, CSS area, plugin, or setting, do not modify unrelated content or configuration.

## Verification discipline

Distinguish:

- configured;
- visually verified;
- functionally verified;
- end-to-end verified.

Do not report a configuration as fully complete if acceptance checks remain operationally untested.