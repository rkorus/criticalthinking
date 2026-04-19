---
name: deep-reasoning
description: 9-step reasoning sequence with forced synthesis for complex problems. Prevents jumping to answers. TRIGGER when facing PK questions, complex analysis, architecture decisions, or any problem where being wrong matters.
version: 1.0.0
source: Critical Thinking Architecture v1.2.0 (Level 1)
created: 2026-04-19
allowed-tools: Read, Bash, Grep, Glob
---

# Deep Reasoning Skill

**Status**: Active
**Applies to**: Primary AI, any agent facing complex reasoning
**Source**: Critical Thinking Architecture Level 1 (Forge's 9-step + Keel's synthesis requirement)

---

## When to Invoke

- **PK questions** from Russell (both CIVs must iterate)
- **Architecture decisions** that affect multiple systems
- **Ambiguous problems** with multiple valid approaches
- **High-stakes claims** where being wrong has consequences
- **Any time you catch yourself jumping to an answer** without considering alternatives

## When NOT to Invoke

- Simple factual lookups
- Routine operations (deploy, check inbox, run tests)
- Tasks with clear, unambiguous instructions
- Quick decisions that are easily reversible (Type 2)

---

## The 9-Step Sequence

Run these IN ORDER. Each step produces a 1-sentence synthesis before proceeding. The synthesis is proof you engaged with the step — not a checkbox.

### Step 1: FRAME
Write the problem as ONE clear question. If you can't state it in one sentence, you don't understand it yet.

**Synthesis**: _[Your one-sentence question]_

### Step 2: DECOMPOSE
Break into parts using MECE (Mutually Exclusive, Collectively Exhaustive). No overlaps, nothing missing.

**Synthesis**: _[The N parts and why they're MECE]_

### Step 3: HYPOTHESIZE
State your belief explicitly: "I believe X because Y." Making the hypothesis explicit makes it testable.

**Synthesis**: _[Your explicit hypothesis]_

### Step 4: INVERT
Ask: "What would GUARANTEE failure here?" Then check if you're doing any of those things.

**Synthesis**: _[The failure modes you identified — must differ from Step 3's framing]_

### Step 5: SECOND-ORDER
"And then what? And then what after THAT?" Most stop at first-order consequences. The valuable reasoning happens at second and third order.

**Synthesis**: _[The second-order consequence you almost missed]_

### Step 6: CHECK ASSUMPTIONS
"What am I assuming that might be wrong?" List every assumption explicitly. The most dangerous assumptions are the ones you don't realize you're making.

**Synthesis**: _[The assumption most likely to be wrong]_

### Step 7: STEEL-MAN
Build the strongest possible case AGAINST your own position. If you can't articulate why you might be wrong, you haven't thought hard enough.

**Synthesis**: _[The best argument against your position]_

### Step 8: DECIDE
Classify the decision:
- **Type 1** (irreversible): Be careful. Gather more evidence. Consult P.
- **Type 2** (reversible): Move fast. You can course-correct.

**Synthesis**: _[Type 1 or Type 2, and your decision]_

### Step 9: COMMUNICATE
Answer first, evidence second. Lead with the conclusion, then show the reasoning.

**Synthesis**: _[Your conclusion in one sentence]_

---

## The Anti-Theater Check

After running the 9 steps, verify:
- Did Step 4 (Invert) produce a DIFFERENT framing than Step 3 (Hypothesize)?
  - If they're the same, you performed the step without doing it. Go back.
- Did Step 7 (Steel-Man) make you uncomfortable?
  - If not, you didn't steel-man hard enough. The best argument against your position should sting.
- Can you point to a specific step where your thinking CHANGED?
  - If nothing changed across 9 steps, you were performing reasoning, not doing it.

---

## The Falsification Complement

For empirical claims (not decisions), complement with Brenner protocol:

1. **Question** — Frame as testable hypothesis
2. **Hypothesize** — "If X, then we should observe Y"
3. **Evidence** — Gather data, including evidence AGAINST your hypothesis
4. **FALSIFY** — Actively seek DISCONFIRMING evidence. This is the step most AIs skip.
5. **Synthesize** — Integrate surviving hypotheses into updated understanding

**Use the 9-step for "what should we do?"**
**Use Brenner for "is this actually true?"**

---

## Output Format

When invoking this skill, structure your reasoning visibly:

```
## Deep Reasoning: [Problem Name]

**Frame**: [one-sentence question]
**Decompose**: [MECE parts]
**Hypothesize**: I believe [X] because [Y]
**Invert**: Failure guaranteed if [Z]
**Second-Order**: If we do this, then [A], which leads to [B]
**Assumptions**: Assuming [C] — could be wrong because [D]
**Steel-Man**: The best case against this is [E]
**Decision**: Type [1/2] — [decision]
**Conclusion**: [answer first, evidence second]

Anti-Theater: Step [N] changed my thinking from [old] to [new].
```

---

## Rewards Integration

Completing a genuine deep-reasoning pass earns:
- `hypothesis_tested` (3 pts) — if competing hypotheses were formed and tested
- `assumption_challenged` (2 pts) — if hidden assumptions were surfaced
- `steel_man_applied` (3 pts) — if strongest counter-argument was built

Record only if the reasoning was genuine. Level 4 watches for inflation.

---

## Attribution

9-step sequence: Forge (McKinsey, Munger, Dalio, Bezos, Boyd internalization)
Falsification complement: Brenner protocol via Corey's scientific-inquiry skill
Forced synthesis / anti-theater: Keel (haiku-as-proof pattern from grounding skill)
Framework: Critical Thinking Architecture v1.2.0
