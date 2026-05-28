---
title: "Flow — editorial"
type: skill
kind: flow
status: active
created: 2026-05-26
tags: [skill, flow, editorial]
---

# Flow — editorial (idea → [ask channel] → draft → derive → promote)

> **CLI mode:** run when the human says *"I have an idea"* or wants to turn/spread content.
> **Web-chat mode:** paste the relevant prompt block.

**Writes:** `12-editorial/ideas/`, `12-editorial/posts/`

## Steps
1. [[capture-idea]] — structure the idea in `12-editorial/ideas/`. **If the channel isn't
   stated, ASK** (blog / LinkedIn / Substack / X / Instagram / youtube-script). Never assume.
2. [[draft-post]] — write the channel-formatted draft in `12-editorial/posts/` (respect the
   channel rules in `12-editorial/guides/`).
3. [[derive-post]] — optionally adapt to another channel (e.g. blog→LinkedIn), linking
   `derived-from`; group related pieces under a `series`.
4. [[promote-post]] — when a published piece earns audience, deepen it into a Substack/blog
   piece and record metrics.

## Guard-rails
- Channel unknown → ASK. Keep ConsoliDados voice (see `12-editorial/guides/voice.md`).
- YouTube = `content-type: video-script`, parked for now.

---
## Prompt (copy-paste for web chat)
> I have a content idea: <idea>. If I didn't say the channel, ask me which (blog / LinkedIn /
> Substack / X / Instagram / YouTube script). Then structure it as an idea, and on my go write
> the channel-formatted draft. Suggest how to derive it to other channels.
