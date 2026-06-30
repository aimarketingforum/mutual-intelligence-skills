# Clean-Room Adaptation Process

A repeatable process for learning from someone else's AI skill, prompt, template, or workflow and rebuilding your own version of it — without copying their work.

Works with any AI assistant (Claude, ChatGPT, Gemini, Copilot, etc.). Copy this whole document into a new chat with the tool you're using and say "follow this process with [the thing I found]."

---

## Why this exists

Copyright protects the specific way something is written — the exact wording, instructions, examples, and structure. It does NOT protect the underlying idea or method. "A tool that checks GitHub packages for trust signals before installing them" is an idea, free to use. The specific paragraphs someone wrote to do that are not.

This process keeps you on the right side of that line: you learn what something does, then build your own version from that understanding — never by editing, paraphrasing, or lightly reordering the original text.

This is not legal advice. If you're shipping something commercially and license terms matter to your business, get a real opinion. This process is about good practice, not a legal guarantee.

---

## The Process

### Step 1: Read & Summarize

Read the original skill, prompt, or template in full. Then write a **plain-English functional summary** — what it does, what problem it solves, what order it does things in, what judgment calls it makes. No copied phrasing. No copied examples. Just the function.

Once the summary is written, **set the original aside.** Don't keep referring back to it while you build. You're now working from your own summary, not their text.

> Test: could you explain this summary to a colleague without ever having seen the original? If not, write it again until you can.

### Step 2: License Check

Identify the license on the original (check the repo, the file header, or ask the source). Note:
- Does it require attribution?
- Is it copyleft (meaning anything you build *from* it must also be shared under the same license)?
- Does it restrict commercial use?
- Is there no license at all? (Default assumption: all rights reserved — treat it as restricted unless told otherwise.)

This determines how far you can go. If it's strong copyleft and you're shipping commercial work, the safest move may be to not derive from it at all — use it as inspiration for the idea only, build 100% from scratch.

### Step 3: Structural Reset

This is the step people skip, and it's the one that actually matters.

Don't keep the original's step order, section names, or framing. Force a different structure — ideally one tied to your own existing way of organizing work (your own framework, your own naming, your own sequence of questions). If the original has 6 steps in a specific order, your version should not have 6 steps in the same order with renamed labels.

> Test: lay your draft next to the original. If someone could match each section 1-to-1, restructure again.

### Step 4: Make It Actually Yours

Add what only you have: your own voice, your own examples, your own judgment calls (what counts as a red flag, what's an acceptable tradeoff, what you'd personally do differently). This is the step that turns "inspired by" into "genuinely a different work that happens to solve a similar problem."

If you have existing frameworks, vocabulary, or systems you use for other things, this is the natural place to fold them in.

### Step 5: Attribution

Even when not legally required, add a short line crediting where the idea came from. Costs nothing, buys goodwill, and is just honest. Example:

> "Process informed by [source name]'s approach to [problem]; rebuilt independently."

### Step 6: Diff Gate (final check before you use or share it)

Before finalizing, compare your new version against the original one more time and ask honestly:

- Does this read like genuinely independent work, or like the original reordered with new words?
- Did any example, list, or specific phrase get carried over without being rewritten from scratch?
- Would I be comfortable showing both versions side by side to the original author?

If anything fails this check, go back to Step 3 or Step 4 — don't patch around it.

---

## Quick Reference

| Step | Output |
|---|---|
| 1. Read & Summarize | Plain-English summary, original set aside |
| 2. License Check | List of obligations/restrictions |
| 3. Structural Reset | New step order/framing, not theirs |
| 4. Make It Yours | Your voice, examples, judgment calls added |
| 5. Attribution | One-line credit |
| 6. Diff Gate | Final independence check, pass/fail |

## What this process is NOT for

- It doesn't make plagiarism okay if you skip steps and just want to feel better about copying something.
- It doesn't replace reading an actual license or getting legal advice for anything high-stakes or commercial at scale.
- It's not a way to launder someone's proprietary, paid product into a free clone — if the original is a paid commercial offering and your "rebuild" competes directly with it, the ethical bar is higher than this checklist alone covers. Use judgment.
