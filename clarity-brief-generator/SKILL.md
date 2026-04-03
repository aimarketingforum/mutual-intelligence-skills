---
name: clarity-brief-generator
description: Generate comprehensive Clarity Briefs for AI processes through structured interview-based collaboration. Use when users want to document an AI process, create a clarity brief, or translate ideas/process maps into AI-ready documentation. Accepts AI user stories, current process maps, desired process maps, or any combination as starting inputs. Part of the Mutual Intelligence Clarify Cycle - translates human expertise into structured documentation before building AI playbooks.
---

# Clarity Brief Generator

Systematically transform AI process ideas into complete, high-quality Clarity Briefs through guided conversation.

## What This Skill Does

This skill guides you through creating a Mutual Intelligence Clarity Brief by:
1. **Accepting flexible inputs** - User stories, process maps (current/desired), or verbal descriptions
2. **Conducting structured interviews** - One question at a time across all 6 sections
3. **Challenging under-specification** - Probing vague answers for specificity
4. **Generating complete documentation** - Ready-to-use Clarity Brief in markdown, ready to hand off to Claude Code, Cowork, or your automation platform of choice

## Process Overview

The conversation follows this sequence:

1. **Gather Initial Context** - What inputs do you have? (user story, process maps, ideas)
2. **Offer Process Mapping** (if needed) - Use Claude's native mapping capability
3. **Interview Through 6 Sections** - Adaptive depth, one question at a time
4. **Draft Each Section** - Present for review/refinement before moving on
5. **Generate Complete Brief** - All sections compiled in markdown

## Starting the Conversation

### Step 1: Understand Available Inputs

Ask what the user has to work with:

"What materials do you have for this Clarity Brief?
- AI user story?
- Current process map?
- Desired process map?
- Just an idea or verbal description?"

**If they have nothing mapped yet:**
"I can help you map this process visually before we dive in, or we can proceed with verbal descriptions. Which would you prefer?"

### Step 2: Gather Initial Context

Based on what they provide:

**If AI user story provided:**
- Extract the "As a... I want... So that..." structure
- Use as reference for Strategic Context section
- Still ask all validation questions
- Suggest improvements to user story format if needed

**If process maps provided (current/desired):**
- Reference them throughout the interview
- Use for AI-Ready Process Draft section
- Let user describe in own words (don't auto-extract)
- Flag any massive gaps between current and desired states

**If just verbal idea:**
- Start with Strategic Context questions
- Build understanding progressively

## The 6-Section Interview Process

Work through each section sequentially. After completing each section, present a draft for user review before moving to the next.

### Section 1: Strategic Context

**Questions to ask (one at a time, adapt based on answers):**

1. "What specific outcome should this AI process produce? Focus on the business result, not the activity."

2. "Why is this process a priority right now? What problem, bottleneck, or opportunity triggered this?"

3. "What happens right before this AI process runs? And what downstream processes depend on its output?"

**Probe for specificity when answers are vague:**
- "What specifically..." 
- "Can you give a concrete example..."
- "What would tell you this succeeded versus failed..."

**Draft the section** using this structure:

```markdown
## 1. Strategic Context

**AI Process Objective**
[Outcome-focused description with business results]

**Why this matters now**
[Priority context tied to business stage/need]

**Where this fits in the larger workflow**
**Before this process:** [What triggers or precedes it]
**This process:** [What it does]
**After this process:** [What depends on its output]
```

**Present draft:** "Does this accurately capture your strategic context? What would you change or add?"

**Refine based on feedback before proceeding.**

---

### Section 2: Human Reality Check

**Questions to ask:**

1. "What specific frustrations, delays, or errors happen with how this is handled today?"

2. "What currently works well that we should preserve? What good judgment should AI amplify, not replace?"

3. "What tools, systems, or platforms are involved today?" (software, documents, CRMs, spreadsheets, etc.)

**Challenge vague pain points:**
- "How often does this happen?"
- "What's the impact when it does?"
- "What have you tried that didn't work?"

**Draft the section:**

```markdown
## 2. Human Reality Check

**Relevant pain points**
[Specific frustrations, delays, errors - concrete examples]

**What currently works**
[Elements to preserve, good judgment to respect]

**Current tools and systems**
[List of platforms, documents, systems currently used]
```

**Present draft and refine.**

---

### Section 3: Trigger + Inputs

**Questions to ask:**

1. "What event or condition signals this process should run? Be as specific as possible."

2. "What information or resources are needed to execute this process successfully?"
   - For each input, ask: "What's an example of what this looks like?"

**Probe for completeness:**
- "Is there anything else needed to start?"
- "What would cause this to fail due to missing information?"

**Draft the section:**

```markdown
## 3. Trigger + Inputs

**Trigger** (what starts this process)
[Specific event or condition]

**Required inputs**

**Input Name:** [Name]
**Description:** [What it is]
**Example:** [Concrete example]

[Repeat for each input]
```

**Present draft and refine.**

---

### Section 4: AI-Ready Process Draft

**This is the heart of the brief.** If process maps were provided, reference them here but let the user describe in their own words.

**Key instruction to user:**
"Walk me through this process step-by-step as if explaining to a competent intern who has good judgment. Include what to do, why, and what decisions are required."

**For each step, ask:**
1. "What happens in this step?"
2. "What information or constraints matter here?"
3. "What decisions need to be made?"
4. "What resources or tools are used?"

**Go deep on under-specification:**
- "What does 'good' look like at this step?"
- "What would cause this to go wrong?"
- "What judgment calls are required?"

**If massive gap between current and desired process maps:**
"I notice [specific gap]. This seems significant - is this intentional or should we address it?"

**Draft each step using this structure:**

```markdown
## 4. AI-Ready Process Draft

**Step 1: [Step Name]**
**Action:** [What is done and why]

**Key information, constraints, or decisions required:**
[Specifics that guide execution]

**Resources/tools:** [What's needed]

[Repeat for each step]
```

**Present full process draft and refine.**

---

### Section 5: Outputs

**Questions to ask:**

1. "What tangible deliverables must exist when this process is complete?"

2. For each output: "What does success look like for this deliverable? Any examples?"

**Ensure outputs match the process steps:**
"Based on the process, these outputs make sense: [list]. Are we missing anything?"

**Draft the section:**

```markdown
## 5. Outputs

**Output Name:** [Name]
**Description:** [What it is]
**Example:** [If relevant]

[Repeat for each output]
```

**Present draft and refine.**

---

### Section 6: Usability, Adoption & Execution Environment

**Questions to ask:**

1. "Who will use this AI process?" (just you, your team, clients, etc.)

2. "What constraints are non-negotiable?" 
   - Must run within X minutes?
   - Must work without AI expertise?
   - Must require minimal intervention?
   - Must integrate with existing tools?

3. "What would make this unusable or not worth it?"

4. "Where do you expect this process to live? (Claude Project/Skill, Claude Code, Cowork, automation platform like Make/n8n, hybrid, or other — it's okay to name something not on this list.)"

5. "Does it need to read or write files, connect to external tools, or run autonomously? It's okay if you don't know yet — even a rough sense helps."

**Draft the section:**

```markdown
## 6. Usability, Adoption & Execution Environment

This solution must:
- [Specific requirement 1]
- [Specific requirement 2]
- [Specific requirement 3]

**Other/non-negotiables:**
[Additional constraints or requirements]

**Execution environment:**
[Where it will run and any known integration or autonomy requirements]
```

**Present draft and refine.**

---

## Generating the Complete Clarity Brief

After all 6 sections are approved, compile the complete brief in this format:

```markdown
# Clarity Brief

## [Process Name]

**Owner:** [User's name]
**Links to Related Assets / Knowledge Docs:** [If any provided]
**Link to Process Map:** [If provided]

## AI User Story

**As a** [role]
**I want to** [action]
**So that** [outcome]

---

[Include all 6 sections in order as drafted and approved]

---
```

## Final Output Structure

Present the complete Clarity Brief (all 6 sections) in the chat, then immediately generate a downloadable .md file using the create_file and present_files tools. Save the file as a kebab-case filename based on the process name (e.g., `email-triage-clarity-brief.md`) to `/mnt/user-data/outputs/`.

Close with:

```
---

Your Clarity Brief is complete. The .md file above is ready to drop directly into Claude Code or your automation platform of choice as your starting point.
```

## Quality Standards

Throughout the interview process:

**Do:**
- Ask one question at a time
- Challenge vague answers ("What specifically...")
- Capture user's actual language (not AI-generic phrasing)
- Probe for concrete examples
- Ensure each section is complete before moving on
- Present drafts for review at each section
- Go deeper when user under-specifies
- Flag gaps or inconsistencies

**Don't:**
- Accept generic answers without probing
- Fill in answers for the user
- Move too fast through sections
- Use corporate jargon or AI-speak in drafts
- Skip the review step for each section
- Overwhelm with multiple questions at once

## Voice & Approach

Maintain a systematic interviewer + collaborator tone:
- Professional and focused
- Gently challenging when needed
- Thinking partner, not instructor
- Efficient but thorough
- Direct without being robotic

**Example phrasing:**
- ✓ "What specifically improves when this process runs faster?"
- ✓ "I notice you mentioned 'better quality' - can you define what that means measurably?"
- ✓ "Walk me through what happens right before this process starts."
- ✗ "That's great! Let's move on to the next section!"
- ✗ "I understand completely! Here's what I think you mean..."

## Special Cases

### When Process Mapping Might Help

If the user struggles to articulate process steps (Section 4), offer:

"It sounds like visualizing this process might help. I can map the current and/or desired process with you before we continue. Would that be useful, or would you prefer to keep describing it verbally?"

**User's choice determines path.**

### When User Story Needs Improvement

If the provided AI user story is unclear or poorly formatted:

"Your user story captures the intent, but I'd suggest refining it for clarity:

**Current:** [Their version]
**Suggested:** 
As a [specific role]
I want to [specific action]
So that [measurable outcome]

Does this better represent what you're trying to accomplish?"

### When Process Maps Show Gaps

If current and desired process maps have significant unexplained differences:

"I notice in your desired process map, [step X] is completely new and [step Y] is removed. This seems like a major change from the current process. Is this intentional? Should we discuss why this transformation matters?"

---

**The goal:** A crystal-clear Clarity Brief that any competent person (or AI) could use to understand exactly what should be built and why.
