# Knowledge Map

A personal [Obsidian](https://obsidian.md) vault: a connected map of physics (and the math behind it), built from derivations worked out by hand. The goal is understanding, not collecting. Notes link to each other, so the structure of the subject, and the structure shared *between* subjects, becomes visible.

## Structure

One folder per course or topic, numbered in learning order:

| Folder | Topic |
|---|---|
| `00 - Index` | Roadmap, learning method, isomorphism log, monthly audit |
| `01 - Mechanics` | Classical mechanics |
| `02 - Electromagnetism` | Electromagnetism |
| `03 - Analytical Mechanics` | Lagrangian / Hamiltonian mechanics |
| `04 - EM Fields and Waves` | Fields and waves |
| `05 - Optics` | Optics |
| `06 - Quantum Mechanics 1` | Quantum mechanics |
| `07 - Quantum Mechanics 2` | Quantum mechanics, continued |
| `08 - Quantum Optics` | Quantum optics |
| `09 - Nanophotonics` | Nanophotonics |
| `10 - Quantum Information` | Quantum information |
| `11 - Linear Algebra` | Complex numbers, matrices, vector spaces, inner products |

Start with `00 - Index/Physics Roadmap.md` for the overall plan and `00 - Index/How to Learn.md` for the method.

## Note types

Every note is one of three kinds, tagged as `[<folder-name>, <type>]`:

- **Concept**: one self-contained idea. Core idea, key equation, supporting formulas, derivation outline, physical intuition, open questions.
- **Derivation**: the full step-by-step proof of a result a concept note only summarizes.
- **System**: a device or framework built from several concepts (a resonator, an interferometer). It links to its prerequisite concepts instead of re-deriving them.

Extra tags: `technique` for methods reused across courses, `device` for physical hardware.

## Conventions

- Links are relative Markdown links, not `[[wikilinks]]`, with spaces encoded as `%20`.
- Filenames are Title Case, four words at most.
- Equations are LaTeX (`$...$` inline, `$$...$$` display). In derivations, each step's main equation sits on its own display line.
- **Physical Intuition** is written only after explaining the idea out loud, never generated from the derivation.
- Notes that share mathematical structure across courses are recorded in `00 - Index/Isomorphism Log.md`.

## Using it

Open the folder as a vault in Obsidian. Shared app settings are tracked in `.obsidian/`; per-device workspace state is git-ignored.

## Status

Work in progress. Coverage is uneven: Quantum Optics, Nanophotonics and Quantum Information are the most developed.
