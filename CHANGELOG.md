# CHANGELOG — `rasa.domain.soccer.team`

Reverse-chronological. Each entry is a version bump.

---

## 0.1.0 — INITIAL (TODO: date)

### Forked from rasa.domain.core

Scaffolded via `bin/new-element domain soccer-team`. Inherits
canon-required files (§4) + Apache-2.0 LICENSE + bin/init +
bin/check-manifest + seed templates + content/SHAPE.md (which forks
should delete after picking a shape pattern).

### TODO before first ship

- Fill in `rasa.json#description` (currently a placeholder)
- Decide shape pattern: edit `rasa.json#rasa.shape_pattern`
- Populate `content/` per chosen pattern (delete content/SHAPE.md
  after; replace with content/README.md)
- Fill in `rasa.json#capabilities[]`
- Author README.md + CLAUDE.md for this Element specifically
- Run `bin/check-manifest`
- Create `RasaOS/domain-soccer-team` on GitHub
- First commit + tag v0.1.0 + push
- Register in `elements/REGISTRY.md` + `elements/CHANGELOG.md`
