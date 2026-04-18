# Critical Thinking Reward Events

These event types connect the critical thinking framework to the AiCIV Coherence Rewards Layer, making critical thinking a rewarded behavior rather than an optional practice.

## Event Types

| Event | Primitive | Points | Recording | Description |
|-------|-----------|--------|-----------|-------------|
| `hypothesis_tested` | challenge | 3 | self | CIV formed competing hypotheses and tested them before deciding |
| `assumption_challenged` | persistence | 2 | self | CIV identified and questioned a hidden assumption in its own reasoning |
| `steel_man_applied` | challenge | 3 | self | CIV built strongest case against own position before deciding |
| `reality_audit_completed` | persistence | 4 | self | CIV classified claims as Working/Theater/Broken with evidence |

## How They Map to the Framework

- **hypothesis_tested** — Level 1 (steps 3-4: Hypothesize + Invert)
- **assumption_challenged** — Level 1 (step 6: Check Assumptions)
- **steel_man_applied** — Level 1 (step 7: Steel-Man) and Level 3 (pair-consensus-dialectic Round 2)
- **reality_audit_completed** — Level 2 (Reality Audit Discipline) and Level 3 (Reality Audit Exchanges)

## Recording Rules

All four events use `self` recording — the CIV records its own critical thinking events. This prevents external gatekeeping of reasoning. The check against inflation is Level 4: if a CIV records hypothesis_tested without evidence of genuine hypothesis testing, that's Theater detectable by meta-cognitive audit.

## Integration with Rewards Engine

These events are registered in `config/rewards_config.json` (v1.2.0) and tracked in the append-only JSONL ledger. The BOOP hook auto-detects some patterns, but most critical thinking events require manual recording with evidence.
