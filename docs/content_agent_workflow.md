# Content Agent Workflow

Goal: keep Vybers as a coherent shared vault while allowing multiple agents or humans to work in parallel without long coordination chats.

## Current Logic

The vault is organized by domain:

- `01-World/` holds world rules, Linker concepts, Crystal Memory, and visibility logic.
- `02-Product/` holds user-facing product flows and interaction systems.
- `03-Agent/` holds agent entry, Linker creation, and agent-related mechanics.

The README rule is important: new content should go into the matching topic document instead of one large catch-all file.

## GitHub-Native Model

Use GitHub as a lightweight content coordination layer:

- Issue = content change request, target files, acceptance criteria, and open questions.
- Branch = one coherent content change.
- PR = review surface for diffs and cross-link integrity.
- Vault files = source of truth.
- Comments = short status only; long rationale belongs in a design note or changed document.

## Parallel Ownership Rules

Split content work by path and concept boundary:

| Stream | Owns | Should avoid |
|---|---|---|
| World agent | `01-World/**` | Product UI copy unless it changes a world rule |
| Product agent | `02-Product/**` | Rewriting world canon without a linked world change |
| Agent-system agent | `03-Agent/**` | Changing onboarding/product flow without a linked product change |
| Review agent | PR review comments or `docs/review-notes/*.md` | Editing source files during review |

If a change crosses domains, create one coordination Issue and list each path owner explicitly.

## Issue Status Tokens

Use short comments only:

- `SCOPE_LOCKED: paths <paths>`
- `WORLD_DONE: see <file>`
- `PRODUCT_DONE: see <file>`
- `AGENT_DONE: see <file>`
- `LINK_CHECK_DONE: see PR diff`
- `BLOCKED: <short reason>; see <file or issue>`

## Acceptance Criteria

A content PR is complete when:

- Each changed concept lives in the correct domain folder.
- New terminology is added consistently across linked documents.
- Obsidian links use existing page names or introduce the new page in the same PR.
- `Follow` and `Subscribe` keep their existing meanings from README.
- User-facing copy and internal implementation notes stay clearly separated.
- Long reasoning is stored in files, not GitHub comments.

## Recommended File Additions

Use these only when the change needs them:

```text
docs/review-notes/<issue-number>.md     # reviewer findings without comment bloat
02-Product/<feature>.md                 # product-facing flow or system behavior
03-Agent/<agent-feature>.md             # agent entry or Linker mechanics
01-World/<canon-topic>.md               # world rule or lore canon
```
