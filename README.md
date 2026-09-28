# evidence-first-teaching

Teaching skill that forces "get evidence before speaking."

Every factual claim in an explanation must be traceable to a source you actually opened: code, command output, official docs, a web page or link the user gave you, a local file, an image, or material the user provided. If you can't find a source, say you can't.

## Why

LLMs explain things fluently and confidently whether or not they checked. The failure mode isn't being wrong — it's being wrong in a way that *sounds* verified, with file names and line numbers attached to claims that were never read.

This skill adds a few guardrails against that:

- Three-part answer structure separating what's verified from what isn't
- Seven named fabrication patterns to catch (invented mechanisms, analogies, numbers, quotes, causal chains, cross-system misattribution, and — the worst one — speaking in a "I checked" voice about things you didn't check)
- Explicit rules for handling links and documents the user provides
- Guidance for when the user pushes back: suspect yourself first, never silently swap one unverified claim for another unverified claim

## Install

Copy the directory into your skills folder:

```bash
cp -r evidence-first-teaching ~/.pi/agent/skills/
```

For Claude Code, place it under `.claude/skills/` in your project or `~/.claude/skills/` globally.

## What it does

Loads automatically when the task involves explaining something and the answer risks fabricated mechanisms, analogies, constants, citations, or causal chains. Trigger phrases include "explain how X works", "teach me", "I don't get it", "explain again", "why does X happen", "look at this link/doc".

It does not load for small talk, for explicitly speculative requests ("just guess a possible cause"), or for creative writing.

## License

MIT
