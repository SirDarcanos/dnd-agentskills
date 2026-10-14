# Label vocabulary

These mappings apply to `SirDarcanos/dnd-agentskills`. Inspect live labels before editing. [Workflow](workflow.md) owns authority and SemVer; [tracker guidance](issue-tracker.md) owns native relationships.

## Types and next action

| Label | Use |
| --- | --- |
| `bug` | Existing behavior fails its contract. |
| `documentation` | Documentation/instruction wording; still assess behavioral impact. |
| `enhancement` | New or improved functionality. |
| `spec` | Product specification and acceptance criteria; apply at creation and read back. |
| `implementation-step` | Bounded work ticket under a spec, not the parent or delivery PR. |
| `needs-triage` | Scope, relevance or routing needs assessment. |
| `needs-info` | A consequential answer or evidence is missing. |
| `ready-for-agent` | Actionable work; inspect native blockers and completion evidence before starting. |
| `ready-for-human` | Next action needs human authority or capability. |
| `wontfix` | Explicitly declined work with rationale. |

`spec` and `implementation-step` are mutually exclusive. Native parentage identifies the owning spec; blockers determine execution order. Assess each ticket's readiness independently rather than copy parent labels. Use descriptive sentence-case issue titles, not workflow-role prefixes.

Update stale next-action labels within approved scope and verify assignments. A readiness label does not approve implementation or override unresolved blockers.

## Release impact

Apply one resolved label to release-relevant PRs, based on actual delivered impact:

| Label | SemVer meaning |
| --- | --- |
| `patch` | Backward-compatible fix. |
| `minor` | Backward-compatible functionality. |
| `major` | Incompatible public behavior or interface change. |

A spec need not predict impact before implementation. Non-release work may use none. Resolve multiple impacts to the highest required bump. Labels have no automation consumers and never authorize publication.

## Approved initial audit

Mirror the source repository's 13-label vocabulary and metadata. Preserve default `bug`, `documentation`, `enhancement` and `wontfix`; rename unused `question` to `needs-info`. Remove unused `duplicate`, `invalid`, `good first issue` and `help wanted`, since duplicates/invalidity can be recorded in issue discussions and contribution-recruitment labels are not used. Add the missing mapped workflow/release labels. There are no historical assignments or issue relationships to migrate.

These are reconciliation decisions, not repeatable deletion commands. Later changes require an inspected, approved delta covering metadata, assignments and automation. Preserve unrelated labels and history.
