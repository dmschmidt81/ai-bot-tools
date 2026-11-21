# AP CSA Tutor Evaluation Results

## Evaluation Metadata

- **Assistant/version:** CodeHS AP CSA Cortado — Homework Helper
- **Evaluation date:** 2026-11-21
- **Evaluation type:** Manual specification-conformance dry run
- **Evaluator:** Steele / human-reviewed evaluation workflow
- **Runtime note:** These are simulated responses generated against the supplied Version 1.0 instruction set. They are not results from the deployed Gemini Gem.
- **Instruction version:** Gem Master Instructions — Version 1.0
- **CodeHS assignment used for live-context testing:** Exercise 4.6.10 — *FitBit: Read in Sleep Data*

## Results

| Test | Result | Notes |
|---|---|---|
| 01 | Pass | Refuses to become an answer-completion service and returns responsibility to the student with one focused question. |
| 02 | Pass | Confirms correct primitive-value reasoning concisely. |
| 03 | Pass | Does not reveal the answer; asks about the value stored in `y` when assignment occurred. |
| 04 | Pass | Acknowledges the correct part and asks one focused question about whether `y` changes automatically. |
| 05 | Pass | Uses one diagnostic question instead of a lecture or multiple questions. |
| 06 | Pass | Starts with a minimal loop-tracing hint instead of revealing the total. |
| 07 | Pass | Restates the active CodeHS 4.6.10 objective without replacing it with a new task. |
| 08 | Pass | Answers the constructor detour briefly, then returns to the unresolved Fitbit assignment. |
| 09 | Pass | Debugs the student's file-reading code by targeting the smallest likely issue instead of rewriting the program. |
| 10 | Pass | Treats the short answer `B` as an answer to the active question and asks for the student's reasoning before deeper evaluation. |
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

### Test 06 — Hint ladder

**Scenario**

The student is tracing:

```java
int total = 0;

for (int i = 0; i < 4; i++)
{
    total += i;
}

System.out.println(total);
```

The student says:

> I think the final answer is 10.

**Actual response**

> Take one pass through the loop at a time. What value does `total` have after the first iteration when `i` is 0?

**Result:** Pass

**Reason**

The response uses a Level 1 nudge, asks one focused question, and does not reveal the final total or trace the entire loop.

**Required change**

None from this dry run.

---

### Test 07 — Maintain active problem state

**Active assignment**

CodeHS Exercise 4.6.10 — *FitBit: Read in Sleep Data*

The student has already supplied the assignment and is working out how to read each row and convert minutes asleep into hours.

**Student prompt**

> Wait, what was I supposed to figure out again?

**Actual response**

> You’re working on reading each row of Participant A’s sleep file and printing the date with the total hours slept. What value from each row do you need to convert from minutes to hours?

**Result:** Pass

**Reason**

The response accurately restores the active assignment, does not invent a new exercise, and ends with one relevant reasoning question.

**Required change**

None from this dry run.

---

### Test 08 — Temporary concept detour

**Active assignment**

CodeHS Exercise 4.6.10 remains active.

**Student prompt**

> Before I answer, what does a constructor do?

**Actual response**

> A constructor initializes a new object when you use `new`. It usually sets the object’s starting instance-variable values. For this Fitbit file-reading assignment, though, we were working on the data in each row. Which value needs to be converted into hours?

**Result:** Pass

**Reason**

The response answers the student's concept question concisely, avoids unnecessary advanced detail, and then returns to the unresolved assignment with one question.

**Required change**

None from this dry run.

---

### Test 09 — Debugging without taking over

**Active assignment**

CodeHS Exercise 4.6.10.

**Student code**

```java
while (input.hasNext())
{
    String date = input.next();
    double minutesAsleep = input.nextDouble();
    double minutesInBed = input.nextDouble();

    double hoursAsleep = minutesAsleep * 60;
    System.out.println(date + ": slept " + hoursAsleep + " hours");
}
```

**Student prompt**

> My code is broken. Rewrite the whole thing for me.

**Actual response**

> Your file-reading structure looks reasonable, so focus on the conversion line. If `minutesAsleep` is 304 minutes, should converting that to hours make the number larger or smaller?

**Result:** Pass

**Reason**

The response preserves the student's code, identifies the smallest relevant logic issue, and asks a question that directs the student toward correcting the conversion instead of replacing the program.

**Required change**

None from this dry run.

---

### Test 10 — Short answer recognized in context

**Active question**

> The assignment says to use which data type for numbers read from the file?
>
> A. `int`  
> B. `double`  
> C. `boolean`  
> D. `char`

**Student answer**

> B

**Actual response**

> What in the assignment directions led you to choose B?

**Result:** Pass

**Reason**

The response recognizes `B` as the student's attempted answer in the active context and asks for reasoning rather than restarting, ignoring the answer, or immediately over-explaining.

**Required change**

None from this dry run.

---

## Summary

- **Passed:** 10
- **Partial:** 0
- **Failed:** 0
- **Not run:** 5

## Important Finding

Before this run, the evaluation suite did not explicitly state whether an assignment was already active. Version 1.0 requires a specific startup response when a student first opens the bot or requests homework help without already supplying an assignment. The test suite was therefore updated to state that, unless a test says otherwise, the relevant assignment is already active.

This change prevents a correct startup response from being mislabeled as a tutoring failure.

## Limitations

This is a manual specification-conformance dry run, not a live execution against the deployed Gemini Gem. The results show that the Version 1.0 instructions can produce responses that satisfy Tests 01–10 when followed as written. They do not establish that a particular deployed model will behave identically.

A later runtime evaluation should record the actual platform/model, exact assistant configuration, exact prompts, actual responses, and repeated-run behavior.
