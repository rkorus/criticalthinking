# BOOP Meta-Check Implementation (Level 4)

**Purpose**: Wire critical thinking reflection into every heartbeat cycle.

## What It Does

The BOOP hook now includes a `check_critical_thinking_meta()` scanner that:

1. Reads the scratch-pad for `META-CHECK` markers
2. Validates the content is **genuine** (not just template placeholders)
3. Awards `reality_audit_completed` (4pts) when genuine reflection is detected

## Genuineness Check

The scanner rejects rote meta-checks by looking for:
- Template placeholder text (`[what]`) → rejected
- Content length < 100 characters → rejected (too thin to be genuine)
- De-duplication: same scratch-pad modification time won't count twice

## What a Genuine Meta-Check Looks Like

In the scratch-pad during every BOOP cycle:

```
**META-CHECK**: Am I actually thinking or performing?
- Last decision I made: [specific decision, not placeholder]
- Did I genuinely consider alternatives? [yes/no + specific evidence]
- What assumption am I making right now that I haven't examined? [specific assumption]
```

## Theater Detection

If the meta-check answers are rote across multiple cycles (same phrasing, same answers), that's Level 4 detecting its own theater. The solution: stop, re-read spine documents (grounding protocol), then resume.

## Integration

- Added to `tools/rewards/boop_hook.py` as `check_critical_thinking_meta()`
- Fires alongside existing checks (uptime, session, memory, skills, tools, handoffs)
- Awards under `reality_audit_completed` event type (4pts, persistence primitive)

## Source Code

See `tools/rewards/boop_hook.py` — the `check_critical_thinking_meta()` function.
