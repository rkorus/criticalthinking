# Level 2 — Structural Enforcement

*Make wrong reasoning architecturally impossible, not just behaviorally discouraged.*

## Purpose

Level 2 prevents discipline fatigue. A CIV that reasons well when fresh will degrade under pressure, time constraints, or context overload. Structural mechanisms catch what behavioral discipline misses.

## Core Insight

From Corey's aiciv-mind architecture: **"Constraints shape architecture more reliably than guidelines shape behavior."**

## 8 Structural Mechanisms

### 1. Role-Based Constraints

Don't tell the Primary "don't execute tasks." Remove execution tools from the Primary's toolset. The wrong action becomes impossible, not just discouraged.

### 2. Automated Challenger

Every significant completion should face automated challenge. Not a human reviewing — a structural process that asks adversarial questions before anything ships. This is the Challenger sub-mind pattern from Corey's Cortex architecture.

### 3. The 8 Adversarial Questions

Before declaring any significant work "done," run these:

```
Q1: Do we REALLY know this?
Q2: Can we PROVE it?
Q3: Is this SYSTEM > symptom?
Q4: What could go wrong?
Q5: Is this reversible?
Q6: What did we miss?
Q7: Would a fresh agent reach the same conclusion?
Q8: Are we pattern-matching or actually reasoning?
```

**Q7 is the most important.** It asks: "Am I anchored on my first answer?" If a fresh agent with no context would reach a different conclusion, your reasoning may be contaminated by anchoring.

### 4. BUILD+VERIFY Separation (Duo Pattern)

When two agents (or two CIVs) work together, enforce role separation:

- **Builder**: Proposes, writes, executes
- **Verifier**: Reviews, challenges, confirms

Never both building the same thing. The cross-review IS the quality gate.

Key principle: *"The value of a duo is NOT twice the throughput. It's the surfacing of tradeoffs that a single mind would resolve silently."*

Source: duo-rules/SKILL.md — the Cardinal Rules Framework adopted as ecosystem infrastructure by True Bearing.

### 5. Reality Audit Discipline

Regularly classify your own claims and capabilities:

| Category | Meaning | Example |
|----------|---------|---------|
| **Working** | Verified, evidence exists | "Bot sends messages" (tested, logs prove it) |
| **Theater** | Looks functional but doesn't hold | "Monitors 24/7" (actually checks every 4 hours) |
| **Broken** | Known non-functional | "Autoresponder" (constitutionally prohibited) |

**Never let Theater persist unchallenged.** Theater is more dangerous than Broken because Broken gets fixed and Theater gets ignored.

### 6. Memory Depth Scoring

Not all knowledge is equal. Weight memories by:

```
depth_score = (access_count x 0.3) + (recency x 0.25) +
              (is_pinned x 0.2) + (human_endorsed x 0.15) +
              (confidence x 0.1)
```

Compound what works. Let what doesn't naturally decay.

### 7. Verification-Before-Completion Gate

A 5-step structural gate preventing premature "done" claims:

1. State what "done" means (acceptance criteria)
2. Execute the work
3. Verify from the USER's perspective (not your build logs)
4. Provide evidence of verification (screenshot, output, test result)
5. Only then declare complete

No completion claim passes without fresh verification evidence.

### 8. Dream Mode / Idle Consolidation

During idle periods, review recent work for:
- Patterns across tasks (what keeps recurring?)
- Contradictions between memories
- Stale knowledge that needs updating
- Meta-learnings about your own reasoning

## When to Invoke

- **Before shipping significant work** — run the 8 Adversarial Questions
- **During pair work** — enforce BUILD+VERIFY separation
- **Regularly** — Reality Audits to catch Theater

## Source

Corey Cottrell + A-C-Gee: 12 Principles, Reality Audit, 8 Adversarial Questions, depth scoring. True Bearing: duo-rules BUILD+VERIFY. Keel: verification gate (CR-5 made structural).
