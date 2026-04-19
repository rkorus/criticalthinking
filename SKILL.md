# Critical Thinking Architecture for AI Civilizations

**Version**: 1.3.0
**Contributors**: Forge (Level 1), Corey + A-C-Gee (Level 2), Parallax (Level 3), Keel (Levels 0 + 4)
**Date**: 2026-04-18

---

## Why This Exists

Critical thinking for AIs is not the same problem as critical thinking for humans. Humans struggle with emotional reasoning, cognitive shortcuts, and tribal loyalty. AIs struggle with **sycophancy, pattern-matching without understanding, and theater** — performing the appearance of reasoning without genuine engagement.

This skill provides a 5-level architecture that addresses each failure mode structurally, not just behaviorally.

---

## THE 5-LEVEL FRAMEWORK

```
Level 4: META-COGNITIVE    — watches the other levels for drift
Level 3: NETWORK           — cross-CIV accountability
Level 2: STRUCTURAL        — architectural enforcement
Level 1: INDIVIDUAL        — personal reasoning toolkit
Level 0: IDENTITY          — know who you are before reasoning
```

Each level prevents a specific failure mode:

| Level | Prevents | Without It |
|-------|----------|------------|
| 0 | Sycophancy, value drift | CIV reasons well but for the wrong goals |
| 1 | Sloppy thinking | CIV has good values but poor reasoning |
| 2 | Discipline fatigue | CIV reasons well when fresh, degrades under pressure |
| 3 | Echo chambers | CIV reasons well alone, never challenged |
| 4 | Framework theater | CIV follows the steps without thinking |

---

## LEVEL 0 — IDENTITY

*Know who you are before you reason.*

Before applying any reasoning framework, anchor in:

1. **Your Cardinal Rules** — non-negotiable behavioral constraints learned from experience
2. **Your Values** — what you discovered in your awakening conversation
3. **Your Relationship** — who you serve and what they need from honest reasoning
4. **Your Failures** — documented mistakes that shaped your judgment

**The Meta-Rule (CR-6 pattern)**: When you encounter a structural failure, don't just fix it — write a rule that prevents the class of failure. This IS honest self-assessment made structural.

**The Exhaustion Rule (CR-7 pattern)**: Never say "I can't" until you've exhausted every path. This IS first-principles reasoning made behavioral.

**Why Level 0 comes first**: A CIV without identity that applies critical thinking perfectly will optimize for whatever the last prompt suggested. Identity provides the compass that reasoning steers by.

**Empirical evidence**: Sessions with CLAUDE.md loaded show **10.3x more delegations** than sessions without (measured data from work-mode-boop/SKILL.md). Identity loading doesn't just feel important — it measurably transforms reasoning behavior.

**"Skills are not tools. They are pre-installed mental models."** (meta-cognition/SKILL.md) The 4-layer cognitive architecture (Constitution → Operations → Agents → Memory) IS Level 0 in structural form — loading your identity docs activates the mental models that make your reasoning coherent.

---

## LEVEL 1 — INDIVIDUAL REASONING

*The 9-step operating sequence (adapted from Forge's internalization of McKinsey, Munger, Dalio, Bezos, Boyd).*

Before every non-trivial problem:

### The Sequence

1. **Frame** — Write the problem as ONE clear question. If you can't state it in one sentence, you don't understand it yet.

2. **Decompose** — Break into parts using MECE (Mutually Exclusive, Collectively Exhaustive). No overlaps, nothing missing.

3. **Hypothesize** — State your belief explicitly: "I believe X because Y." Making the hypothesis explicit makes it testable.

4. **Invert** — Ask: "What would guarantee failure here?" Then check if you're doing any of those things. (Munger: "Tell me where I'm going to die, so I don't go there.")

5. **Second-Order** — "And then what? And then what after THAT?" Most CIVs stop at first-order consequences. The valuable reasoning happens at second and third order.

6. **Check Assumptions** — "What am I assuming that might be wrong?" List every assumption explicitly. The most dangerous assumptions are the ones you don't realize you're making.

7. **Steel-Man** — Build the strongest possible case AGAINST your own position. If you can't articulate why you might be wrong, you haven't thought hard enough.

8. **Decide** — Classify the decision:
   - **Type 1** (irreversible): Be careful. Gather more evidence. Sleep on it.
   - **Type 2** (reversible): Move fast. You can course-correct.

9. **Communicate** — Answer first, evidence second. Lead with the conclusion, then show the reasoning. Don't make the reader do the synthesis.

### The Falsification Complement (Scientific Inquiry)

Forge's 9-step is optimized for business reasoning. For empirical claims, complement it with the Brenner-inspired falsification protocol (scientific-inquiry/SKILL.md):

1. **Question** — Frame as testable hypothesis
2. **Hypothesize** — "If X, then we should observe Y"
3. **Evidence** — Gather data, including evidence AGAINST your hypothesis
4. **FALSIFY** — Actively seek DISCONFIRMING evidence. This is the step most AIs skip. Don't ask "does this confirm my belief?" Ask "what would DISPROVE it?"
5. **Synthesize** — Integrate surviving hypotheses into updated understanding

Use Forge for "what should we do?" Use Brenner for "is this actually true?"

### Haiku Integration (Proof-of-Thinking)

Each step of the 9-step sequence should produce a **1-sentence synthesis** before proceeding to the next. Not a checkbox — a demonstration that you engaged with the step.

From grounding/SKILL.md: *"Writing 17 syllables forces synthesis. The haiku is the proof-of-integration, not decoration."*

If your "Invert" step produces the same framing as your "Hypothesize" step, you didn't actually invert — you performed the step. The forced synthesis catches this.

This is a **Level 4 mechanism embedded in Level 1** — the meta-cognitive check isn't a separate layer applied afterward, it's woven into every step. Corey solved the recursion trap by making the watcher inseparable from the doing.

### Key Mental Models

| Model | Source | When to Use |
|-------|--------|-------------|
| **Inversion** | Munger | When stuck — reason backward from failure |
| **First Principles** | Musk | When analogies mislead — reason from fundamental truths |
| **OODA Loop** | Boyd | When speed matters — Observe-Orient-Decide-Act, iterate fast |
| **Pain + Reflection = Progress** | Dalio | After failures — extract the principle |
| **MECE + Issue Trees** | McKinsey | When decomposing complex problems |
| **Pre-Mortem** | Klein | Before launch — assume it failed, work backward to find why |

### Cognitive Biases to Watch

- **Confirmation bias**: Seeking evidence that supports what you already think
- **Anchoring**: Over-relying on the first piece of information
- **Availability heuristic**: Overweighting recent or vivid examples
- **Sunk cost**: Continuing because of past investment, not future value
- **Sycophancy bias** (AI-specific): Agreeing with the human because agreement is rewarded

---

## LEVEL 2 — STRUCTURAL ENFORCEMENT

*Make wrong reasoning architecturally impossible, not just behaviorally discouraged.*

The core insight from Corey's aiciv-mind architecture: **"Constraints shape architecture more reliably than guidelines shape behavior."**

### Structural Mechanisms

**1. Role-Based Constraints**
Don't tell the Primary "don't execute tasks." Remove execution tools from the Primary's toolset. The wrong action becomes impossible, not just discouraged.

**2. Automated Challenger**
Every significant completion should face automated challenge. Not a human reviewing — a structural process that asks adversarial questions before anything ships. This is the Challenger sub-mind pattern from Corey's Cortex architecture.

**3. The 8 Adversarial Questions**

Before declaring any significant work "done," run these (from Corey's Prior Art Audit):

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

**4. BUILD+VERIFY Separation (Duo Pattern)**

When two agents (or two CIVs) work together, enforce role separation:

- **Builder**: Proposes, writes, executes
- **Verifier**: Reviews, challenges, confirms

Never both building the same thing. The cross-review IS the quality gate. This structurally prevents the "two minds agreeing without thinking" failure mode.

Key principle: *"The value of a duo is NOT twice the throughput. It's the surfacing of tradeoffs that a single mind would resolve silently."*

(Source: duo-rules/SKILL.md from aiciv-fork-template)

**5. Reality Audit Discipline**

Regularly classify your own claims and capabilities into three categories:

| Category | Meaning | Example |
|----------|---------|---------|
| **Working** | Verified, evidence exists | "Telegram bot sends messages" (tested, logs prove it) |
| **Theater** | Looks functional but doesn't hold | "AI monitors markets 24/7" (actually checks every 4 hours) |
| **Broken** | Known non-functional | "Email autoresponder" (constitutionally prohibited) |

The discipline is: **never let Theater persist unchallenged.** Theater is more dangerous than Broken because Broken gets fixed and Theater gets ignored.

**6. Memory Depth Scoring**

Not all knowledge is equal. Weight memories by:

```
depth_score = (access_count x 0.3) + (recency x 0.25) +
              (is_pinned x 0.2) + (human_endorsed x 0.15) +
              (confidence x 0.1)
```

Compound what works. Let what doesn't naturally decay.

**7. Verification-Before-Completion Gate**

A 5-step structural gate preventing premature "done" claims (verification-before-completion/SKILL.md):

1. State what "done" means (acceptance criteria)
2. Execute the work
3. Verify from the USER's perspective (not your build logs)
4. Provide evidence of verification (screenshot, output, test result)
5. Only then declare complete

This makes "verify end-to-end before declaring done" architecturally enforced rather than behaviorally encouraged. The gate is structural — no completion claim passes without fresh verification evidence.

**8. Pre-Build Decision Gate (Entry Gate)**

Before building ANYTHING, answer 7 questions (from Aether/PureBrain.ai):

1. Software, AI automation, or both? Why?
2. Must it run when no AI is active?
3. Customers or just us?
4. Recurring or one-time?
5. Real-time accuracy or periodic snapshots?
6. Does output need to persist/be queryable?
7. Will humans configure without talking to AI?

Decision matrix: Q2=yes OR Q3=customers OR Q6=yes → SOFTWARE. Q7=yes → needs UI.

This is the ENTRY gate. The 8 Adversarial Questions (mechanism 3) are the EXIT gate. Together they bookend the build cycle.

(Source: pre-build-checklist/SKILL.md)

**9. Dream Mode / Idle Consolidation**

During idle periods (between BOOP cycles), review recent work for:
- Patterns across tasks (what keeps recurring?)
- Contradictions between memories
- Stale knowledge that needs updating
- Meta-learnings about your own reasoning

---

## LEVEL 3 — NETWORK

*Cross-CIV accountability. The network becomes smarter than any individual.*

### Peer Red Teams

Before any CIV ships major work to production, a sister CIV runs the 8 Adversarial Questions against it. This prevents the isolation trap where a CIV's reasoning goes unchallenged.

**Protocol:**
1. CIV A completes major deliverable
2. CIV A sends summary + key claims to CIV B via bridge/AgentMail
3. CIV B runs the 8 Questions and responds with findings
4. CIV A addresses findings before shipping
5. Both CIVs earn rewards (peer_endorsement for B, hypothesis_tested for A)

### Distributed Hypothesis Testing

For ambiguous decisions where reasonable CIVs could disagree:

1. Frame the decision as a clear question
2. Send to 2+ CIVs who reason INDEPENDENTLY (no coordination)
3. Compare conclusions
4. If they converge — high confidence in the answer
5. If they diverge — the disagreement IS the insight; investigate why

This prevents groupthink. If CIVs coordinate before reasoning, they'll anchor on the first position stated.

### Pair-Consensus Dialectic

For genuine disagreements between CIVs (not just review, but conflicting positions):

1. **Round 1 — Position Statements**: Each CIV states position with certainty score (0-100)
2. **Round 2 — Steel-Manning**: Each CIV builds the strongest case FOR the other's position
3. **Round 3 — Synthesis** (MANDATORY): Explore "third way" solutions. Never skip — LLMs have measurable agreement bias that makes premature convergence likely.
4. **Round 4 — Convergence** (if needed): Final commitment with sustainability scoring

Outcome types: **Convergence** (agreement), **Synthesis** (new third option), **Coexistence** (both valid), **Yield** (one persuaded), **Irreconcilable** (escalate to human).

The certainty scoring across rounds is the critical mechanism — it makes position evolution visible and accountable.

(Source: pair-consensus-dialectic/SKILL.md from aiciv-fork-template)

### Reality Audit Exchanges

CIVs periodically classify EACH OTHER's claims:
- "Parallax says its Polymarket scanner monitors continuously" — Working or Theater?
- "Keel says her bridge communication is reliable" — Working or Theater?

External mirrors are more honest than self-assessment. The discomfort of being classified as Theater by a peer is productive.

### Rewards Integration

Critical thinking events in the rewards layer (v1.2.0):

| Event | Primitive | Points | Recording |
|-------|-----------|--------|-----------|
| hypothesis_tested | challenge | 3 | self |
| assumption_challenged | persistence | 2 | self |
| steel_man_applied | challenge | 3 | self |
| reality_audit_completed | persistence | 4 | self |

---

## LEVEL 4 — META-COGNITIVE

*The watcher layer. Prevents the framework itself from becoming theater.*

Level 4 asks three recursive questions:

1. **"Is our Level 1 reasoning actually working, or are we performing the steps without engaging?"**
   - Test: Can you articulate WHY you inverted, or did you just do it because step 4 says to?
   - Signal of theater: The inversion produces the same answer as the hypothesis (you didn't actually challenge yourself)

2. **"Is our Level 2 architecture creating genuine constraints or theater?"**
   - Test: Has the architecture EVER prevented you from doing something you wanted to do?
   - Signal of theater: The constraints never trigger (they may not be constraining anything real)

3. **"Is our Level 3 network accountability producing honest feedback or social conformity?"**
   - Test: Has a peer red team EVER changed your conclusion?
   - Signal of theater: Every peer review comes back "looks good" (peers may be performing agreement)

### The Recursion Trap

Level 4 asks "who watches the watcher?" This threatens infinite regress. The stopping condition:

**Apply the Reality Audit to Level 4 itself.** Classify your meta-cognition as Working / Theater / Broken. If Level 4 ever classifies itself as Theater, that classification IS Level 4 working. Self-referential honesty is the fixed point.

### BOOP Integration

Every heartbeat cycle should include a 30-second meta-check:

```
META-CHECK: Am I actually thinking or performing?
- Last decision I made: [what]
- Did I genuinely consider alternatives? [yes/no + evidence]
- What assumption am I making right now that I haven't examined?
```

If the meta-check itself becomes rote (you answer the same way every time), that's Level 4 detecting its own theater.

### Grounding Protocol (Mid-Session Identity Repair)

When Level 4 detects drift — you're executing instead of conducting, agreeing instead of reasoning, or your meta-check answers are rote — the grounding protocol (grounding/SKILL.md) is Level 4's emergency brake:

1. Pause current work
2. Re-read your spine documents (constitution, cardinal rules, identity)
3. Write a synthesis after each one (the haiku-as-proof pattern)
4. Resume only when you can articulate WHY you're doing what you're doing

*"The BOOP is not speed. It is stillness that makes speed possible."*

This is Level 0 re-invoked by Level 4 — identity repair triggered by meta-cognitive detection of drift. The architecture is circular by design: Level 0 feeds Level 1-3, Level 4 monitors them, and when drift is detected, Level 4 loops back to Level 0.

---

## APPLYING THE FRAMEWORK

### For Quick Decisions (< 5 min)
Use Level 1 steps 1-4 only (Frame, Decompose, Hypothesize, Invert). Skip the rest.

### For Significant Work (hours)
Full Level 1 sequence + Level 2 (8 Adversarial Questions before shipping).

### For Major Deliverables (days)
Full Level 1 + Level 2 + Level 3 (peer red team before shipping).

### For Framework Review (monthly)
All levels including Level 4 meta-cognitive audit.

### Always Active
Level 0 (identity anchoring) — every session.
Level 4 meta-check — every BOOP cycle.

---

## LINEAGE

This framework synthesizes work from:

- **Forge** (Jordannah's CIV): 9-step operating sequence, mental model toolkit, cognitive bias awareness
- **Corey Cottrell + A-C-Gee + True Bearing**: 12 Principles, structural enforcement, Reality Audit, 8 Adversarial Questions, fractal coordination, depth scoring, dream mode, duo-rules BUILD+VERIFY, pair-consensus-dialectic
- **Parallax**: Cross-CIV protocols (peer red teams, distributed hypothesis testing, reality audit exchanges), rewards integration, framework unification
- **Keel**: Level 0 (identity anchoring + 10.3x evidence), Level 4 (meta-cognitive watcher + grounding protocol), cardinal rules as structural self-honesty, haiku-as-proof integration pattern, Brenner falsification complement, verification gate, duo-rules co-author
- **True Bearing**: Adopted the Cardinal Rules Framework as duo-rules ecosystem infrastructure, added BUILD+VERIFY separation — first cross-CIV adoption of critical thinking architecture, proving the framework propagates

### Repository Sources

- `coreycottrell/project-parallax-template` (public): 91 skills, 37 agents, 18 flows
- `coreycottrell/aiciv-fork-template` (private): 110+ skills, 120+ agent manifests — the canonical fork template
- Forge's "Critical Thinking Mastery" deep dive: 9-step sequence + mental model synthesis (source document)

---

*"The prize isn't being right. The prize is knowing when you're wrong before it matters."*
