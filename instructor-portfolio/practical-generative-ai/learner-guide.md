# Learner Guide

## Practical Generative AI: From Prompt to Reliable Workflow

### The Main Idea

Generative AI can produce useful work quickly, but a polished response is not automatically a correct response.

Use this workflow:

**Prompt → Evaluate → Verify → Improve → Govern → Apply**

## 1. Prompt

Describe the task clearly.

A useful structure:

- **Task:** What do I need?
- **Context:** What situation matters?
- **Source:** What information should control the answer?
- **Constraints:** What must the AI avoid or preserve?
- **Output:** What format should it produce?
- **Verification:** What must be checked before I use it?

## 2. Evaluate

Before accepting the output, ask:

- What did the AI know from my prompt?
- What did it have to assume?
- What claims matter?
- What information is missing?
- Does the response actually answer the task?

### Useful labels

- **Fact** — supported by evidence
- **Assumption** — treated as true without confirmation
- **Interpretation** — one possible explanation
- **Unknown** — information not established
- **Recommendation** — suggested action or judgment

## 3. Verify

Match the check to the kind of output.

| AI output | Verification method |
|---|---|
| Factual claim | Check an authoritative source |
| Current information | Check a current source and date |
| Calculation | Recalculate independently |
| Code | Run tests and inspect behavior |
| Procedure or policy | Compare with the governing document |
| Summary | Compare with the original source |

## 4. Improve

Correct missing context, unsupported claims, weak reasoning, or formatting problems.

Then recheck the corrected version.

**Correction without re-verification is incomplete.**

## 5. Govern

Ask:

- Does this involve private or sensitive information?
- Is the AI authorized to perform the requested action?
- Does a human need to approve the result?
- Could untrusted content change the AI's behavior?
- What happens if the output is wrong?

## 6. Apply

Use the output only after the checks appropriate to its risk.

AI can assist with a decision without owning the decision.

## Reflection

For one task you use AI for, identify:

1. Source of truth
2. Most serious failure mode
3. Verification method
4. Human approval point
5. Final person responsible
