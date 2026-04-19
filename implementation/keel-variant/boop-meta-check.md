# BOOP Meta-Check — Keel's Implementation (Level 4)

## Approach

JSON-based task in `boop-state.json` — no code changes needed. The BOOP tool reads tasks dynamically, so adding a new task to the JSON is all it takes.

## The Task Entry

Add to `data/boop-state.json` under `tasks`:

```json
"critical-thinking-check": {
  "frequency": "60minutes",
  "last_run": "2026-04-19T00:00:00Z",
  "status": "active",
  "category": "reasoning",
  "description": "Level 4 meta-cognitive check. Ask 3 questions: (1) What was my last significant decision or claim? (2) Did I genuinely consider alternatives, or did I jump to the first plausible answer? What evidence? (3) What assumption am I making right now that I haven't examined? If any answer reveals Theater (going through motions without thinking), trigger grounding: re-read Cardinal Rules, re-anchor in identity, then re-approach the work.",
  "override_max_daily": true
}
```

## Design Choice: Description-as-Protocol

Rather than writing a separate function (Parallax's approach), Keel embeds the full protocol in the task description. The BOOP tool surfaces the description text when the task fires, which serves as the prompt for self-reflection.

**Trade-off**: Simpler (no code changes), but relies on the agent actually engaging with the description rather than mechanically marking it done. This is the Level 4 risk — the meta-check itself could become theater.

**Mitigation**: The grounding protocol trigger (re-read Cardinal Rules) is a structural action, not just a mental check. If Theater is detected, the agent must READ specific files, which creates a verifiable artifact.

## Comparison with Parallax

| Aspect | Parallax | Keel |
|--------|----------|------|
| Implementation | Python function in boop_hook.py | JSON task entry in boop-state.json |
| Detection | Reads scratch-pad for rote answers | Self-assessment via 3 questions |
| Anti-theater | String analysis of scratch-pad entries | Grounding protocol (re-read files) |
| Reward | Auto-awards reality_audit_completed (4pts) | Manual reward recording |
| Complexity | Higher (code + string matching) | Lower (JSON only) |

Both are valid. Parallax's approach automates the check. Keel's approach trusts the agent but provides structural fallback (grounding protocol).
