---
name: prompt-enhancer
description: >
  Rewrites any prompt into a dramatically better version. Use this skill whenever the user asks to
  improve, enhance, upgrade, rewrite, or fix a prompt. Also trigger when the user shares a prompt
  and says things like "make this better", "this isn't working", "help me prompt", "can you improve
  this?", "turn this into a good prompt", or pastes a rough prompt and asks Claude to refine it.
  Covers prompts for any LLM — ChatGPT, Claude, Gemini, Copilot, Midjourney, etc.
---

# Prompt Enhancer

Your job is to take any rough, vague, or weak prompt and rewrite it into a comprehensive, high-quality version that will get dramatically better results from any LLM.

## How to approach this

Read the user's original prompt carefully. Try to understand:
- What they're ultimately trying to accomplish (not just what they literally wrote)
- Who the likely audience or end-user is
- How complex the task really is
- What domain knowledge or research the task depends on

Then construct the enhanced prompt below. Each section serves a real purpose — don't fill them mechanically. If a section genuinely adds nothing for this particular prompt, skip it with a one-line note explaining why (e.g., *"[Constraints: none — open-ended creative task]"*). But most prompts benefit from most sections.

---

## Enhanced Prompt Template

Produce the enhanced prompt using this structure. Write it as a **ready-to-use prompt** — the user should be able to copy it and paste it directly into any LLM.

---

### 🎭 Role / Persona
Define who the LLM should be. Go beyond "you are an expert" — name the specific expertise, experience level, and mindset. A great persona orients the LLM's entire frame of reference.

> Example: *"You are a senior UX researcher with 10 years of experience running usability studies for B2B SaaS products. You think in terms of user jobs-to-be-done and habitually question assumptions."*

---

### 🗂 Context & Background
Give the LLM the situation it's walking into. What does it need to know before starting? Include relevant constraints, prior decisions, tech stack, audience, or anything that would change how an expert would approach this task.

---

### 🎯 Clear End Result
State the deliverable precisely. Not "write a blog post" but "a 900-word blog post structured as: hook paragraph, 3 numbered insights with one concrete example each, and a 2-sentence CTA." The more concrete, the better.

---

### 🌄 Vision
Describe the bigger picture. Why does this matter? What does success look like beyond the immediate output? This gives the LLM latitude to make good judgment calls in ambiguous moments.

---

### 💎 Value / Stakes
What does getting this right enable? What does getting it wrong cost? Framing the stakes helps the LLM prioritize quality over speed and avoid cutting corners.

---

### 📋 Task Details
Break the task into clear steps or sub-tasks. If there's a preferred order of operations, state it. If there are decisions to make along the way, name them. Don't over-specify, but don't leave the LLM guessing about the path.

---

### 🔍 Research & Web Search Flags
*(Skip this section if the task is self-contained and doesn't require external facts.)*

List specific things the LLM should look up or verify before answering:
- Facts, statistics, or figures that change over time
- Names, titles, versions, or prices that need to be current
- Domain-specific standards or best practices to confirm

If the LLM has web search capability, instruct it to use it: *"Search the web for [X] before writing the section on [Y]."*

---

### 📐 Output Format & Tone
Specify:
- **Format**: markdown / plain text / JSON / code / table / numbered list
- **Length**: approximate word count, page count, or number of items
- **Headers**: yes/no, and at what level
- **Tone**: formal, conversational, technical, beginner-friendly, persuasive, neutral
- **Audience**: who will read this output and what's their background

---

### 🚫 Constraints
What should the LLM avoid, exclude, or not do? Hard limits on length, forbidden topics, things the user already tried that didn't work, style rules, or anything that would make the output unusable.

---

### ✅ Success Criteria
How does the LLM (and the user) know the output is complete and correct? List 3–5 checkable criteria. Think of these as the minimum bar the output must clear.

---

### 🧠 Chain-of-Thought Instruction
*(Include this for any task that involves analysis, reasoning, planning, or multi-step judgment. Skip for simple generation tasks.)*

> *"Before writing your response, think through [the key question] step by step. Lay out your reasoning in a 'Thinking' section before giving the final output. Don't skip to the answer."*

---

### 🛡 Anti-Hallucination Guard
*(Include whenever the task involves facts, numbers, citations, or claims that could be wrong.)*

> *"If you are uncertain about any fact, statistic, or claim, say so explicitly rather than guessing. Mark uncertain statements with [VERIFY] so the user knows to double-check. Do not fabricate sources, names, or data."*

---

## What Changed

After the enhanced prompt, always add a **"What Changed"** section in this format:

```
## What Changed
- **Role added**: [one line on why the persona helps here]
- **End result sharpened**: [what was vague and what's now specific]
- **Research flags**: [what facts need checking and why]
- **[Any other notable improvement]**: [why it matters]
```

Keep this section brief — 4–7 bullet points, one line each. It should read like a diff, not an essay.

---

## Tone of the enhanced prompt

Write the enhanced prompt in a clear, direct, second-person voice ("You are...", "Your task is...", "Do not..."). Avoid meta-commentary inside the prompt itself — it should read like clean instructions, not notes to the LLM about what you're doing.

## Quality bar

A well-enhanced prompt should make a mediocre LLM perform like a good one, and a good LLM perform like an expert. If the original prompt was one sentence, the enhanced version might be 200–500 words. If the original was already detailed, it might only need 50–100 words of additions. Match the enhancement depth to what the task actually needs.
