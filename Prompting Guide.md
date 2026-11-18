## How we work
1. **Brainstorm** in the Claude chat. Describe what I'm imagining with words, screenshots, or references.
2. The chat writes the **exact prompt** and tells me which **model** to use.
3. On the gaming laptop, run `/clear`, then `/model <model>`, then paste the prompt.
4. For big tasks the agent posts a plan first. I either reply "ok" or correct it.
5. **Test** it in Studio, then tick the box in [[Roadmap]].
6. **Report back** to the chat by pasting the newest [[CHANGELOG]] entry and screenshots of anything that looks off. The chat uses that to write the next prompt.

## Rules of thumb
- One feature, system, or bug per prompt.
- Interrupting with Esc is always fine, since the place is saved and the log says where it stopped.
- If a bug is in something that's about to get replaced, skip it.
- If the agent keeps looping on a fix, tell it "stop, explain the problem in plain English, and give me 2 approaches."
- To roll back, go to Creator Hub, then the place, then Version History.
- Never have the place open in Studio on two computers at the same time.

## Models (the chat will usually tell me)
- Opus is for new systems and anything everything else builds on.
- Sonnet is for small, clear tasks, assets, layout, and most bugs. It uses way less of the limit.
- If Sonnet hasn't fixed a bug after 2 tries, switch to Opus.

## Quick one-off templates (for when I don't ask the chat)

**Bug**
```
Bug: <what went wrong>
Steps: <what I did right before it>
Expected: <what should have happened>
<red Output lines / screenshot>
Find the root cause, fix it, playtest it, do the logging steps, and tell me the cause in one sentence.
```

**Small tweak**
```
Tweak: <e.g. make Spark Snap's explosion 30% bigger>
Change only what's needed, playtest it, and do the logging steps.
```