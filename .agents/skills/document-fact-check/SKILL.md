---
name: document-fact-check
description: Fact-check technical documentation. Use when the user asks to fact-check, verify, validate accuracy, check sources, correct claims, or add references to documentation.
---

# Document Fact Check

Use this skill when checking or correcting factual claims in documentation.

## Workflow

1. Identify the target document. It may be an uploaded file, a path in the working directory, or content pasted inline. If the source is unclear, ask the user before proceeding.
2. Prefer official documentation, specifications, standards, vendor docs, or other primary sources.
3. For programming languages, frameworks, libraries, tools, APIs, and platforms, prefer their official docs or release notes.
4. Check whether each claim is accurate, overstated, ambiguous, outdated, or missing important context.
5. If a claim cannot be verified from reliable sources, do not present it as fact. Either leave it unchanged and report the uncertainty, or revise it to a clearly qualified statement when that preserves the document's intent.
6. Edit only what is needed to make the document accurate and clear.
7. Add concise reference links when they help future readers verify the claim.
8. Preserve the document's existing tone, structure, and level of detail.
9. After editing, review the changed file and `git status`.
10. Commit or push only when the user explicitly asks.

## Reporting

Use this format:

- Checked: brief list of claims or sections reviewed
- Changed: file-by-file bullet list of edits, with concise before/after intent rather than a full patch
- Sources: official or primary sources used, with links when available
- Uncertainty: any claims left unchanged, qualified, or unresolved because reliable sources were insufficient

Do not paste a full diff unless the user asks for one.
