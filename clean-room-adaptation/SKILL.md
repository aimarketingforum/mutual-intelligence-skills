---
name: clean-room-adaptation
description: Use this skill whenever the user has found someone else's AI skill, prompt, GitHub repo, template, or workflow and wants to learn from it and build their own version without copying it. Triggers on phrases like "I found this skill/prompt/tool and want to make my own version", "rebuild this without copying", "clean-room", "is this different enough to not violate the license", or any request to adapt, rewrite, or get inspired by someone else's AI tooling. Also use proactively if the user pastes in someone else's skill/prompt content and asks Claude to "improve" or "modify" it for their own use — pause and run this process instead of directly editing their copy.
---

# Clean-Room Adaptation

This skill walks a user through learning from someone else's AI skill, prompt, or template and rebuilding their own version — without copying it.

The full process lives in `clean-room-adaptation.md` in this same folder. Read that file in full before guiding the user through it; it's the canonical version of the process and is also what gets handed to users of other AI tools, so keep this SKILL.md and that file in sync if either changes.

## How to run this with a user

1. Ask the user to share or describe the original skill/prompt/tool they found (paste the text, link the repo, or summarize it).
2. Walk through Steps 1–6 from `clean-room-adaptation.md`, one step at a time — don't skip ahead. This mirrors the user's general preference for one-step-at-a-time work.
3. **Critical: do not directly edit, paraphrase, or "clean up" the original text at any point.** The whole point of Step 1 is to produce an independent summary and then stop referencing the source. If the user pastes the original and asks for a rewrite, write the plain-English summary first, confirm it with them, and only then start building — from the summary, never from the source text.
4. At Step 2 (License Check), if you can web-search, look up the actual license on the source repo/page rather than guessing.
5. At Step 6 (Diff Gate), be honest and specific if something still reads too close to the original — don't rubber-stamp it to be agreeable.
6. If the user wants the end result packaged as a Claude skill, use the `skill-creator` skill for that packaging step once the clean-room content itself is finished.

## Sharing with others

If the user wants to hand this process to someone using a different AI tool (ChatGPT, Gemini, Copilot, etc.), point them to `clean-room-adaptation.md` directly — it's written to be pasted into any chat interface and is fully self-contained.
