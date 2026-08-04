# Task Loop

**Stop drift. Pick one move. Prove it. Repeat.**

Task Loop is a tiny agent skill for disciplined continuation. It turns "what
next?" into a scored decision, then allows action only when the evidence is
strong enough.

No vibes. No endless polishing. No scope creep.

## The Rule

> Execute the next task only when it reaches the configured confidence threshold.

The default threshold is `85`, but it is a human-configurable policy, not an
empirically validated formula. Adjust it when the project has a clearer local
standard for deciding whether the next action is justified.

If the best task scores below the configured threshold, stop and report why.

## The Loop

Goal -> Evidence -> Score -> One Move -> Verify -> Continue or Stop.

## Use It For

Semi-automatic loop engineering:

- Score the next move
- Execute one verified step
- Continue only with enough evidence

## Install

```bash
mkdir -p ~/.codex/skills/task-loop
cp SKILL.md ~/.codex/skills/task-loop/SKILL.md
```

Then ask the agent to use `task-loop` when you want progress driven by evidence,
not momentum.

## License

MIT. See `LICENSE`.
