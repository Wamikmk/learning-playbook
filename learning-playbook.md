# The Learning Playbook

*A reusable protocol for learning any subject from zero to fluency.*

---

## Why this exists

You can read a thousand books on learning and still not know what to *do* Monday morning. This playbook closes that gap. It takes the principles you already accept.  Automaticity before understanding, mastery before advancement, prerequisites over confusion and turns them into a step-by-step operating procedure you can run on any subject: a new mathematical topic, a programming language, a research area, a manual skill.

Use it the way a pilot uses a checklist: not because you can't fly without it, but because running the checklist every time is how you avoid the mistakes that cost you.

---

## Part I — The Seven Core Principles

Read these once. Return to them whenever you're tempted to violate one.

### 1. Automaticity before understanding

Your working memory holds about four items at once. If three are burned on sub-skills you haven't automated, you have one slot left for actual learning. This is why understanding a concept while reading the textbook doesn't translate into solving problems: the moment you have to *use* the concept, your working memory is full of bookkeeping.

*Implication:* drill sub-skills to the point where they feel boring before trying to understand the higher-level concept.

### 2. Mastery before advancement

You do not move up a level until the level below is automatic. "I get it mostly" is not a pass. The criterion is: on a blank page, with no notes, can you produce the thing in a time budget appropriate to its difficulty? If not, you're not ready.

*Implication:* your gating test is always a blank-page reproduction, never a nod of recognition.

### 3. Confusion is diagnostic, not a verdict

When you're confused, the cause is almost never "this topic is hard" or "I'm not smart enough." The cause is almost always a specific prior skill that isn't fluent. Confusion is the signal that tells you *where* that skill is.

*Implication:* when confused, stop. Ask *"what specific prior thing am I not fluent in right now?"* Drop down, drill it, return.

### 4. Active retrieval beats passive exposure

Re-reading, watching lectures, and highlighting feel productive because familiarity rises. But familiarity is not retrievability, and only retrievability transfers. The skill you want is the ability to *generate* the content on demand, not to *recognize* it when you see it.

*Implication:* every session ends with a blank-page test of what you covered. No notes, no hints.

### 5. FIRE — one exercise, many skills

Fractional Implicit Repetition (Skycak's term). A single well-chosen problem can exercise a dozen sub-skills simultaneously and give you practice credit for all of them. This is the multiplier that makes learning efficient. Implementing linear regression from scratch is not one exercise — it's gradient derivation, matrix operations, loss functions, optimization, and numerical stability, all in one.

*Implication:* prefer fewer, harder, integrative problems over many small isolated drills — *once* the isolated sub-skills are fluent.

### 6. Interleave, don't block

Practicing the same sub-skill for a week feels efficient — it's not. Mixing different sub-skills within a session feels harder and slower — but retention and transfer are dramatically better. The discomfort is a feature.

*Implication:* within a session, rotate between 2–3 sub-skills. Within a week, cover multiple graph nodes.

### 7. Metacognition closes the loop

Learning you can't *describe* is brittle. The weekly review — asking what clicked, what didn't, what's next — is the thing that converts practice into durable ability. Skip it and you'll regress to the "I've been studying for weeks with nothing to show" state.

*Implication:* 30 minutes every week, four questions (Part VI), non-negotiable.

---

## Part II — Setting Up a Learning Project

Run these five steps *before* your first practice session. Most people skip setup and wonder why they plateau. Setup typically takes 2–3 hours and saves weeks of misdirected effort.

### Step 1: Define the target with a blank-page test

Write a single sentence describing what you want to be able to do, in the form of a thing you can test on a blank page.

- Bad: "Understand calculus."
- Good: "On a blank page, compute ∂L/∂W for a 2-layer MLP with MSE loss, in under 10 minutes, without looking anything up."

- Bad: "Learn Rust."
- Good: "Build a small TCP server that handles concurrent connections using only Rust's standard library and the Tokio runtime, explaining ownership and borrow-checker decisions as I go."

If you can't write the target as a blank-page test, your target is too vague and you don't yet know what you want. Keep rewriting until you can.

### Step 2: Classify the domain

The playbook applies to all subjects, but emphasis shifts by domain type.

- **Hierarchical** (math, physics, formal logic): prerequisite graph is strict; mastery gates are absolute; FIRE works beautifully.
- **Skill-based** (programming, writing, design): partially hierarchical; lateral exploration matters; implementation projects are the main FIRE vehicle.
- **Fact-dense** (biology, history, languages): prerequisite graph is looser; spaced repetition becomes the dominant tool; retrieval practice is still king.

Write down which one your subject is. This decides how strictly you apply the later steps.

### Step 3: Audit your real available time

Be honest, not aspirational. Across a typical week, how many 30-minute blocks of *actually focused* practice can you protect? Not theoretical free time. Not "if I wake up at 5am." The real number.

Multiply by weeks to get the project budget. If your target requires more than the budget, either shrink the target or extend the timeline. Don't start with a budget you know will fail — it collapses to zero on week three and takes your confidence with it.

### Step 4: Build the prerequisite graph

This is the central exercise of setup. You are building a directed acyclic graph where:

- Nodes are *atomic* skills you can test on a blank page
- Edges point from prerequisite to dependent

"Understand backpropagation" is not atomic. "Compute ∂L/∂w for a single linear layer with MSE loss on one training example" is atomic.

**Procedure:**

1. Write the target node at the top.
2. Ask: "what do I need to be able to do *before* I can do this?" List each prerequisite as a node below, with an edge up to the target.
3. Recurse on each new node. Stop recursing when you hit a node you're *already fluent in* on a blank page.
4. Cross-check: can you state each node as a blank-page test? If not, refine it.

The graph usually ends up with 15–40 nodes for a single 3–6 week project. If you have 100+, your target is too broad — split it into multiple projects.

*How to use Claude here:* paste your target and initial graph, and ask Claude to find *prerequisites you missed*. LLMs are genuinely excellent at this one thing. What they're bad at is replacing your thinking — so use Claude for gap discovery, not for building the graph *for* you.

### Step 5: Diagnose your frontier

For each node, rate yourself on three tiers:

- **Fluent**: I can produce this on a blank page, quickly, without notes. I've done it recently.
- **Wobbly**: I recognize it and can sometimes do it, but slowly or with errors.
- **Nonexistent**: I don't know what this is or how to do it.

Your **frontier** is the deepest layer of fluent nodes. Everything between your frontier and the target is what you have to close.

Honesty here is everything. "Wobbly" is not "fluent." Rating yourself fluent when you're wobbly is how you waste months. The blank-page test settles it.

---

## Part III — The Daily Engine

A single 30-minute practice session. You run this 4–6 times per week.

### Session structure (30 min)

- **Minute 0–2 — Retrieval warm-up.** On a blank page, reproduce the key result from yesterday's session without looking. Check against notes after.
- **Minute 2–25 — Targeted practice.** Work on your current node(s). Mix 2–3 sub-skills; don't block on one.
- **Minute 25–30 — Blank-page closing test.** Pick one thing from today's session. Close the notebook. Reproduce it from scratch.

If you can't pass the closing test, you did not make progress today. That's acceptable information — you try again tomorrow. What is *not* acceptable is deciding you made progress because you "felt like you understood it."

### The retrieval protocol

Whenever you're tempted to re-read or re-watch:

1. Stop.
2. Close the material.
3. Try to produce the content from memory.
4. *Then* check against the material and fix gaps.

The struggle of failed retrieval is what produces learning. If it feels easy, you're probably not practicing retrieval — you're practicing recognition.

### The problem-solving discipline

For math and programming specifically: when attempting a problem, force yourself through these phases before peeking at a solution.

1. **Restate** the problem in your own words.
2. **Identify** which node(s) of your graph this is exercising.
3. **Plan** the approach before writing anything — what tool, what sequence.
4. **Execute** the plan.
5. **Verify** — does the answer type-check, unit-check, pass a sanity case?
6. **Reflect** — what would I do differently? What was the crux?

Most people collapse these into "look at problem, start writing, hope." The six-phase discipline is the difference between practice that builds and practice that spins.

### Daily log (four lines, not a journal)

```
Date:
Target node(s) today:
What I can now do on a blank page:
Where I got stuck (= which prerequisite to check tomorrow):
```

---

## Part IV — The Feedback Loop

How to notice you're off-track and correct course.

### When you're confused: the drop-down protocol

1. Name the confusion in a sentence. *"I don't see why the gradient of softmax gives that form."*
2. Ask: *"to understand this, what would I need to already know fluently?"* List 2–3 candidate prerequisites.
3. Pick the one you're least fluent in. Drop to that node.
4. Work until you pass its blank-page test.
5. Return to the original problem. 80% of the time it's now clear. If not, there was another prerequisite — repeat.

### When you're bored: re-diagnose

Boredom almost always means the current node is below your real frontier. You're reviewing, not learning. Move up a level.

Occasionally boredom means the node is too small and you need to combine it with others into a FIRE exercise. Either way, boredom is a signal to *change what you're doing*, not to push through.

### When you're overwhelmed: the scope is wrong

If sessions feel bad three days running and you can't point to a specific missing prerequisite, your current node is too large — it's actually three nodes pretending to be one. Break it apart in the graph.

### How to use Claude (or any LLM)

LLMs are good at:
- Finding prerequisites you missed when building the graph.
- Diagnosing *where* your confusion points to when you describe it.
- Generating practice problems at a specified difficulty.
- Checking a derivation you've done step-by-step.

LLMs are dangerous at:
- Doing your thinking for you. Every time Claude hands you a derivation you didn't struggle for, you lose the practice opportunity.
- Giving you the feeling of understanding without the ability.

**Rule:** use Claude to sharpen questions, not to answer them. If you're about to ask Claude to *solve* something, stop. Ask it instead to tell you which prerequisite you're missing.

---

## Part V — Integration: the FIRE Exercise

You don't actually know a subject until you've built something with it that stresses many of its sub-skills at once. The FIRE exercise is that test.

### What it is

A single problem or project that:

- Exercises at least 60% of the nodes in your prerequisite graph.
- Cannot be solved by rote — it requires synthesis.
- Produces an artifact you can show someone (a proof, a working program, a written derivation).

### How to design one

Near the end of your project timeline, look at your graph and ask: *"What is the smallest thing I could build or prove that would force me to use most of this?"*

Examples by domain:

- **Calculus for ML:** derive and implement gradient descent for linear regression from scratch, no library help.
- **Rust fundamentals:** build a small thread-safe key-value store.
- **Probability for ML:** derive and implement EM for a Gaussian mixture on synthetic data.
- **Linear algebra:** derive SVD from first principles and implement power iteration.

### The "I can now..." statement

When you finish the FIRE exercise, write a one-paragraph statement describing your new ability in concrete, testable terms. If you can't write it concretely, you're not actually done — you have more closing to do.

---

## Part VI — The Weekly Review

30 minutes, same time every week. Four questions. Write the answers down, not in your head.

1. **What did I make automatic this week?** List the nodes that moved from wobbly to fluent. If the list is empty, something is wrong with the daily engine.
2. **Where did I get stuck, and what prerequisite was missing?** Each stuck point should resolve to a specific node in the graph. If "I'm just bad at this" appears, you haven't diagnosed yet.
3. **What's the next atomic skill to target?** Specify the node and the blank-page test. This is next week's plan.
4. **Is my path still right, or do I need to re-plan?** Sometimes new nodes appear that weren't in the original graph. Add them. Sometimes the target itself needs revising. Do it.

---

## Part VII — Seven Failure Modes

Check yourself against these in the weekly review.

1. **Passive study masquerading as practice.** Re-reading, re-watching, highlighting. Symptom: you feel productive but fail blank-page tests.
2. **Skipping setup.** Starting practice without the graph. Symptom: you don't know what you're working on today, so you drift to the most interesting surface topic.
3. **Rating yourself fluent when you're wobbly.** Symptom: the same confusions keep reappearing at higher levels. Fix: use blank-page tests, not self-assessment.
4. **Blocking instead of interleaving.** One sub-skill all week. Symptom: you feel strong in week 1, lose it all in week 3.
5. **Avoiding the FIRE exercise because it feels hard.** Symptom: you have "learned" the subject for months but can't produce anything.
6. **Using Claude as a crutch.** Symptom: you can follow any explanation but can't generate one.
7. **Skipping the weekly review.** Symptom: you can't tell anyone what you've actually learned, and you quietly start doubting the whole process.

---

## Part VIII — Worked Example: Calculus for ML in 3 Weeks

Running the full protocol on a concrete subject.

### Setup

**Target (blank-page test):** Compute ∂L/∂W for a 2-layer MLP with MSE loss, in under 10 minutes, on paper, with a correct derivation showing every chain-rule step.

**Domain type:** Hierarchical. Strict gating, graph-driven.

**Budget:** 6 sessions × 30 min × 3 weeks = 9 hours of focused practice.

**Prerequisite graph (abbreviated):**

```
Target: ∂L/∂W for 2-layer MLP
├── Chain rule for composite functions
│   ├── Derivatives of elementary functions (x^n, e^x, sin, log)
│   └── Composition rule f(g(x))
├── Partial derivatives
│   ├── Treating other variables as constants
│   └── Notation discipline (∂ vs d)
├── Gradient as vector of partials
├── Vector-by-vector derivatives (Jacobian)
└── Matrix calculus rules
    ├── ∂(Wx)/∂W
    └── ∂(Wx)/∂x
```

**Frontier diagnosis:** Fluent on elementary derivatives. Wobbly on partials. Nonexistent on matrix calculus.

### Week 1 — Close the calculus gaps

Target nodes: chain rule, partial derivatives. 6 sessions interleaving both. End-of-week mini-FIRE: on a blank page, derive ∂/∂x of three composite expressions of varying difficulty.

### Week 2 — Build up to matrix calculus

Target nodes: gradient vector, Jacobian, basic matrix calculus rules. Sessions alternate between scalar-input and vector-input examples. End-of-week mini-FIRE: derive ∂(Wx)/∂W and ∂(xᵀAx)/∂x from scratch.

### Week 3 — Integration

Target: the full target. Sessions build the 2-layer MLP loss derivation piece by piece. Final FIRE exercise: implement linear regression from scratch in NumPy using the gradient you derived; confirm it converges on synthetic data.

### Weekly reviews

End of week 1: confirm partial derivatives are fluent. If not, push week 2 back one week. This is non-negotiable — skipping the mastery gate is how the whole thing collapses.

---

## Part IX — Templates (copy-paste)

### Subject Setup

```
SUBJECT:
TARGET (blank-page test):
DOMAIN TYPE (hierarchical / skill / fact-dense):
BUDGET (sessions/week × weeks):
PREREQUISITE GRAPH: [attach]
FRONTIER DIAGNOSIS:
  Fluent nodes:
  Wobbly nodes:
  Nonexistent nodes:
FIRE EXERCISE (end-state):
```

### Daily Log

```
Date:
Target node(s) today:
What I can now do on a blank page:
Where I got stuck (= which prerequisite to check tomorrow):
```

### Weekly Review

```
Week of:
Nodes that moved to fluent:
Where I got stuck and which prerequisite was missing:
Next atomic skill to target (with blank-page test):
Path adjustments needed:
```

### FIRE Exercise Spec

```
FIRE EXERCISE for [subject]:
Problem statement:
Nodes exercised:
Success criterion (blank-page):
Artifact produced:
```

---

## One final note

This playbook is a tool, not an oath. Rigid adherence to a bad plan is worse than flexible pursuit of a good one. The seven principles (Part I) are the fixed points. Everything else — the 30-minute blocks, the specific templates, the 6-session weeks — is scaffolding you can adjust when evidence tells you to.

Evidence, not mood.
