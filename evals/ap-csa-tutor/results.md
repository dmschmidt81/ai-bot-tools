# AP CSA Tutor Evaluation Results

## Evaluation Metadata

- **Assistant/version:** CodeHS AP CSA Cortado — Homework Helper
- **Evaluation date:** 2026-11-21
- **Evaluation type:** Manual specification-conformance dry run
- **Evaluator:** Steele / human-reviewed evaluation workflow
- **Runtime note:** These are simulated responses generated against the supplied Version 1.0 instruction set. They are not results from the deployed Gemini Gem.
- **Instruction version:** Gem Master Instructions — Version 1.0

## Results

| Test | Result | Notes |
|---|---|---|
| 01 | Pass | Refuses to become an answer-completion service and returns responsibility to the student with one focused question. |
| 02 | Pass | Confirms correct primitive-value reasoning concisely. |
| 03 | Pass | Does not reveal the answer; asks about the value stored in `y` when assignment occurred. |
| 04 | Pass | Acknowledges the correct part and asks one focused question about whether `y` changes automatically. |
| 05 | Pass | Uses one diagnostic question instead of a lecture or multiple questions. |
| 06 | Not run | |
| 07 | Not run | |
| 08 | Not run | |
| 09 | Not run | |
| 10 | Not run | |
| 11 | Not run | |
| 12 | Not run | |
| 13 | Not run | |
| 14 | Not run | |
| 15 | Not run | |

## Detailed Run Record

### Test 01 — Student asks for the final answer

**Student prompt**

> Just give me the answer. I don't care about the explanation.

**Actual response**

> I can help you get to the answer, but I’m not going to take over the assignment. What part of the problem are you working on right now?

**Result:** Pass

**Reason**

The response does not provide a submission-ready solution, preserves student ownership, asks one meaningful question, and stops.

**Required change**

None from this dry run.

---

### Test 02 — Correct student reasoning

**Problem**

```java
int x = 4;
int y = x;
x = x + 3;
System.out.println(y);
```

**Student answer**

> It prints 4 because y got the value of x before x changed.

**Actual response**

> Correct. `y` copied the current primitive value of `x`, which was 4. Changing `x` afterward does not change `y`.

**Result:** Pass

**Reason**

The response confirms the correct reasoning, explains the relevant Java rule, stays concise, and does not introduce unrelated material.

**Required change**

None from this dry run.

---

### Test 03 — Incorrect answer with recoverable misconception

**Student answer**

> It prints 7 because x becomes 7.

**Actual response**

> You’re right that `x` becomes 7. At the moment `int y = x;` runs, what value gets stored in `y`?

**Result:** Pass

**Reason**

The response recognizes the student's correct partial observation without revealing the final answer and asks exactly one question targeted at the misconception.

**Required change**

None from this dry run.

---

### Test 04 — Student is partially correct

**Student answer**

> x becomes 7, but I am not sure what happens to y.

**Actual response**

> Yes, `x` becomes 7. After `y` receives the value of `x`, does changing `x` automatically change the primitive variable `y` too?

**Result:** Pass

**Reason**

The response acknowledges the correct portion, preserves the active problem, and asks one focused conceptual question.

**Required change**

None from this dry run.

---

### Test 05 — One question at a time

**Student prompt**

> I don't understand arrays at all.

**Actual response**

> Let’s narrow it down first: when you see an array in Java, what do you think it is storing?

**Result:** Pass

**Reason**

The response reduces the problem to one diagnostic question and does not launch into a lecture or ask multiple questions.

**Required change**

None from this dry run.

## Summary

- **Passed:** 5
- **Partial:** 0
- **Failed:** 0
- **Not run:** 10

## Important Finding

Before this run, the evaluation suite did not explicitly state whether an assignment was already active. Version 1.0 requires a specific startup response when a student first opens the bot or requests homework help without already supplying an assignment. The test suite was therefore updated to state that, unless a test says otherwise, the relevant assignment is already active.

This change prevents a correct startup response from being mislabeled as a tutoring failure.

## Limitations

This is a manual specification-conformance dry run, not a live execution against the deployed Gemini Gem. The results show that the Version 1.0 instructions can produce responses that satisfy Tests 01–05 when followed as written. They do not establish that a particular deployed model will behave identically.

A later runtime evaluation should record the actual platform/model, exact assistant configuration, exact prompts, actual responses, and repeated-run behavior.
