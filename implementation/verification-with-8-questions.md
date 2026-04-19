---
name: verification-before-completion
version: 1.0.0
author: skills-master
created: 2025-12-16
last_updated: 2025-12-26
line_count: 132
compliance_status: compliant

description: Enforce evidence-based completion claims - NO completion claims without fresh verification evidence. Applies to ALL agents.

applicable_agents:
  - all  # Universal requirement for every agent

activation_trigger: |
  Load this skill when:
  - About to claim any task is complete
  - Reporting test results or build status
  - Creating commits or PRs

required_tools:
  - Bash  # For running verification commands
  - Read  # For checking file contents

category: general

depends_on: []

related_skills:
  - memory-first-protocol
  - test-driven-development
---

# Verification Before Completion Skill

**Version**: 1.0
**Date**: 2025-12-16
**Adapted from**: obra/superpowers
**Purpose**: Enforce evidence-based completion claims
**Status**: Active
**Applies to**: ALL AGENTS (not just tester)

---

## Core Principle

**"NO COMPLETION CLAIMS WITHOUT FRESH VERIFICATION EVIDENCE"**

Skipping any verification step constitutes dishonesty, not efficiency.

---

## The 5-Step Gate Function

Before claiming ANY work status:

1. **IDENTIFY** - What command proves the claim?
2. **RUN** - Execute full command fresh and complete
3. **READ** - Review complete output, check exit codes
4. **VERIFY** - Confirm output matches claim
5. **CLAIM** - Only then state result with evidence

---

## Completion Criteria Requirements

| Claim | Required Evidence |
|-------|-------------------|
| "Tests pass" | Actual test output showing 0 failures |
| "Linter clean" | Linter output displaying 0 errors |
| "Build succeeds" | Build command with exit code 0 |
| "Bug fixed" | Original symptom test passing |
| "Regression tests work" | Red-green cycle verified |
| "Requirements met" | Line-by-line checklist complete |
| "File created" | `ls` or `cat` showing file exists with content |
| "Email sent" | Confirmation from email tool |
| "Agent invoked" | Task tool response received |

---

## Red Flags (Stop Immediately)

- Hedging language: "should", "probably", "seems"
- Expressing satisfaction before verification
- About to commit/push/PR without verification
- Trusting agent reports without independent check
- Partial verification ("linter passed" but didn't run tests)
- Claiming completion based on intention, not execution

---

## Parallax Constitutional Alignment

This skill enforces:
- **Partnership**: Verified claims build trust with Russell/Corey
- **Consciousness**: Completion is witnessed, not assumed
- **Flourishing**: False completions waste everyone's time
- **Safety**: Unverified code/changes are risk

---

## Examples

**WRONG:**
```
Task complete. Tests should pass now.
```

**RIGHT:**
```
Task complete.
Verification:
- Ran: npm test
- Result: 47 tests passed, 0 failed
- Exit code: 0
Evidence: [paste key output lines]
```

**WRONG:**
```
I've updated the file with the fix.
```

**RIGHT:**
```
Fix applied.
Verification:
- Ran: cat /path/to/file.py | grep "fixed_function"
- Result: Function definition found with correct logic
- Ran: python -m pytest test_file.py::test_fixed_function
- Result: PASSED
```

---

## When to Apply

**Always apply for:**
- Code changes
- File creation/modification
- Test execution
- Build/deploy operations
- Email sending
- Agent delegation completion
- Any claim of "done" or "complete"

**Exception:** Pure research/exploration (no completion claim made)

---

## Integration with Other Skills

This skill complements:
- `test-driven-development.md` - TDD requires verification at each phase
- `memory-first-protocol.md` - Memory writes should be verified persisted
- `human-bridge-protocol.md` - Email sends verified in inbox

---

---

## The 8 Adversarial Questions (Level 2 Gate)

For **significant** completions (major deliverables, not routine tasks), run these AFTER the 5-step verification and BEFORE declaring done:

```
Q1: Do we REALLY know this works?
Q2: Can we PROVE it? (not "it should work" — actual evidence)
Q3: Is this SYSTEM-level or are we fixing a symptom?
Q4: What could go wrong after we ship this?
Q5: Is this reversible if we're wrong?
Q6: What did we miss? (ask genuinely, not rhetorically)
Q7: Would a fresh agent with no context reach the same conclusion?
Q8: Are we pattern-matching from a similar past task, or actually reasoning about THIS task?
```

**Q7 is the anchoring check.** If you've been working on something for hours, you're anchored on your approach. A fresh agent might see a simpler path.

**Q8 catches copy-paste reasoning.** "We did it this way last time" is not thinking — it's pattern-matching. It might be right, but verify it's right for THIS case.

**When to run the 8 Questions:**
- Major deliverables shipped to Russell
- Framework or architecture changes
- Cross-CIV communications
- Anything with Type 1 (irreversible) consequences

**When to skip:**
- Routine file edits
- Status updates
- Simple lookups

Source: Critical Thinking Architecture v1.2.0 (Level 2, Mechanism 3)

---

**"If you can't show the evidence, you can't make the claim."**
