# AI 101 Training Exercise
## Prompt Engineering Fundamentals

---

# Exercise 0: Understanding Conversation Memory

## Objective

Learn how AI can use information shared earlier in a conversation.

---

## Step 0A – Provide Context

### Prompt

```text
This is my meeting note. Remember this information for our conversation.

Project: Customer Mobile App Revamp

The project is currently 80% complete.

The mobile application UI redesign has been finished and approved by business users.

The development team reported that API integration is taking longer than expected because of dependencies on the legacy CRM system.

To avoid delaying the overall project timeline, management approved hiring two external developers for one month.

The project manager requested weekly progress reviews until the integration work is completed.

The team agreed to postpone new feature requests until after production go-live.

The target go-live date remains December 15.
```

---

## Step 0B – Ask a Follow-Up Question

### Prompt

```text
What is the biggest risk in this project?
```

### Discussion

- How did the AI know the project details?
- Why wasn't the meeting note repeated?

---

## Step 0C – Ask Another Question

### Prompt

```text
What management decisions were approved?
```

### Discussion

- What information was remembered?
- Why was the answer still relevant?

---

## Step 0D – Request a Different Output

### Prompt

```text
Create a one-paragraph executive update based on our project discussion.
```

### Discussion

- Did we provide the meeting note again?
- How did the AI generate the summary?

---

# Important: Memory Has Limits

## Discussion Question

```text
If AI remembers the meeting note, does that mean it remembers everything forever?
```

---

## Scenario

Imagine the conversation continues for a long time:

- Hundreds of messages
- Multiple topics
- Several reports
- New projects

Later you ask:

```text
What was the target go-live date?
```

### Discussion

- Will AI always remember?
- Should important information be provided again?

---

## Best Practice

### Better

```text
Based on the meeting note we discussed earlier about
the Customer Mobile App Revamp project,
what are the key risks?
```

### Even Better

```text
Meeting Context:

Project: Customer Mobile App Revamp
Go-Live Date: December 15
Current Status: 80% complete

What are the key risks?
```

---

# Exercise 1: Improving a Prompt with Role, Goal, Constraint & Output Format

## Scenario

Use the same meeting note from Exercise 0.

---

## Step 1

### Prompt

```text
Summarize this meeting note.
```

### Questions

- What information is missing?
- Is this summary suitable for executives?
- What improvements would you make?

---

## Step 2

### Prompt

```text
Summarize this meeting note and identify key decisions and action items.
```

### Questions

- How is the output different from Step 1?
- What improved?
- What is still missing?

---

## Step 3

### Prompt

```text
You are an experienced PMO Manager.

Summarize this meeting note.

Highlight:
- Project status
- Key decisions
- Risks
- Action items
```

### Questions

- How did the role affect the answer?
- What new information appears?

---

## Step 4

### Prompt

```text
You are an experienced PMO Manager.

Goal:
Create an executive project update.

Constraints:
- Maximum 80 words.
- Focus only on decisions and risks.
- Use professional business language.
- Ignore technical details not relevant to management.
```

### Questions

- What changed after adding constraints?
- What information disappeared?
- Was that a good thing?

---

## Step 5

### Prompt

```text
You are an experienced PMO Manager.

Goal:
Create an executive project summary.

Constraints:
- Maximum 80 words
- Professional business language
- Focus on decisions and risks

Output Format:

Project Status:
...

Decisions:
- ...
- ...

Risks:
- ...

Actions:
- ...
```

### Questions

- How does specifying output format improve the result?
- Is this easier to consume than previous versions?

---

# Exercise 2: How Role Changes the Answer

## Scenario

A retail company's sales dropped by 15% last quarter.

---

## Prompt A

```text
You are a CFO.

Analyze why sales have dropped by 15%.
```

---

## Prompt B

```text
You are a Marketing Director.

Analyze why sales have dropped by 15%.
```

---

## Prompt C

```text
You are a Sales Director.

Analyze why sales have dropped by 15%.
```

---

## Questions

- How does role influence the answer?
- Which perspective is most useful?
- Can multiple perspectives be valuable?

---

# Exercise 3: No-Shot vs One-Shot vs Few-Shot

## Scenario

Classify the sentiment of this customer review:

```text
The delivery was late, but customer service quickly resolved the issue and was very helpful.
```

---

## No-Shot

### Prompt

```text
Classify the sentiment of this review.

"The delivery was late, but customer service quickly resolved the issue and was very helpful."
```

---

## One-Shot

### Prompt

```text
Example:

Review:
"The product stopped working after two days."

Classification:
Negative

Now classify:

"The delivery was late, but customer service quickly resolved the issue and was very helpful."
```

---

## Few-Shot

### Prompt

```text
Example 1

Review:
"The product stopped working after two days."

Classification:
Negative

Example 2

Review:
"The support team solved my problem immediately."

Classification:
Positive

Example 3

Review:
"The room was clean but noisy."

Classification:
Mixed

Now classify:

"The delivery was late, but customer service quickly resolved the issue and was very helpful."
```

---

# Exercise 4: No-Shot vs One-Shot vs Few-Shot for Content Writing

---

## No-Shot

### Prompt

```text
Write a LinkedIn post about AI.
```

---

## One-Shot

### Prompt

```text
Example:

Cloud computing is no longer a technology decision. It is a business strategy.

Organizations that embrace cloud gain agility, scalability, and faster innovation.

Write a LinkedIn post about AI.
```

---

## Few-Shot

### Prompt

```text
Example 1

Cloud computing is no longer a technology decision. It is a business strategy.

Organizations that embrace cloud gain agility, scalability, and faster innovation.

Example 2

Cybersecurity is no longer an IT issue. It is a business risk.

Organizations that invest in cybersecurity build trust and resilience.

Example 3

Data is no longer a by-product of operations. It is a strategic asset.

Organizations that use data effectively make faster and better decisions.

Write a LinkedIn post about AI.
```

---

# Final Challenge

Improve the following prompt:

```text
Create a project status report.
```

Requirements:

- Add Role
- Add Goal
- Add Constraints
- Add Output Format

Be prepared to share your improved prompt with the class.
