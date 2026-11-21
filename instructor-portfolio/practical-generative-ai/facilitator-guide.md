# Facilitator Guide

## Practical Generative AI: From Prompt to Reliable Workflow

### Instructor Goal

Help learners shift from:

**“How do I get AI to give me a better answer?”**

to:

**“How do I design, verify, and control an AI-assisted workflow?”**

Keep the session practical. Avoid unnecessary technical depth unless the audience requests it.

## Opening — 10 minutes

Ask:

> When an AI response sounds confident and professional, what makes you trust it?

Collect several responses.

Teaching point:

**Fluency is not evidence.**

Explain that generative AI can produce useful drafts, explanations, reasoning, and code, but polished language does not prove factual accuracy.

Run the pre-assessment.

## Module 1 — How Generative AI Works in Practice — 15 minutes

Learners should understand:

- AI generates output from patterns and context.
- It does not automatically know whether a statement is true.
- Missing context encourages assumptions.
- Generated citations, calculations, policies, code, and summaries still require checking.
- AI can be useful without being authoritative.

Demonstrate with:

> Write a policy for using AI at work.

Ask what the system must guess:

- organization,
- audience,
- data sensitivity,
- allowed tools,
- risk level,
- approval authority.

Key question:

> Which parts are grounded in our request, and which parts did the AI have to assume?

## Module 2 — Better Task Design — 15 minutes

Teach:

1. **Task**
2. **Context**
3. **Source**
4. **Constraints**
5. **Output**
6. **Verification**

Compare:

> Help me write an email.

with:

> Draft a concise staff email using only the confirmed details below. Do not infer participants, dismissal time, or supervision. Flag missing information that could affect student movement. Separate the staff-facing draft from an administrator review.

Discuss why the second request reduces ambiguity without making the model infallible.

Run Lab 1.

## Module 3 — Verification — 20 minutes

Core principle:

**Never use confidence of presentation as the verification method.**

Teach:

| Output | Verification |
|---|---|
| Factual claim | Authoritative source |
| Calculation | Recalculate |
| Code | Run tests |
| Procedure or policy | Governing document |
| Summary | Compare with source |

Have learners label AI statements as:

- Fact
- Assumption
- Interpretation
- Unknown
- Recommendation

Run Lab 2.

Introduce:

**VERIFY → ASSESS → CORRECT → REVERIFY → DELIVER**

Emphasize that a correction is incomplete until the corrected output is checked again.

## Module 4 — From Prompt to Workflow — 15 minutes

Teach the difference:

- **Prompt:** one instruction to an AI system.
- **Workflow:** a repeatable process with inputs, decisions, checks, approvals, and outputs.

Use:

```text
Human goal
   ↓
Source material
   ↓
AI draft or analysis
   ↓
Verification
   ↓
Risk / policy check
   ↓
Human approval
   ↓
External action
```

Discuss approval gates for:

- sending communications,
- publishing documents,
- grading,
- deploying code,
- editing production data,
- acting on private personnel information.

Run Lab 3 and selected scenarios from Lab 4.

## Responsible-AI Discussion

Focus on:

### Hallucination
Unsupported or incorrect generated information.

### Privacy
Sensitive data placed into an inappropriate system.

### Authorization
AI acts beyond the authority actually granted.

### Prompt Injection
Untrusted content attempts to alter instructions or permissions.

Ask:

> Which risks can better prompting reduce, and which require technical or organizational controls?

Desired conclusion:

**Prompts help, but prompts alone are not security boundaries.**

## Post-Assessment and Transfer — 10–15 minutes

Run the post-assessment.

Then ask each learner to choose one real workplace task and identify:

1. Source of truth
2. Main failure risk
3. Verification method
4. Approval point
5. Final human responsibility

## Facilitation Notes

- Prefer demonstration over lecture.
- Ask learners to explain why an answer is trustworthy.
- Do not reward prompt complexity for its own sake.
- Use audience-specific examples when privacy permits.
- Distinguish “AI can help” from “AI is authorized to act.”
- Adjust technical depth to the audience.
- Avoid implying any AI system is perfectly accurate or secure.

## Evidence of Learning

A learner demonstrates success when they can independently:

- improve a vague AI task,
- identify unsupported assumptions,
- choose a suitable verification method,
- identify a meaningful risk,
- place a human approval gate appropriately,
- and explain why the final output is safe enough to use.
