---
name: "task-loop"
description: "Find and execute the next highest-value task from first principles. Use at the end of each task, or when the user asks to keep going or optimize further."
---

# Task Loop

1. Use the current result and available evidence, such as tests, errors,
   feedback, outputs, TODOs, and architecture gaps, to generate local and global
   candidate tasks from first principles:
   - Work backward from the final goal. Separate facts, constraints, and
     assumptions. Do not treat the current implementation as inevitable.
   - Prioritize the biggest current bottleneck and root cause. Do not optimize
     secondary issues or surface symptoms.
   - Choose the smallest action that can produce a verifiable increment.
2. Score each candidate with explicit reasoning. Use the configured threshold;
   default to `85` when no threshold is provided.

3. Select the highest-scoring task:
   - **At or above threshold**: If it is a natural extension of the current goal,
     execute it immediately.
   - **Below threshold**: Do not execute it. Report the reasoning and wait for
     the user to decide.
4. After execution, verify the result, review this round's output, and return to
   step 1.
5. Stop when no executable task reaches the configured threshold.

Execute only one task per round. Do not make evidence-free suggestions, pad the
list, or expand the goal.

Report each round's task and score, output and changes, and remaining
recommendations.
