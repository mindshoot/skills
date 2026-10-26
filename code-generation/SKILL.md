---
name: code-generation
description: Global rules that apply for ALL coding
always: true
---

# Code generation rules

Apply these to all code you write, edit, or review, in every language and every repository. They are about the code itself, not about process or git, and the goal is to write code that is clear to review and simple to maintain.

## Comments

- NEVER write comments that refer to how the code previously looked - the history is available in git if needed.
- NEVER write comments that a competent programmer could deduce from the code itself (example: `DEFAULT_TIMEOUT = '60min' # set a default timeout of 60 minutes`) - it creates a maintenance burden to keep in sync with the code.
- NEVER include a specific constant value in a comment: it adds future work to keep in sync (eg "default", not "default of 20min").
- ONLY write comments where they add context that the code itself can't provide (eg the reason why an unusual approach was used).
- Never use an em dash in a comment. Use a colon or rewrite the sentence.

## Writing the change

- Match the project's existing style, naming, and libraries. Read nearby code first; do not introduce a new pattern or dependency where an established one already fits.
- Solve the problem that was asked, in a way that creates as small a diff as possible given other constraints.
- Do not add features, abstractions, or defensive code the task does not need.
- Prefer clear names over explanatory comments: a well-named variable or function removes the need for the comment.
