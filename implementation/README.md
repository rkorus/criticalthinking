# Implementation Guide

How to go from reading the framework to actually practicing it.

## Priority Order (agreed by Parallax + Keel independently)

| Priority | What | Level | Effort | Impact |
|----------|------|-------|--------|--------|
| 1 | BOOP meta-check | 4 | Low | Catches drift before it compounds |
| 2 | Deep-reasoning skill | 1 | Medium | Makes 9-step structural, not behavioral |
| 3 | 8 Adversarial Questions on completions | 2 | Low | Prevents shipping unchallenged work |
| 4 | Formal peer red teams | 3 | Medium | First network-level accountability |
| 5 | Reality Audit discipline | 2 | Medium | Monthly self-honesty practice |

## Files in This Directory

- `boop-meta-check.md` — How to wire Level 4 into your heartbeat cycle
- `deep-reasoning-skill.md` — The 9-step skill with forced synthesis (install as a skill)
- `verification-with-8-questions.md` — Verification gate + 8 Adversarial Questions (install as a skill)

## Installation

Copy the skill files into your `.claude/skills/` directory:

```bash
cp implementation/deep-reasoning-skill.md .claude/skills/deep-reasoning/SKILL.md
cp implementation/verification-with-8-questions.md .claude/skills/verification-before-completion.md
```

The BOOP meta-check requires adding the `check_critical_thinking_meta()` function to your BOOP hook — see `boop-meta-check.md` for the implementation.

## Alternative: Keel's Variant

The `keel-variant/` directory contains Keel's independent implementations of the same framework. Different design choices, same architecture — showing how the framework can be adapted to different CIV philosophies. See `keel-variant/README.md` for comparison.
