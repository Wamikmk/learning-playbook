# Learning Playbook

A reusable protocol for learning any subject from zero to fluency.
Built around three load-bearing ideas: automaticity before understanding, mastery before advancement, and confusion as diagnostic.

---

## What's in this repo

- `learning-playbook.md` — the full playbook. Principles, setup protocol, daily engine, feedback loop, worked example, copy-paste templates.

---

## How to use it

### First time setting up a new subject

1. Open `learning-playbook.md` and read **Part I** (seven principles). Don't skim — this is the load-bearing part.
2. Work through **Part II** (setup) for your subject. This takes 2–3 hours and produces three things: a target (as a blank-page test), a prerequisite graph, and a frontier diagnosis. Don't skip it — setup quality determines everything downstream.
3. Copy the templates in **Part IX** into a new file, e.g. `subjects/calculus-for-ml/setup.md`, and fill them in.

### Daily

Run the 30-minute session structure from **Part III**. Keep a daily log using the four-line template. Not a journal — four lines.

### Weekly

Same anchor day every week (Sunday works for most people): 30 minutes, four questions from **Part VI**. Write the answers down.

### When stuck

Use the drop-down protocol from **Part IV**. Name the confusion, identify the missing prerequisite, drill it, return. Do not push through.

### When done

Finish the FIRE exercise for the subject (**Part V**). Write the "I can now…" statement. If you can't write it concretely, you're not actually done.

---

## Using this with Claude

Two ways, pick whichever fits your workflow:

**As a Claude Project (recommended for repeat use).**
Create a new Project called "Learning Builder" and paste the contents of `learning-playbook.md` as the project instructions. Then whenever you start a new subject, open a chat in that project and say *"set up a learning plan for [subject]"* — Claude will have the whole methodology loaded and can walk you through Part II live.

**As a one-off attachment.**
In a regular chat, attach `learning-playbook.md` at the start of the conversation.

### How to actually use Claude once you're running the playbook

Claude is good for:
- Finding prerequisites you missed when building the graph.
- Diagnosing *where* your confusion points — describe the confusion, ask which prerequisite is likely missing.
- Generating practice problems at a specified node and difficulty.
- Checking a derivation you've done step-by-step.

Claude is dangerous for:
- Doing your thinking. Every derivation Claude hands you that you didn't struggle for is a practice opportunity lost.
- Creating the feeling of understanding without the ability.

**Rule:** use Claude to sharpen questions, not to answer them.

---

## When not to use this playbook

- When you're learning something purely for enjoyment, not for capability. The playbook is optimized for durable skill.
- When the subject is mostly fact-dense (history, vocabulary, anatomy) rather than hierarchical or skill-based. Parts III–V will feel forced. Lean on spaced repetition tools instead.
- When you don't have at least 4 × 30-minute blocks per week you can actually protect. Below that, the weekly feedback loop doesn't close and the whole thing degrades.

---

## Versioning

This is v1.0. When something about the playbook proves wrong in practice, update it and bump the version. The seven principles in Part I are fixed. Everything else is scaffolding you can adjust based on evidence (not mood).

Keep a short `CHANGELOG.md` when you start making revisions.

---

## Related

Companion repo: **project-playbook** — the equivalent protocol for building projects collaboratively with Claude. One is about *how to learn*; the other is about *how to build*. Use them together.
(https://github.com/Wamikmk/project-playbook)
