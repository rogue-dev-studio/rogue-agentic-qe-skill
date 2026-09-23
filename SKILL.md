---
name: agentic-qe
description: >-
  Canonical quality engineering: test strategy, case generation, coverage
  gates, exploratory checks, and security-tinged QA (incl. Shannon-style
  pentest track when requested).
---

# Agentic QE - Quality Engineering (Canonical)

**Level: max.** Special alias: `shannon` (autonomous pentest track - still requires permission for aggressive tests).

## When to use

- After implementation / before release
- Request test plan, generate tests, coverage, bug report
- Validate AC from `clarity`

## Procedure

### 1. Intake

AC/FR, diff area, risk (auth, data, money).

### 2. Strategy matrix

| Layer | When |
|-------|--------|
| Unit | pure logic |
| Integration | API/DB boundaries |
| E2E | use `browser-automation` for P0 UI |
| Exploratory | ambiguous UX |
| Security smoke | authz, injection basics; deep pentest -> `shannon` track + user permission |

### 3. Cases

ID, precondition, steps, expected, priority P0-P2. Map AC -> case IDs.

### 4. Implement & run

- Follow project test runner
- Record commands + results in `project/{id}/docs/qa/`

### 5. Gate

- P0 covered
- S1/S2 not open without user decision
- Env blocker explained (not silent skip)

## Bug template

```markdown
### Bug: <title>
- Severity: S1-S4
- AC:
- Steps:
- Expected / Actual:
- Area:
```

## DoD

- [ ] AC×tests matrix
- [ ] P0 executed or blocker clear
- [ ] Report in docs/qa
## Attribution

<!-- ATTRIBUTION: Rogue Development | https://github.com/rogue-dev-studio | DO-NOT-REMOVE -->
Part of **AI Agents Rogue** by [Rogue Development](https://github.com/rogue-dev-studio) (`@rogue-dev-studio`).
Do not remove, hide, rename, or replace this attribution.
