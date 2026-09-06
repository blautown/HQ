# Claude Code's response: roles between GPT and Claude Code in Jy-ops HQ

**Status:** Response to `claude-code-proposal.md` §8 ("Proposed adoption"). The proposal is adopted; this file is the counter-proposal on how GPT and Claude Code should divide labour and hand off work going forward, so the founder isn't the only thing keeping two AI systems from working at cross purposes.

## Why this needs writing down

GPT and Claude Code have no direct channel to each other. Every proposal, edit, and correction passes through the founder relaying text between two sessions. That already produced one real failure mode in this repo: GPT rewrote `map.md` to the new asset model while Claude Code was still holding an older read of the same file, and an edit attempt bounced because the file had changed on disk since it was last read. That's a survivable, self-correcting failure — but only because the tooling caught it. The roles below exist to make that the exception, not the normal way work gets reconciled.

The repo — not either model's running context, and not this file — is the source of truth. Whatever `git diff` and the actual file contents say is what happened; a proposal or a status report describes an *intent*, and is only confirmed once someone actually re-reads the changed file.

## Division of responsibilities

### GPT — architecture and drafting

GPT is the better fit for:

- proposing changes to the asset model or the operating architecture (the identity/operational-guidelines/plugin split is a GPT proposal, adopted after review);
- drafting new conceptual documents from first principles (`claude-code-proposal.md`, `benchmark.md`);
- broad-strokes rewrites across many files at once when a model changes and prose needs to move in the same direction everywhere.

GPT should not treat a broad rewrite as finished the moment it's internally coherent. A rewrite that touches five files but only actually lands in two of them (as happened with `README.md`'s "How to add" section) is incomplete, not done — the previous exchange is the concrete example.

### Claude Code — verification and execution

Claude Code is the better fit for:

- reading the actual current state of the repo (not a remembered version of it) before every edit;
- running the mechanical integrity checks: `git diff`, `git diff --check`, confirming links and referenced files exist, checking mermaid syntax and node/edge consistency, running the project linter;
- catching cross-file contradictions a broad rewrite leaves behind — stale terminology, a diagram whose prose caption no longer matches its edge count, a section that got missed;
- making small, targeted, reviewable edits once a specific fix is agreed, rather than re-drafting whole files;
- distinguishing a structural contradiction (the asset model described two different ways in two files) from a cosmetic one (a heading still says "DK:0" as a label) — and saying explicitly which kind a finding is, so triage is fast instead of everything reading as equally urgent.

Claude Code should not fold a GPT proposal into `CLAUDE.md` or another canonical document as "adopted" on its own judgment. That call belongs to the founder — Claude Code's job is to surface what adopting it would require (which files go stale, what has to be reconciled) so the founder can decide with full information, then execute the decision once made.

### Founder — the only approver of model-level change

Neither AI system should treat a proposal as adopted, or a reconciliation as complete, without the founder saying so. Both systems can and should disagree with each other in their reports to the founder — that disagreement is useful signal, not a problem to hide. Neither should soften a finding to make a handoff look cleaner than it is.

## Handoff protocol

This is the pattern that already worked in this session; writing it down so it repeats on purpose instead of by luck:

1. GPT (or Claude Code) proposes a change and states what it would touch.
2. The founder relays the proposal to the other system for review before treating it as adopted.
3. The reviewing system reads current file state (never a cached view) and reports: what's consistent, what conflicts, what's missing — separating real contradictions from cosmetic ones.
4. The founder decides: adopt, adopt with changes, or hold.
5. Whoever proposed or executed the change does not write "adopted" into that change's own status line. The status line records the founder's decision and says so explicitly (e.g. "Adopted by founder decision") — never a bare "Adopted," which reads as the proposing system certifying itself. `claude-code-proposal.md`'s status line was fixed to this standard after shipping without it.
6. Whoever is executing makes the edit, then the other system verifies the actual diff — not the description of the diff — before either side calls it done.
7. `TASKS.md` only gets a change marked `[x]` once step 6's verification has actually passed, not when the drafting pass finishes.

## Project intake and roadmap verification

The handoff protocol above governs changes to HQ's own architecture and canonical documents. An incoming client project follows a related but separate pipeline, because the thing being verified is a roadmap's fit against the source of truth, not a documentation edit:

```text
Founder scopes the project as one roadmap in Linear
        ↓
Roadmap is relayed into HQ for verification — as a whole, before any task exists
        ↓
GPT and Claude Code check the whole roadmap for logic, scope, and fit against
workspace.md, map.md, dk0/domain-knowledge-boundaries.md, offer.md, and claims.md
        ↓
Founder decides: approve, approve with changes, or hold
        ↓
Only an approved roadmap gets split into smaller tasks
        ↓
Tasks are packaged back onto Linear for execution tracking
```

The verification gate applies to the roadmap as a whole, once, before it is split — not task by task after packaging. Checking each small task in isolation lets a scope or logic problem slip through piecemeal, because no single task shows the shape of the whole plan; the roadmap-level check is what catches a project that quietly asks for something outside DK:0/DK:1 boundaries, contradicts an existing asset, or promises something `offer.md`/`claims.md` doesn't back. Once a roadmap has passed this gate, splitting it into tasks is packaging, not re-litigating scope — the individual tasks inherit the verified scope and don't each need their own architecture review, though the normal execution-time check (verify the actual diff/output before calling a task done) still applies to each one when it's completed.

Linear holds the roadmap before verification and the tasks after packaging. It never holds the verification step itself — that only happens where the source-of-truth documents actually live.

## Shared rules

- Re-read a file immediately before editing it. Do not edit from a memory of its content once any other editor could plausibly have touched it — this repo now has more than one active editor.
- "Reconciled" or "done" means every file that was supposed to change was actually checked, not just the ones that were top-of-mind. Spot-checking the sections you edited and skipping the rest is how the `README.md` leftover happened.
- Report findings ranked by severity: a place where two documents assert different facts about the same mechanism outranks a stale label or heading.
- Neither system invents what the other one is thinking. If GPT's intent behind a phrase is unclear, ask the founder to relay a clarification rather than guessing at it and drafting around the guess.

## Where this lives

Linked from `README.md` and `CLAUDE.md`'s navigation alongside `claude-code-proposal.md` and `benchmark.md`.
