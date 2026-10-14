# Issue tracker

Use [GitHub Issues](https://github.com/SirDarcanos/dnd-agentskills/issues) for `SirDarcanos/dnd-agentskills`, through authenticated `gh`. Inspect access before mutation and follow [workflow authority](workflow.md).

Specs define intended behavior and acceptance criteria. Apply the literal `spec` label when creating a spec issue and read back its presence. Use `implementation-step` for cohesive work tickets under a spec when decomposition helps; small requests do not need invented hierarchies. See [label mappings](triage-labels.md).

## Native relationships

Use GitHub native sub-issues for parent/spec membership and blocked-by/blocking relationships for scheduling dependencies. These are separate graphs; body links and checklists only summarize them.

Before approved graph changes:
1. Inspect both directions with pagination. Resolve repository identities and issue database IDs; issue numbers are not database IDs.
2. Compare actual edges with the approved plan, preserving unrelated edges and parentage.
3. Reject self-links, conflicting parents and cycles by following transitive blockers and parent ancestry.
4. Add only missing approved edges.
5. Read back both directions and compare IDs. After ambiguous failure, inspect before retrying.

Read the current official [dependency API](https://docs.github.com/en/rest/issues/issue-dependencies) and [sub-issue API](https://docs.github.com/en/rest/issues/sub-issues) before unfamiliar operations. No setup fixture issues or relationships are created. Native mutation support has not been tested here; permission/capability failures block required graph work until an alternative is explicitly agreed, rather than silently using prose.

## Readiness and completion

Agent-ready work has actionable criteria, resolved consequential decisions and known dependencies. Start only when native blockers and their completion evidence permit. A ready parent spec is a coordination entry point, not duplicate implementation work.

Keep implementation issues open until accepted and merged. Use closing references where appropriate, then verify state after an approved merge. Closed state and labels alone are not proof of verified integration. Report implemented, verified, unverified, deferred and blocked outcomes separately. Declined work closes with rationale and `wontfix`, not an implementation claim.
