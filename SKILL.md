# scope-aligned-naming

Choose scopes and names that express the actual responsibility of each element.

Apply when creating, renaming, reorganizing, or reviewing files, directories, modules, namespaces, packages, crates, types, functions, and methods.

## Responsibility

Identify the responsibility before choosing its scope or name.
One element represents one coherent responsibility; several operations may belong together when they serve that purpose.
Use the project's responsibility boundaries and expose independent responsibilities concealed within one element.

## Scope and name

Read the surrounding scope from the repository root to the element; that context already contributes to its meaning.
Keep a directory, module, or namespace level only when it adds a concrete distinction within that context or satisfies an identified build or public import requirement.
Choose the local name to convey the responsibility with only the detail needed within the selected scope, neither more broadly nor more narrowly.

## Terminology

Prefer established project terms, then conventional domain terms, and use them directly.
Follow the project's naming form and language conventions.
Use concrete responsibility names where generic labels such as `utils` or `manager` would hide the role.

## Maintenance

Base scope and naming decisions on present responsibilities and concrete requirements rather than anticipated reuse or hypothetical implementations.
When responsibilities change, update the affected scopes and names within the task's authorized migration scope, accounting for existing build and public import contracts.
