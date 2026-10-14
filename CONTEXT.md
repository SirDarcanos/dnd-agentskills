# D&D Agent Skills vocabulary

**Skill package:** An independently installable unit of agent instructions, with a `SKILL.md` entry point and any shipped references, scripts or assets. This is the source/distribution unit, not the project an agent modifies when using it.

**Entry point:** The `SKILL.md` that declares a skill's invocation conditions and working instructions. Supporting material is reached through its conditional pointers; an entry point is not the full instruction set by itself.

**Installed skill:** The copy or link exposed through an agent runtime's discovery mechanism. A separately installed copy needs its own update; a symlink reflects changes to its linked directory. A repository merge alone does not refresh separate installed copies.

Game terminology, prose modes and monster-output schemas remain authoritative in the packages that define them. This glossary preserves applicable distribution terms from the source repository rather than redefining D&D rules.
