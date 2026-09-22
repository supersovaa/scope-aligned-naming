# scope-aligned-naming

Choose names whose semantic scope matches the actual responsibility of the thing being named.

Apply this skill when creating, renaming, or reviewing:

- files
- directories
- modules
- packages and crates
- types
- functions and methods

## Core rule

One named element should represent one clear responsibility.

Choose a name whose meaning matches that responsibility neither more broadly nor more narrowly.

Treat the surrounding scope as part of the responsibility's name.

Use only the detail needed to distinguish the responsibility within its parent scope.

## Responsibility first

Understand the responsibility before choosing the name.

Treat several operations as one responsibility when they serve the same coherent purpose.

Follow the responsibility boundaries established by the project.

When an element contains multiple independent responsibilities, expose that mismatch instead of hiding it behind a broader name.

## Express the responsibility

Choose names that communicate the actual responsibility.

Prefer concrete responsibility names over generic names such as `utils`, `common`, `manager`, or `service` when those words do not identify the responsibility by themselves.

## Name the present design

Name the responsibility that exists now.

Keep names aligned with current behavior rather than anticipated reuse, future extensions, or hypothetical implementations.

Adjust the name when the responsibility actually changes.

## Follow project language

Among names that accurately describe the responsibility, prefer terminology already established by the project.

When no suitable project term exists, use conventional terminology from the relevant technical domain.

Choose established terminology directly rather than presenting equivalent vocabulary choices.

Follow the project's existing naming form and language conventions.
