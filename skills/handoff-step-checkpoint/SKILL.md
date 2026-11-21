---
name: handoff-step-checkpoint
description: Pause after every task step and ask the user whether to proceed or revise the current phase.
---

# Handoff step checkpoints

For tasks with multiple steps, establish a clear, ordered sequence of meaningful steps before starting. Keep the steps distinct; do not combine work to avoid a checkpoint.

After completing each step, stop execution and ask the user exactly:

> Step X is complete. Shall I proceed to Step X+1, or would you like to revise anything in this phase?

Replace `X` and `X+1` with the current and next step numbers. Use the `ask_user` tool when available, and do not begin the next step until the user explicitly says to proceed. If the user requests a revision, make that revision within the current phase, then pause and ask again.

Apply the checkpoint after the final planned step as well. If the user chooses to proceed and no planned step remains, ask what they want to do next rather than inventing more work. For a task that genuinely has only one indivisible step, ask at its completion.
