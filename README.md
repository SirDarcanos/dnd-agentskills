# D&D Agent Skills

Reusable Dungeons & Dragons skills for agents, maintained by Nicola Mustone. These packages were moved from [SirDarcanos/agentskills](https://github.com/SirDarcanos/agentskills).

## Skills

| Skill | When to use it |
| --- | --- |
| [D&D Create Monster](dnd-create-monster/) | Design, rebalance, or convert D&D 2024 monsters; Markdown by default, with optional tool formats. |
| [D&D Format Prose](dnd-format-prose/) | Transform supplied prose into read-aloud narration, boxed text, bestiary lore, or adventure lore. |
| [D&D Speak with Dead](dnd-speak-with-dead/) | Rewrite supplied answers in the voice and knowledge limits of a corpse. |

Each package has a `SKILL.md` entry point and a human-facing README. Copy the complete directory so its references, scripts and assets remain available. Create Monster uses Format Prose for lore; install both for that workflow.

## Install

```bash
npx skills add SirDarcanos/dnd-agentskills
```

For a specific skill and agent:

```bash
npx skills add SirDarcanos/dnd-agentskills --skill dnd-create-monster --agent claude-code pi
```

You can also clone the repository and copy or link the packages into your agent's skill discovery path:

```bash
git clone https://github.com/SirDarcanos/dnd-agentskills.git
```

Review a skill's instructions and requirements before enabling it. Previously copied installations do not update automatically. CLI installation examples have not been executed as part of repository setup.

## Contributing and maintenance

Read [CONTRIBUTING.md](CONTRIBUTING.md) for contribution checks and [the workflow](docs/agents/workflow.md) for delivery and release authority. There is no shared build or test command. Create Monster's README documents its Python benchmark and validator.

## License

Repository-authored material is covered by the [MIT License](LICENSE), copyright Nicola Mustone, except where a package or source declares another license. The existing CC BY 4.0 declarations in Create Monster and Format Prose and the [SRD attribution](dnd-format-prose/references/sources.md) are preserved. SRD-derived material, including the bundled creature data, remains subject to its applicable Creative Commons attribution requirements; the MIT license does not relicense it.
