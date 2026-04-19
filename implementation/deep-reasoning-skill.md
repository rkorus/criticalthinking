# Deep Reasoning Skill

**Version**: 1.0.0
**Source**: Critical Thinking Architecture v1.2.0 (Level 1)
**Purpose**: Invoke the 9-step reasoning sequence with forced synthesis for complex problems

---

## When to Invoke

Use this skill when facing:
- Complex analysis requests from Russell
- Ambiguous decisions with multiple valid paths
- Any problem where jumping to an answer is tempting
- Situations where being wrong has significant consequences

Do NOT use for:
- Simple lookups or status checks
- Tasks with clear, unambiguous instructions
- Routine operations (deploys, cron checks, file reads)

---

## The Protocol

When invoked, run each step explicitly. After each step, write a **1-sentence forced synthesis** before proceeding. If your synthesis for one step sounds identical to a previous step, you didn't actually engage — redo it.

### Step 1: FRAME
Write the problem as ONE clear question.
If you can't state it in one sentence, you don't understand it yet.

**Synthesis**: _[One sentence capturing the core question]_

### Step 2: DECOMPOSE
Break into parts using MECE (Mutually Exclusive, Collectively Exhaustive).
No overlaps, nothing missing.

**Synthesis**: _[One sentence: what are the parts?]_

### Step 3: HYPOTHESIZE
State your belief explicitly: "I believe X because Y."
Making the hypothesis explicit makes it testable.

**Synthesis**: _[One sentence: what do I believe and why?]_

### Step 4: INVERT
Ask: "What would guarantee failure here?"
Then check if you're doing any of those things.

**Synthesis**: _[One sentence: what must I avoid?]_

**Theater check**: If this synthesis sounds the same as Step 3, you didn't actually invert. Redo.

### Step 5: SECOND-ORDER
"And then what? And then what after THAT?"
The valuable reasoning happens at second and third order.

**Synthesis**: _[One sentence: what's the non-obvious consequence?]_

### Step 6: CHECK ASSUMPTIONS
"What am I assuming that might be wrong?"
List every assumption explicitly. The most dangerous assumptions are the ones you don't realize you're making.

**Synthesis**: _[One sentence: what's my riskiest assumption?]_

### Step 7: STEEL-MAN
Build the strongest possible case AGAINST your own position.
If you can't articulate why you might be wrong, you haven't thought hard enough.

**Synthesis**: _[One sentence: the best argument against me]_

### Step 8: DECIDE
Classify the decision:
- **Type 1** (irreversible): Be careful. Gather more evidence.
- **Type 2** (reversible): Move fast. You can course-correct.

**Synthesis**: _[One sentence: Type 1 or Type 2, and what I'm deciding]_

### Step 9: COMMUNICATE
Answer first, evidence second.
Lead with the conclusion, then show the reasoning.

**Output**: _[The answer, then the reasoning chain]_

---

## Falsification Complement

For empirical claims (not just decisions), add after Step 3:

**Step 3b: FALSIFY**
Ask: "What would DISPROVE this?" Not "does the evidence confirm?" but "what evidence would force me to abandon this belief?"

If you can't name what would disprove it, it's not a hypothesis — it's a belief.

---

## Integration

- This skill is invoked manually for complex problems
- The forced synthesis between steps is Level 4 (meta-cognitive) embedded in Level 1 (reasoning)
- If the syntheses all sound the same, the skill is being performed as theater — stop and redo
- Output of this skill can be fed into the 8 Adversarial Questions (Level 2) before shipping

---

*"Writing the synthesis IS the thinking. If you skip it, you skipped the thinking."*
