# research-agentic-math

Researching how (poorly) coding agents handle mathematical reasoning — and what can be done to make them better at it.

## What this is

Transcripts of real sessions where I give competition math problems to coding agents (Claude Code, etc.) and push back on their mistakes. The goal is to document:

- What kinds of errors agents make when doing math (false claims, incomplete proofs, wrong generalizations)
- How they respond to adversarial questioning ("when did you prove that?")
- Whether they can self-correct when challenged
- What interaction patterns lead to correct solutions

## Session naming convention

```
<competition>-<problem>-<agent>-<mode>-<lang>.md
```

- **competition**: e.g. `oma-nacional-2010-1` (OMA Nacional 2010, problem 1)
- **agent**: e.g. `cc-opus46` (Claude Code with Opus 4.6)
- **mode**: `ht` (human-triggered corrections), `auto` (agent self-corrects), etc.
- **lang**: `es` (Spanish), `en` (English)

## Sessions

| File | Problem | Agent | Notes |
|------|---------|-------|-------|
| [oma-nacional-2010-1 (es)](sessions/oma-nacional-2010-1-cc-opus46-ht-es.md) | Non-negative difference game on {1..2010} | Claude Code Opus 4.6 | 3 major errors, all corrected after human pushback |
| [oma-nacional-2010-1 (en)](sessions/oma-nacional-2010-1-cc-opus46-ht-en.md) | Same | Same | English translation |
