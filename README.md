# Gary Davidson

**Repeatable, verifiable AI-assisted software engineering.** I build software with AI agents under
engineering discipline — specs before code, gates that can refuse, review layers that catch what the
previous layer missed — and I publish the receipts so the claims can be checked rather than taken on
faith. Every repo below runs its own tests in CI; the numbers in each README are the numbers the
badge proves.

## How I work

1. **Verification, not trust.** A completion claim carries evidence or it isn't a completion claim —
   commit SHA if code changed, test command and exit code if tests ran. Schemas enforce it, because
   *prose drifts, schemas don't.*
2. **Claims corroborated by commits.** Execution reports are assembled from the run journal and
   `git log`; nothing is asserted without a commit to point at.
3. **Test against your own confirmation bias.** Hand-authored expectations are written by the same
   person who wrote the code, so they get checked by differential tests against independent
   implementations and property-based invariants. That layering surfaces real bugs.
4. **Gates that can refuse.** Plan validation returns FAIL and execution stops; only an explicit
   human override proceeds, and the override goes in the report. AI is a force multiplier for
   engineering judgment, not a substitute for it.
5. **Regenerate over patch.** When a codebase is bad enough, capture its behavior in tests, then
   rebuild clean-room from that specification instead of patching around the defects.

## Published work

**Verifiable delivery** · [opening-dojo](https://github.com/garyld1962/opening-dojo) — a chess
opening trainer built end-to-end by a multi-agent pipeline, with the PRD, plan, parallel agent lanes,
five review passes, traceability matrix, and postmortem all committed. 86 tests in CI.

**Regenerate-don't-patch** · [gorules](https://github.com/garyld1962/gorules) →
[rustrules](https://github.com/garyld1962/rustrules) — a 2016 Go rules engine audited by four AI
specialists (37 findings), test-rehabbed 29→124 to pin down real behavior, then regenerated
clean-room in Rust: 12+ bugs fixed, 15 operators added. 124 and 121 tests in CI.

**Applications** · [the-strand](https://github.com/garyld1962/the-strand) — a Go literary-analysis
engine with a provenance-linked pipeline, deterministic replay providers, and release gates ·
[tonewise](https://github.com/garyld1962/tonewise) — a native iOS ear trainer teaching relative pitch
numerically, 93 tests over the domain engines.

More publishing as it clears review — MCP servers, evaluation harnesses, and the methodology skill
library behind the workflow above.

## Lab

Work runs on a five-machine homelab: a Ryzen 9950X3D / RTX 5090 workstation for local inference and
agent runs, an Apple Silicon node for always-on inference, and an Ubuntu server for reverse proxy,
monitoring, and storage — with local LLM serving, vector search, and speech-to-text self-hosted.

📍 Boone, NC · [savviety.ai](https://savviety.ai/)
