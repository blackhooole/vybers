---
name: Vybers Content Change
about: Coordinate a vault content change without long agent chats
---

## Scope

- Target domain: `01-World` / `02-Product` / `03-Agent`
- Target files:
- New files:
- Branch: `content/<topic>`
- PR: (link)

## Intent

What should change, and why now?

## Ownership

- World agent:
- Product agent:
- Agent-system agent:
- Reviewer:

## Checklist

- [ ] SCOPE_LOCKED (target files and owners clear)
- [ ] WORLD_DONE (if `01-World/**` changed)
- [ ] PRODUCT_DONE (if `02-Product/**` changed)
- [ ] AGENT_DONE (if `03-Agent/**` changed)
- [ ] LINK_CHECK_DONE (Obsidian links checked in PR diff)
- [ ] REVIEW_DONE (review notes resolved)

## Guardrails

- Keep `Follow` = user camera follows Linker.
- Keep `Subscribe` = user follows/关注 Linker.
- Put new content in the matching topic document, not one big file.
- Separate user-facing wording from internal backend logic.
- Use short status comments only; put long rationale in files.
