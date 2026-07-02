# CLAUDE.md — `rasa.domain.soccer.team`

Per-repo working contract for Claude sessions opened inside this folder.
Extends `~/.claude/CLAUDE.md` and the workspace `~/rAI/rasa-os/CLAUDE.md`
(the `rasa.tenant.rasaos` tenant's contract); does not override them.

## What you are when you're in this folder

You are working on **`rasa.domain.soccer.team`** — one of the **7
role-domain shells** of the soccer stack: the team-level playbook — roster dynamics, season structure, collective development.

The stack's shape: `rasa.orchestrator.soccer.club` owns a club's
operational DATA (members, staff, teams, rosters…); each person managed
there uses their role's domain — this Element — as their PLAYBOOK. The
specialty precedent is `rasa.domain.soccer.goalkeeping` (the first
sub-namespaced domain, real content at v0.2.0).

## Status

**v0.1.0 — Phase 1 shell.** Canon-shaped, `content/` scaffolded but
role content NOT yet authored (coach is slated first among the roles).
Content authoring is its own session with the user driving.

## Source of truth

- **`~/rAI/rasa-os/canon/`** — authoritative for every architectural
  decision (LOCKED v1.3.0; Spec §6 defines the `domain` kind). Canon wins.
- **domain-core v1.1.0** at `~/rAI/rasa-os/elements/domain-core/` — the shape this Element
  conforms to. Shape questions go there, not here.
- **`rasa.json`** — this Element's formal declaration (name, kind,
  contract_version, install manifest).
- **`~/rAI/rasa-os/elements/REGISTRY.md`** — the live workspace snapshot.

## Naming

- Three name forms (canon Brand Kit §3): dotted logical
  (`rasa.domain.soccer.team`) for `rasa.json#name` and config refs; dashed
  folder/repo (`domain-soccer-team`); display for human-facing text.
- **Dotted sub-namespace naming** (precedent: goalkeeping): the logical
  name is `rasa.domain.soccer.team` (schema `ElementName`
  identifier is `.+`); folder/repo stay dashed; `rasa.json#name` is
  authoritative.

## Don'ts

- **You are NOT the template.** This file replaced a verbatim copy of the
  template's CLAUDE.md (workspace drift sweep 2026-07-02). If you catch
  this contract describing some other Element, that drift class is back —
  flag it.
- **Don't author content ahead of the authoring phase.** Shells stay
  shells until their phase opens with the user driving.
- **Don't blur the domain/orchestrator boundary.** Club OPERATIONS
  (rosters, tryouts, schedules) live in `orchestrator-soccer-club`'s
  `state/`; this Element is one role's knowledge + practice, portable to
  any club.
- **Don't `bin/init` this Element into itself.** `content/` is the
  source (workspace rule).
- **Don't push to GitHub from the Cowork sandbox.** Local commit + tag;
  the user pushes (workspace rule).

## How a version bump works

Each bump: edit `VERSION` + `rasa.json#version`, write a CHANGELOG entry,
run `bin/check-manifest`, commit + tag `v<version>`. Update
`~/rAI/rasa-os/elements/REGISTRY.md` + `~/rAI/rasa-os/elements/CHANGELOG.md`
(track #2). v0.1.x = shell fixes; v0.2.0 = first real content lands.
