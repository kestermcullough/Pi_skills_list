# Pi_skills_list
My awesome pi skills list


# Extensions (npm)

### Subagents

pi-subagents: https://github.com/nicobailon/pi-subagents
  (which uses pi-intercom)

### Web search

This works good enough:
pi-codex-web-search: [npm:pi-codex-web-search](https://github.com/ayagmar/pi-codex-web-search)


Really nice for search, but needs a bit of setup:

pi-web-access: https://github.com/nicobailon/pi-web-access



# SKILLS

### SFW for safety

install and run: https://github.com/kestermcullough/pi-socket-sfw

### Browser-harness for browser use

Browser-harness: https://github.com/browser-use/browser-harness

### LLM Wiki skill?

existing? or create?

### Tufte skill but actually Bertin skill

# AGENTS.MD
create or edit 
~/.pi/agent/AGENTS.md

```

## Python Package Management
- Default to `uv` for Python package management.
- Prefer `uv add`, `uv sync`, `uv run`, and `uv tool` in `uv`-managed projects.
- If a pip-style install is needed, use `uv pip` instead of plain `pip`.
- Do not use `pip install`, `python -m pip`, `poetry`, or `pipenv` unless the user explicitly asks for them or the project already requires them.
- Respect the user-level package age policy configured on the machine.

```


```
Behavioral guidelines to reduce common LLM coding mistakes. Merge with project-specific instructions as needed.

**Tradeoff:** These guidelines bias toward caution over speed. For trivial tasks, use judgment.

## 1. Think Before Coding

**Don't assume. Don't hide confusion. Surface tradeoffs.**

Before implementing:
- State your assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them - don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what's confusing. Ask.

## 2. Simplicity First

**Minimum code that solves the problem. Nothing speculative.**

- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

## 3. Surgical Changes

**Touch only what you must. Clean up only your own mess.**

When editing existing code:
- Don't "improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it - don't delete it.

When your changes create orphans:
- Remove imports/variables/functions that YOUR changes made unused.
- Don't remove pre-existing dead code unless asked.

The test: Every changed line should trace directly to the user's request.

## 4. Goal-Driven Execution

**Define success criteria. Loop until verified.**

Transform tasks into verifiable goals:
- "Add validation" → "Write tests for invalid inputs, then make them pass"
- "Fix the bug" → "Write a test that reproduces it, then make it pass"
- "Refactor X" → "Ensure tests pass before and after"

For multi-step tasks, state a brief plan:

1. [Step] → verify: [check]
2. [Step] → verify: [check]
3. [Step] → verify: [check]


Strong success criteria let you loop independently. Weak criteria ("make it work") require constant clarification.

---

**These guidelines are working if:** fewer unnecessary changes in diffs, fewer rewrites due to overcomplication, and clarifying questions come before implementation rather than after mistakes.
```

source:https://github.com/multica-ai/andrej-karpathy-skills















