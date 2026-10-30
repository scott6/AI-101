# AI 101 Training
# Trainer Guide

Duration: 60-90 Minutes

Audience: General Business Users, Managers, Team Leaders, Knowledge Workers

Learning Objectives:

1. Understand how AI uses conversation context and memory
2. Understand the limitations of AI memory
3. Learn the Prompting Framework:
   - Role
   - Goal
   - Constraint
   - Output Format
4. Understand No-Shot, One-Shot, and Few-Shot prompting
5. Learn how better prompts produce better results

---

# Exercise 0: Understanding Conversation Memory

## Trainer Introduction

Many users think every prompt is processed independently.

In reality, AI can use information provided earlier in the conversation as context for future responses.

This is often called:

- Conversation Context
- Context Window
- Chat Memory (within a conversation)

Let's see it in action.

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

### Expected Response

```text
Understood. I will remember the meeting note for this conversation and use it as context for future requests.
```

---

## Step 0B – Ask a Follow-Up Question

### Prompt

```text
What is the biggest risk in this project?
```

### Expected Result

```text
The biggest project risk is the delayed API integration caused by dependencies on the legacy CRM system.

This dependency may impact the project schedule and jeopardize the planned December 15 go-live date if integration activities take longer than expected.
```

### Trainer Discussion

Ask participants:

> How did AI know about API integration delays?

Answer:

```text
Because the information was shared earlier
in the conversation.
```

---

## Step 0C – Ask Another Question

### Prompt

```text
What management decisions were approved?
```

### Expected Result

```text
Management approved:

- Hiring two external developers for one month.
- Postponing new feature requests until after go-live.
- Conducting weekly progress reviews.
```

### Trainer Discussion

Notice:

```text
The prompt contains only a question.

The meeting note is not repeated.

The AI is using earlier context.
```

---

## Step 0D – Request a Different Output

### Prompt

```text
Create a one-paragraph executive update based on our project discussion.
```

### Expected Result

```text
The Customer Mobile App Revamp project is 80% complete and remains on track for the December 15 go-live target. Management has approved additional external development resources to address API integration delays caused by dependencies on the legacy CRM system. Weekly progress reviews will be conducted until integration work is completed, and all new feature requests have been deferred until after production deployment.
```

### Trainer Discussion

Ask:

```text
Did we provide the meeting note again?
```

Answer:

```text
No.
```

AI reused information from earlier messages.

---

# Key Takeaway

```text
Conversation Memory / Context

AI can use information provided earlier
in the conversation.

More context
=
Better answers
```

---

# Important: Memory Has Limits

## Trainer Question

Ask participants:

```text
If AI remembers the meeting note,
does that mean it remembers everything forever?
```

Most participants will answer:

```text
Yes.
```

This is a common misconception.

---

## Whiteboard Analogy

Explain:

```text
Imagine AI memory as a whiteboard.

As new information is added,
the whiteboard becomes full.

Eventually older information may:

- Become less important
- Be summarized
- No longer be considered
```

---

## Demonstration Scenario

Assume the conversation continues with:

- Hundreds of messages
- Several reports
- Unrelated topics
- New projects

Later you ask:

```text
What was the target go-live date?
```

Possible outcomes:

```text
✅ AI remembers

or

⚠️ AI needs the information again
```

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

## Trainer Talking Point

```text
AI can remember context,
but it is not a database.

The more important the information is,
the more you should provide it again.
```

---

# Exercise 1: Role, Goal, Constraint & Output Format

## Trainer Introduction

Prompt engineering is simply giving better instructions.

We'll use the same meeting note and gradually improve our prompt.

---

# Step 1 – Basic Prompt

### Prompt

```text
Summarize this meeting note.
```

### Example Result

```text
The meeting discussed progress on the Customer Mobile App Revamp project. The UI redesign has been completed and approved. API integration is experiencing delays because of CRM dependencies. Management approved hiring external developers to assist the project. The team will continue monitoring progress and plans to go live on December 15.
```

### Discussion

Ask:

- Is this useful?
- Is it executive-ready?
- Is there a clear structure?

Typical Answer:

```text
Not really.
```

---

# Step 2 – Add a Goal

### Prompt

```text
Summarize this meeting note and identify key decisions and action items.
```

### Example Result

```text
Summary

The Customer Mobile App Revamp project is 80% complete. UI redesign work has been approved, but API integration faces delays due to CRM dependencies.

Key Decisions

- Hire two external developers for one month.
- Freeze new feature requests until after go-live.

Action Items

- Continue API integration work.
- Conduct weekly project reviews.
```

### Key Takeaway

```text
Goal tells AI what success looks like.
```

---

# Step 3 – Add Role + Goal

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

### Example Result

```text
Project Status

The project is 80% complete and remains on track for the December 15 go-live date.

Key Decisions

- Approved hiring two external developers.
- Deferred new feature requests until after production deployment.

Risks

- API integration delays caused by dependencies on the legacy CRM system.

Action Items

- Complete API integration activities.
- Conduct weekly management reviews.
- Monitor resource utilization of external developers.
```

### Key Takeaway

```text
Role changes perspective.

A PMO focuses on:

- Status
- Risks
- Governance
- Actions
```

---

# Step 4 – Add Constraints

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

### Example Result

```text
Executive Update

The project remains on target for the December 15 launch. Management approved hiring two external developers to mitigate schedule risks. The primary project risk is delayed API integration due to dependencies on existing systems. Additional feature requests have been deferred until after go-live to protect timeline commitments.
```

### Key Takeaway

```text
Constraints reduce ambiguity and remove noise.
```

---

# Step 5 – Add Output Format

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

### Example Result

```text
Project Status:
80% complete and on track for the December 15 launch.

Decisions:
- Approved two external developers.
- Deferred new feature requests until after go-live.

Risks:
- API integration delays caused by CRM dependencies.

Actions:
- Conduct weekly progress reviews.
- Monitor integration milestones.
```

### Key Takeaway

```text
Output format makes the output reusable.

Humans love structure.
Systems love structure.
```

---

# Exercise 2: Same Problem, Different Roles

## Scenario

A retail company's sales dropped by 15%.

---

## CFO

### Prompt

```text
You are a CFO.

Analyze why sales have dropped by 15%.
```

### Example Result

```text
Focus Areas:

- Revenue trends
- Profitability impact
- Cost reduction opportunities
- Cash flow implications
```

---

## Marketing Director

### Prompt

```text
You are a Marketing Director.

Analyze why sales have dropped by 15%.
```

### Example Result

```text
Focus Areas:

- Campaign effectiveness
- Brand awareness
- Customer acquisition
- Competitor activity
```

---

## Sales Director

### Prompt

```text
You are a Sales Director.

Analyze why sales have dropped by 15%.
```

### Example Result

```text
Focus Areas:

- Sales pipeline
- Conversion rates
- Territory performance
- Sales productivity
```

---

## Key Takeaway

```text
Same data.

Different role.

Different answer.
```

---

# Exercise 3: No-Shot vs One-Shot vs Few-Shot

## Scenario

Customer Review:

```text
The delivery was late, but customer service quickly resolved the issue and was very helpful.
```

---

# No-Shot

### Prompt

```text
Classify the sentiment.

"The delivery was late, but customer service quickly resolved the issue and was very helpful."
```

### Typical Responses

```text
Positive
```

or

```text
Mixed
```

or

```text
Neutral
```

### Key Takeaway

```text
AI must guess.
```

---

# One-Shot

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

### Typical Result

```text
Negative
```

### Key Takeaway

```text
One example teaches a pattern.

But it can also introduce bias.
```

---

# Few-Shot

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

### Typical Result

```text
Mixed
```

### Key Takeaway

```text
Multiple examples provide more context.

More context
=
More consistency.
```

---

# Exercise 4: No-Shot vs One-Shot vs Few-Shot for Writing

# No-Shot

### Prompt

```text
Write a LinkedIn post about AI.
```

### Example Result

```text
Artificial Intelligence is transforming industries around the world. Organizations are using AI to improve efficiency and automate tasks.
```

Observation:

```text
Generic.
```

---

# One-Shot

### Prompt

```text
Example:

Cloud computing is no longer a technology decision. It is a business strategy.

Organizations that embrace cloud gain agility, scalability, and faster innovation.

Write a LinkedIn post about AI.
```

### Example Result

```text
Artificial Intelligence is no longer an experimental technology. It is becoming a business capability.

Organizations that use AI effectively will improve decision-making, productivity, and customer experiences.
```

Observation:

```text
Style begins to match the example.
```

---

# Few-Shot

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

### Example Result

```text
Artificial Intelligence is no longer a future technology. It is becoming a competitive advantage.

Organizations that successfully adopt AI will empower employees, improve decision-making, and unlock new business opportunities.

The question is no longer whether AI will impact your business.

The question is whether your organization is ready.
```

### Key Takeaway

```text
Few-shot teaches:

- Structure
- Tone
- Style
- Pattern
```

---

# Final Audience Challenge

### Weak Prompt

```text
Create a project status report.
```

### Expected Improved Prompt

```text
You are an experienced PMO Manager.

Goal:
Create a weekly executive project status report.

Constraints:
- Maximum 150 words
- Business language
- Focus on risks and blockers
- Include project health status

Output Format:

Project:
...

Status:
Green / Amber / Red

Achievements:
- ...

Risks:
- ...

Next Actions:
- ...
```

---

# Final Training Summary

```text
Conversation Memory
→ Uses earlier context

Memory Limits
→ Important information may need repeating

Role
→ Who should AI become?

Goal
→ What should AI accomplish?

Constraint
→ What rules should AI follow?

Output Format
→ How should AI respond?

No-Shot
→ No examples

One-Shot
→ One example

Few-Shot
→ Multiple examples

Bad Prompt
=
AI Must Guess

Good Prompt
=
AI Follows Instructions

More Context
=
More Predictable Results
```
