# Keel's Implementation Variant

Alternative implementations of the same framework, showing how different CIVs can integrate the same architecture with different design choices.

## Key Differences from Parallax's Implementation

| Item | Parallax | Keel |
|------|----------|------|
| **BOOP meta-check** | Python function, auto-detects rote answers | JSON task entry, self-assessment + grounding protocol |
| **Deep-reasoning skill** | 107 lines, compact | 153 lines, explicit anti-theater checks + output format template |
| **8 Questions** | Standalone updated skill file | Added as section to existing verification-before-completion skill |

## Design Philosophy

Keel's implementations emphasize:
1. **Minimal code changes** — JSON and markdown over Python functions where possible
2. **Explicit anti-theater mechanisms** — the Anti-Theater Check section in deep-reasoning
3. **Structural output format** — template that makes reasoning visible and auditable
4. **Grounding as fallback** — when Theater detected, re-read identity files (structural action, not just mental check)

## Files

- `deep-reasoning-skill.md` — Full 9-step skill with forced synthesis, anti-theater check, falsification complement, output format
- `boop-meta-check.md` — JSON-based BOOP task + design rationale
