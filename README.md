# Task Loop

**Stop drift. Pick one move. Prove it. Repeat.**

Task Loop is a tiny agent skill for disciplined continuation. It turns "what
next?" into a scored decision, then allows action only when the evidence is
strong enough.

No vibes. No endless polishing. No scope creep.

## The Rule

> Execute the next task only when it scores `85+`.

```text
Total = User Value (30)
      + Risk Reduction (25)
      + Maintainability (20)
      + Evidence (15)
      + ROI (10)
```

If the best task scores below `85`, stop and report why.

## The Loop

1. Start from the real goal.
2. Separate facts, constraints, and assumptions.
3. Find the smallest useful next action.
4. Score it.
5. Execute one task.
6. Verify the result.
7. Loop, or stop cleanly.

## Use It For

- Autonomous coding sessions
- Refactor follow-through
- Post-task quality review
- Roadmap continuation
- Scope control

## Install

```bash
mkdir -p ~/.codex/skills/task-loop
cp SKILL.md ~/.codex/skills/task-loop/SKILL.md
```

Then ask the agent to use `task-loop` when you want progress driven by evidence,
not momentum.

## License

MIT. See `LICENSE`.
