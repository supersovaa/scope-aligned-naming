# scope-aligned-naming

A lightweight skill for keeping names aligned with the actual responsibility of files, directories, modules, packages, crates, types, functions, and methods.

## Purpose

The skill keeps the semantic scope of a name aligned with the responsibility actually represented by the named element.

It favors concise names within their parent scope, requires each directory and namespace level to add a concrete distinction, and names the design that exists now rather than anticipated future abstractions. The hierarchy check includes upper levels and the context already established by the repository root.

## Contents

- `SKILL.md` — skill definition

## Installation

Place the `scope-aligned-naming` directory in the skill location used by your agent or skill loader.

Review the active skill set when introducing it so overlapping or contradictory naming responsibilities can be resolved at integration time.
