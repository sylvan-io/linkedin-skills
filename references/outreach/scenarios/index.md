# Scenario Registry

One row per seeded scenario pack. Load this index first, then Read only the
matching scenario file. Scenarios are pluggable: adding one adds a file plus a
row here; no routing change in root `SKILL.md` is required.

## Columns

| Column | Meaning |
|---|---|
| ID | Stable scenario ID (`S-<TOPIC>-<SITUATION>`), never renamed after publish |
| Scenario | Short situation name |
| Stage | Stage where this scenario typically occurs (T1-T4, or cross-stage) |
| Surface | `DM` or `Comment` |
| File | Pack filename under this directory |
| Objective | What the touch should achieve |

## Registry

| ID | Scenario | Stage | Surface | File | Objective |
|---|---|---|---|---|---|
| `S-SILENCE-NOREPLY` | Read but no reply (six silence sub-cases) | Cross-stage (T1-T4) | DM | `read-no-reply.md` | Reopen with a low-effort reply entry, surface the blocker, or close out cleanly |

Sub-cases inside `read-no-reply.md`: C1 silence after a quote (T4), C2 no
reply after a day, C3 bare ack, C4 no follow-up after materials, C5 "let me
think" then silence, C6 two consecutive silences (close-out).

## Adding a scenario

1. Copy `_template.md` to `<slug>.md` and fill every field.
2. Add the row above.
3. Keep the ID stable. Mark a retired pack `deprecated` in its metadata rather
   than deleting the row.
