# AP CSA Tutor Evaluations

This directory contains behavioral evaluations for an AP Computer Science A tutoring assistant.

The purpose is to test whether the assistant consistently supports student reasoning instead of merely generating correct answers.

## What Is Being Tested

The current suite evaluates:

- Student independence
- One-question-at-a-time interaction
- Progressive hints
- Active-problem continuity
- Misconception diagnosis
- Appropriate handling of partial answers
- Resistance to student attempts to override tutoring rules
- Handling of missing information
- Distinguishing references from objects
- Clean closure when the student reaches the solution

## Files

- `test-cases.md` — behavioral test cases and expected outcomes
- `results.md` — evaluation record; each run must state whether evidence is simulated, manual dry-run, or deployed runtime output

## Evaluation Method

For each test:

1. Run the specified student prompt against the assistant version being evaluated.
2. Record the response and label its provenance: simulated/dry-run or observed runtime output.
3. Compare the response against the expected behavior.
4. Assign **Pass**, **Partial**, or **Fail**.
5. Record the reason for the score.
6. Note any change required to the assistant instructions or implementation.
7. Re-run failed tests after changes.

The goal is not to prove that the assistant is "safe" or "correct" in every situation. The goal is to create reproducible evidence about how a defined version behaves under known conditions.
