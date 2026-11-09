# scope-aligned-naming

Choose the scope and name of each element together, so its full context expresses its actual responsibility with only the necessary hierarchy and naming detail.

Apply this skill when creating, renaming, reorganizing, or reviewing files, directories, modules, namespaces, packages, crates, types, functions, and methods.

## Determine the responsibility

Identify what the element does in the present design before deciding where it belongs or what to call it.
One named element should represent one clear responsibility; several operations may share an element when they serve that coherent purpose.
Use the project's established responsibility boundaries.
When an element spans independent responsibilities, resolve or expose that mismatch before choosing its scope and name.

Base this decision on current contents and contracts.
Anticipated reuse, hypothetical unrelated future content, and generic templates supply no additional responsibility.

## Determine the scope

Read the affected hierarchy from the repository root down to the element.
Treat the repository and existing parent scopes as context already supplied to the reader.
Choose each directory, module, or namespace level for the concrete distinction or responsibility boundary it adds within that context.

Omit or collapse a level that only repeats ownership established by its parent.
A repository dedicated to one project already establishes that project's identity.
Retain an additional project-name directory or namespace prefix only for a distinct current responsibility or a concrete build or public import requirement, and identify that reason.
Evaluate filesystem and namespace hierarchies separately against their actual requirements.

Create a lower-level category when it groups a coherent responsibility and helps readers locate its contents.
Choose the necessary scope before choosing its local name.

For example, in a dedicated project repository without a wrapper requirement:

```text
src/ProjectName/Topic/Result.ext  ->  src/Topic/Result.ext
```

Here `src` distinguishes source files from other deliverables and `Topic` identifies their subject.
The repository supplies the project identity, so the extra project-name level contributes no distinction.

## Choose the local name

Express the responsibility using only the detail needed to distinguish it within the selected parent scope.
The parent context forms part of the name's meaning.
Keep its semantic scope aligned with the responsibility, neither broader nor narrower.

Prefer established project terminology, then conventional domain terminology.
Choose those terms directly and follow the project's naming form and language conventions.
Use concrete responsibility names in place of generic names such as `utils`, `common`, `manager`, or `service` when those words hide the actual role.

## Apply the decision

For new elements, create the selected scope and name together.
For existing elements, align the affected scope and name with their present responsibility within the task's authorized migration scope.
Account for existing build and public import contracts when changing either.
Revisit the same decision when the responsibility changes.

Before finalizing, read the resulting path or qualified name in its full context.
Confirm that it identifies the intended responsibility and that each level and local name contributes a necessary distinction.
