---
title: "Skill — draft-post"
type: skill
status: active
created: 2026-05-26
tags: [skill, editorial]
---

# Skill — draft-post

> **CLI:** run to turn an idea into a channel-formatted draft. **Web-chat:** paste the prompt.

**Reads:** `12-editorial/ideas/<slug>.md` + `12-editorial/guides/` · **Writes:**
`12-editorial/posts/<slug>.md` (template: `96-templates/tp-post.md`)

## Steps
1. Confirm `channel` + `content-type` (post/thread/newsletter/video-script). If unknown, ASK.
2. Write in the channel's format (rules in `12-editorial/guides/<channel>.md`) and ConsoliDados
   voice (`12-editorial/guides/voice.md`).
3. Set frontmatter: `channel`, `publish-status: draft`, `source-idea`, `series`.

## Guard-rails
- Match the channel's length/format. Keep the voice. Don't publish — `publish-status` stays
  `draft` until the human says otherwise.

---
## Prompt (copy-paste)
> Turn this idea into a <channel> draft in our voice and the channel's format: hook, body, CTA.
> Keep it ready-to-edit, not final.
