# scope-aligned-naming

Choose names whose semantic scope matches the actual responsibility of the thing being named.

Apply this skill when creating, renaming, or reviewing:

- files
- directories
- modules
- namespaces
- packages and crates
- types
- functions and methods

## Core rule

One named element should represent one clear responsibility.

Choose a name whose meaning matches that responsibility neither more broadly nor more narrowly.

Treat the surrounding scope as part of the responsibility's name.

Use only the detail needed to distinguish the responsibility within its parent scope.

## Make each hierarchy level meaningful

Treat the repository root and existing parent scopes as established context.
For each level in the affected directory, module, or namespace hierarchy, identify the concrete distinction or responsibility boundary it adds within that context.
Inspect the hierarchy from the repository root down to the changed element, including its upper levels.

Omit or collapse levels that only repeat ownership already established by a parent scope.
In a repository dedicated to one project, the repository already establishes that project's identity. Keep an additional project-name wrapper only when it serves a distinct current responsibility or a concrete build or public import requirement; identify that requirement.
Choose layout from the project's actual contents and contracts. A generic template or hypothetical unrelated future content does not establish a need for another level.

Check directory and namespace hierarchies separately: each needs its own reason for a repeated prefix.
Use the same test before adding lower-level categories; create a category when it groups a coherent responsibility and makes the contents easier to locate.
Apply this check to new layouts and the structure being revised, carrying out migrations within the task's authorized scope.

For example, in a dedicated project repository without a wrapper requirement:

```text
src/ProjectName/Topic/Result.ext  ->  src/Topic/Result.ext
```

Here `src` distinguishes source files from other deliverables and `Topic` identifies their subject. The omitted project-name level only repeats the repository's identity.

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

## Completion check

- Each affected hierarchy level adds an identifiable distinction within its parent context.
- Repeated project names or namespace prefixes have a concrete current justification.
- The result communicates present responsibilities with only the necessary hierarchy and naming detail.
