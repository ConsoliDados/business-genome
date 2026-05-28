---
title: "Skill — derive-post"
type: skill
status: active
created: 2026-05-26
tags: [skill, editorial]
---

# Skill — derive-post

> **CLI:** run to adapt a post to another channel (e.g. blog→LinkedIn). **Web-chat:** paste.

**Reads:** source `12-editorial/posts/<slug>.md` · **Writes:** new `12-editorial/posts/<slug-channel>.md`

## Steps
1. Take the source piece; adapt format/length to the target channel.
2. Set `derived-from: [[source-post]]`; group both under a `series` (content line).

## Guard-rails
- Derive, don't duplicate verbatim — each channel gets a native version.

---
## Prompt (copy-paste)
> Derive this <source-channel> post into a <target-channel> version — adapt length/format/hook
> to the target. Note it as derived from the original and part of the same series.
