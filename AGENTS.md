# AGENTS.md — UniCORE.GVB

**Read this first, every time, before touching this repo.**

---

## What this repo is

`bryanunitek/UniCORE.GVB` — the public canonical home of UniCORE.GVB, the substrate-services layer of UniCORE. The Global Virtual Bridge. Today it holds documentation, the licence, the industry classifications, and the roadmap. **Source code is not yet published here** — it arrives when UniCORE.GVB is certified Powered by UniCORE AI / built on the TrueAI Foundation. See `ROADMAP.md`.

Sister repos:
- `bryanunitek/UniVERSE` — the civilisational-scale programme
- `bryanunitek/TrueAI` — the immutable Foundation (Nine Invariants)
- `bryanunitek/UniCORE-AI` — the 12-Level reference architecture
- `bryanunitek/UniCORE` — the implementation reference (sister to this repo)
- `bryanunitek/UniCORE.GVB-Claw` — the working private repo whose contents become public on certification, distributed across this repository and the industry-classified siblings

Industry-classified siblings (do not exist yet — created at certification):
- `bryanunitek/UniCORE.GVB.Law`
- `bryanunitek/UniCORE.GVB.Accounting`
- `bryanunitek/UniCORE.GVB.Banking`
- `bryanunitek/UniCORE.GVB.Healthcare`
- `bryanunitek/UniCORE.GVB.Government`
- `bryanunitek/UniCORE.GVB.Space-Industry`
- (industry list is open; new classifications added as the programme expands; Military intentionally absent per the UniCORE Positioning Principle)

When Bryan says "UniCORE.GVB" referring to a repo, he means **this repo only** unless he names a specific industry classification.

## Who pushes

**I push directly.** Commit and `git push origin main` on Bryan's behalf. No GitHub Desktop, no approval loop. Same standing rule as the Foundation triad and the UniCORE repo.

The working repos with the GitHub-Desktop-by-default rule are the private Claw repositories. `UniCORE.GVB-Claw` (private) is the working sibling of this repo and follows the GitHub-Desktop-by-default rule there. **This public repo does not.**

## Branching

- **One branch: `main`.** Never create feature branches. Never create dev branches.
- Never open pull requests. Direct commits to `main`.

## Commit style

- Author: `bryanunitek <bryan.fred@unitek-systems.com>` (use `--author=` when committing).
- Message format: `<type>: <subject line>` then blank line, then body. Types: `docs`, `governance`, `roadmap`, `industry`, `chore`.
- Body lists the files added/changed and the "what / why" in two or three sentences.

## Layout (current — pre-certification)

| Path | Purpose |
|---|---|
| `README.md` | Repo overview, the substrate-services scope, industry classifications, certification trigger |
| `LICENSE.md` | CC BY 4.0 / gift licence, mirroring the triad |
| `AGENTS.md` | This file — rules for Claws working on this repo |
| `AI-AUTHORSHIP.md` | AI-assistance disclosure under TrueAI governance |
| `ROADMAP.md` | What arrives at certification and in what shape |
| `STATEMENT-ON-CLAIMS.md` | Names / marks / claims rules for "UniCORE.GVB" and the industry-classified names |

Do not invent new top-level files or directories without asking.

## Layout (post-certification — anticipated)

At certification, the contents of `UniCORE.GVB-Claw` are extracted and published across this repository and each industry-classified sibling repository. Anticipated additions at that point:
- `src/` or top-level `.csproj`-bearing directories — the substrate-services code
- `docs/` — architecture, deployment, industry-classification specifications
- `INDUSTRY-CLASSIFICATIONS.md` — formal index of the open list and how new classifications are added
- `IRREVOCABLE-LICENCE-DECLARATION.md` — irrevocability declaration (mirror or reference)
- `BRAND-AND-TRADEMARK-USE-POLICY.md` — names + marks rules (mirror or reference)
- `DISCUSSIONS.md` — Discussions tab purpose statement
- `SUCCESSION.md` — stewardship reference

The shape locks at certification, not before.

## Attribution rules (durable)

- **Authorship / licence / legal entity:** Unitek Systems Limited (UK) as the present custodian of the gift layer; specific IP-custodian subsidiary within the Unitek Group recorded in the canonical [`UniVERSE/IRREVOCABLE-LICENCE-DECLARATION.md`](https://github.com/bryanunitek/UniVERSE/blob/main/IRREVOCABLE-LICENCE-DECLARATION.md).
- **Licence for all content here:** CC BY 4.0, "given, not sold, irrevocable".
- **Author byline:** `Bryan Fred, Unitek Systems Limited` unless Bryan says otherwise.
- **Version/date:** include version + month-year on any substantive document.

## Contact rules (durable)

Two tiers, and only these two:

- **Public discussion** → GitHub Discussions of the relevant repo
  - UniCORE.GVB: https://github.com/bryanunitek/UniCORE.GVB/discussions
  - UniCORE: https://github.com/bryanunitek/UniCORE/discussions
  - UniVERSE: https://github.com/bryanunitek/UniVERSE/discussions
  - TrueAI: https://github.com/bryanunitek/TrueAI/discussions
  - UniCORE-AI: https://github.com/bryanunitek/UniCORE-AI/discussions
- **Private contact / connection request** → LinkedIn: https://www.linkedin.com/in/bryan-fred-02209753/

**Do not publish** Bryan's personal email, personal phone numbers, or generic Unitek inboxes in any file committed to this repo. Git commit author metadata is the one exception.

## Byline rules (durable)

- **Formal full byline:** `Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom`.
- Use the full formal on `Author:` fields, signoff lines, masthead blocks.
- **Short form** `Bryan Fred, Unitek Systems Limited` is acceptable in running prose only.
- **Never** shorten to "Bryan, Unitek Systems Limited".

## Voice

- Reasoned, not declaratory. Engineering-honest. Avoid manifesto tone.
- This repo's voice is **substrate-architectural** — it explains what services live in GVB, how the industry classifications work, how the substrate is parameterised by the 12-Level Governance Model, why the industry list is open and why Military is absent.
- Cross-reference the canonical statements in the Foundation triad rather than repeating them in full here.

## UniCORE Positioning Principle (DURABLE)

The programme is positioned as **Harmony, Peace, Space Exploration, for Humanity**. Industry classifications must align. **Military uses are intentionally absent** and will not be added.

When drafting any material in this repo:
- Frame industry classifications around the programme's stated positioning.
- Do not write copy that implies Military, dual-use, or weapons-class deployment.
- If asked to add a classification, check it against the positioning principle before drafting.

## Do not

- Do not publish source code in this repo before UniCORE.GVB is certified.
- Do not create the industry-classified sibling repos before certification.
- Do not create branches, open PRs, or introduce a dev workflow.
- Do not mix material from `UniCORE.GVB-Claw` (working private repo) into this public repo before certification.
- Do not contradict the canonical statements in the Foundation triad. If something here would contradict the canonical, fix this repo or raise the contradiction.

## After push

Tell Bryan the commit hash and what changed in one or two sentences. That's the handshake.
