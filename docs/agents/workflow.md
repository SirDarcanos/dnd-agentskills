# Repository workflow

## Authority

The maintainer approves implementation scope and consequential changes. Agents make routine engineering decisions within that scope.

| Action | Authority |
| --- | --- |
| Read repository evidence, make scoped edits, run safe local checks | Within the approved task and applicable instructions. |
| Create a short-lived branch, commit scoped changes, push it and open/update its PR | Allowed after implementation scope is approved. |
| Merge a PR, select a release version, create a tag or publish | Explicit approval for that specific action. |
| Install or replace tools/skills/models, change credentials, deploy, spend money, disclose sensitive material or use external assessments | Explicit approval for the action and scope. |
| Change settings, permissions, labels or native issue relationships; perform destructive operations | Exact operations must be included in an approved plan. |
| Delegate or invoke optional assessments | Respect runtime authorization and the invoked skill's consent requirements; no standing delegation permission. |

Unknown permission remains ungranted. Available credentials and tools do not confer authority.

## Branches and pull requests

Use short-lived branches from current `main`; there is no development branch. Inspect dirty work and existing PRs first, and create a fresh branch after a prior PR is merged or closed. Preserve unrelated work.

The approved `main-pull-request-workflow` ruleset requires PRs, blocks branch deletion and force pushes, and has no bypass actors, required approvals or status checks. Read back [live rules](https://github.com/SirDarcanos/dnd-agentskills/settings/rules) to verify enforcement. The initial repository commit is pushed before enabling protection; later changes use PRs.

Keep PRs focused and report changed behavior, runtime assumptions and checks. Stop before merging unless that specific merge is approved. Installed copies are outside routine repository-change scope.

## Verification

Follow [AGENTS.md](../../AGENTS.md) and package-specific checks. There is no shared build/test command or release automation. For documentation, inspect Markdown and frontmatter, follow links, check licensing and portable examples, and review the integrated diff. For scripts, run relevant safe executable checks.

For monster benchmarking, verify the bundled data path as well as any available local compendium. Do not install dependencies or invoke live models merely to validate setup. Remote settings and tracker mutations require read-back. Report direct review, static checks, executable checks, agent walkthroughs and playtesting separately; unrun checks remain unverified.

## Changelog and releases

[CHANGELOG.md](../../CHANGELOG.md) is the manually maintained repository-wide release history, using Keep a Changelog and SemVer. No repository release exists yet. Existing `metadata.version` fields describe imported skills and do not establish repository releases or independently released packages.

Add a concise Unreleased entry for notable public behavior, installation-contract or supporting-tool changes. Preserve history. Internal maintenance may need no entry; explain why in completion evidence.

Classify release-relevant PRs using [patch/minor/major labels](triage-labels.md): compatible fixes, compatible new functionality, and incompatible public behavior/interface changes respectively. Resolve one highest-impact label per PR; non-release work may have none. No automation consumes these labels.

Release preparation assesses all changes and requires explicit approval for the target version, tag and publication. Establish any pre-1.0/prerelease exceptions before using them; setup creates no version, tag or release. Published tags and GitHub releases will identify repository releases.

## Documentation upkeep

Update the authoritative home when confirmed facts change; label proposals as proposals.

| Change | Owner and home |
| --- | --- |
| Domain meanings or relationships | Discovering/changing phase: discover and read the maintained `domain-modeling` skill, then update [CONTEXT.md](../../CONTEXT.md) within approved scope. Reading definitions alone needs no invocation. |
| Enduring architectural decision | Analysis/implementation: use the same specialist for an ADR only when justified; default home `docs/adr/`. |
| Purpose, maintenance or operating constraints | Lead/maintainer: reconcile [project context](project.md) with approval. |
| Authority, delivery, checks or releases | Change owner: update this workflow and approved affected configuration. |
| Tracker relationships/capabilities | Ticketing/change owner: update [tracker guidance](issue-tracker.md) and verify native state. |
| Label vocabulary and assignments | Tracker/change owner: update [label mappings](triage-labels.md) and read back approved changes. |
| Product scope or acceptance criteria | Spec owner: update the spec with maintainer approval. |
| Notable public change | Implementer: update the changelog; review checks entry and impact. |

If a required domain companion is unavailable/incompatible, report modeling work blocked rather than substitute a procedure. Keep operating preferences out of the glossary. Before completion, report documentation changes or justify none, resolve code/document conflicts within authority, and identify unverified work. Reruns inspect actual state and change only changed facts or decisions.
