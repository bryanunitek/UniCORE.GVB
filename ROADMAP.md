---
title: "UniCORE.GVB — Roadmap"
author: Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
version: "Version 1.0 · May 2026"
status: v1.0 (DRAFT v0.01)
licence: CC BY 4.0
---

# UniCORE.GVB — Roadmap

**What arrives here, when, under what trigger condition, and how the industry classifications are sequenced.**

---

## Status today

This repository holds the canonical public identity of UniCORE.GVB — the substrate-services layer of UniCORE. The licence, the substrate-services scope, the industry classifications, the certification trigger, and the naming rules. **Source code is not yet published.**

The implementation work is being done in the private working repository `bryanunitek/UniCORE.GVB-Claw`. Source code becomes public on certification, not before.

---

## The certification trigger

The trigger that moves UniCORE.GVB from documentation-only to documentation-plus-code is:

> UniCORE.GVB is **certified Powered by UniCORE AI / built on the TrueAI Foundation**.

When that certification is recorded, the contents of `UniCORE.GVB-Claw` are extracted and published. They are distributed as follows:

- The **industry-agnostic substrate-services code** is published in this repository (`bryanunitek/UniCORE.GVB`) under CC BY 4.0.
- The **industry-classified releases** (`bryanunitek/UniCORE.GVB.Law`, `bryanunitek/UniCORE.GVB.Accounting`, `bryanunitek/UniCORE.GVB.Banking`, `bryanunitek/UniCORE.GVB.Healthcare`, `bryanunitek/UniCORE.GVB.Government`, `bryanunitek/UniCORE.GVB.Space-Industry`, etc.) are created and published at the same time, under CC BY 4.0, each carrying the same substrate parameterised by the 12-Level Governance Model for the industry it serves.

The same code runs in every classification. The classification token determines the governance parameters applied through the 12-Level model.

The certification gate is not a marketing milestone. It is a quality threshold. The badge ("Powered by UniCORE AI / built on the TrueAI Foundation") is a claim about Foundation conformance. Source code arriving here before that claim is earned would dilute the badge.

---

## Industry classifications — open list

The industry list is **open**. New classifications are added as the programme expands.

The current list is:

| Classification | Industry served |
|---|---|
| `UniCORE.GVB.Law` | Law firms — global and regional |
| `UniCORE.GVB.Accounting` | Accounting firms |
| `UniCORE.GVB.Banking` | Banking |
| `UniCORE.GVB.Healthcare` | Healthcare |
| `UniCORE.GVB.Government` | Government and public sector |
| `UniCORE.GVB.Space-Industry` | Space industry — Harmony, Peace, Space Exploration, for Humanity |

The list is defined as the programme expands. **Military is intentionally absent and will not be added.** The UniCORE Positioning Principle is Harmony, Peace, Space Exploration, for Humanity — see [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md).

A new classification is added when:
1. A Vertical CORE for that industry exists or is in active development.
2. The classification aligns with the UniCORE Positioning Principle.
3. The 12-Level Governance Model parameters for that classification have been authored.

Adding a classification creates a new `UniCORE.GVB.<Industry>` repository at certification time, peer to the existing classifications, all CC BY 4.0.

---

## What arrives at certification

When UniCORE.GVB is certified, this repository receives:

### Source code (industry-agnostic)
- The substrate-services source code extracted from `UniCORE.GVB-Claw` — the industry-agnostic layer.
- The build files (`.sln`, `.csproj`, `Directory.Packages.props`, `Directory.Build.props`) that compile the substrate.
- Tests for the substrate.

### Documentation
- `docs/` — full architecture: substrate-services, tenancy, topology, federation, mail/file/DNS/FTP, integration points, conformance claims.
- `INDUSTRY-CLASSIFICATIONS.md` — formal index of how classifications are added and which 12-Level parameter sets each one uses.
- `IRREVOCABLE-LICENCE-DECLARATION.md` — formal irrevocability (mirror of, or reference to, the canonical UniVERSE declaration).
- `BRAND-AND-TRADEMARK-USE-POLICY.md` — names + marks rules.
- `DISCUSSIONS.md` — purpose of the GitHub Discussions tab.
- `SUCCESSION.md` — stewardship reference.

### Industry-classified sibling repositories
- `bryanunitek/UniCORE.GVB.Law` and the rest of the classifications, created at the certification moment, each carrying the same substrate code with the industry-specific parameterisation.

---

## What does NOT arrive at certification

- **Vertical CORE Business Objects** stay in their own Vertical CORE repositories (`UniCORE.Law-Claw`, future `UniCORE.Accounting-Claw`, etc.). The substrate-services live here; the industry-specific Business Objects do not.
- **Hosted-service operational state** stays with whoever operates the service. UniCORE.GVB is the substrate-services code. Unitek Systems USA Inc, when it operates a UniCORE.GVB-based hosted service, does so as one consumer of this gift among many — under the same CC BY 4.0 licence as everyone else. The operational state of any specific hosted service is not part of the gift surface.
- **Working-state churn** stays in the private `UniCORE.GVB-Claw` repository.

---

## How Unitek Systems USA Inc relates to this gift

Unitek Systems USA Inc may operate hosted services on top of UniCORE.GVB. When it does, it does so as **one consumer of the gift among many**, under the same CC BY 4.0 licence as anyone else. There is no privileged operator tier. The commercial position of Unitek Systems USA Inc sits in:

- The hosted **service** (the running infrastructure, the SLAs, the support).
- The **Vertical CORE Business Objects** kept in the relevant Vertical CORE working repositories (Law BOs in `UniCORE.Law-Claw`, future Accounting BOs in `UniCORE.Accounting-Claw`, etc.).
- **Professional services, integration, and customisation** offered to clients.

The gift surface is uniform. Anyone in the world may take published UniCORE.GVB and an industry-classified release and stand up their own deployment. That is the point of the gift.

---

## Sequence of certification

1. **Build** — `UniCORE.GVB-Claw` is built privately to the level the Foundation invariants and the substrate-services scope require.
2. **Self-assessment** — the Generation IT producer pair self-assesses against the Nine Invariants and the 12-Level reference architecture, including the parameterisation for each in-scope industry classification.
3. **Solution Review** — independent Solution Review by a [Certified Expert](https://github.com/bryanunitek/UniVERSE/blob/main/CERTIFIED-EXPERTS.md).
4. **Certification recorded** — the Solution Review outcome is recorded; the certification claim becomes valid.
5. **Public publication** — the substrate-services source is extracted and published across this repository AND the industry-classified sibling repositories simultaneously.

The exact procedural detail is governed by the canonical material in [`UniVERSE/docs/10002-Certification-Before-Layered-Governance.md`](https://github.com/bryanunitek/UniVERSE/blob/main/docs/10002-Certification-Before-Layered-Governance.md) and [`UniVERSE/docs/00059-Solution-Review.md`](https://github.com/bryanunitek/UniVERSE/blob/main/docs/00059-Solution-Review.md).

---

## Why DRAFT v0.01 today

The programme as a whole is in DRAFT v0.01. Versioning across the public repositories does not turn on until the first GitHub Discussion is opened in any of the public programme repositories — see [`UniVERSE/HORIZON.md`](https://github.com/bryanunitek/UniVERSE/blob/main/HORIZON.md) for the canonical statement.

This repository inherits that posture. The `Version: 1.0` line is a placeholder.

---

## Time horizon

The same horizon that applies to the wider programme applies here. UniCORE.GVB source publication depends on the certification arc; the certification arc takes as long as it takes to build the substrate-services to the standard the invariants require. That is decade-shaped work.

For the canonical horizon statement, see [`UniVERSE/HORIZON.md`](https://github.com/bryanunitek/UniVERSE/blob/main/HORIZON.md).

---

## What readers can do today

- **Cite the architecture** — the position of UniCORE.GVB as the substrate-services layer, the open industry list, and the certification trigger, are public and citable now.
- **Read the canonical material** — the Foundation triad ([UniVERSE](https://github.com/bryanunitek/UniVERSE), [TrueAI](https://github.com/bryanunitek/TrueAI), [UniCORE-AI](https://github.com/bryanunitek/UniCORE-AI)) is fully published.
- **Build their own substrate-services** under CC BY 4.0 — the architecture is open. Independent producers building Foundation-aligned substrate-services for verticals not yet covered by the official industry list are exactly what the gift principle exists to enable.
- **Discuss** — open a thread on this repository's [Discussions tab](https://github.com/bryanunitek/UniCORE.GVB/discussions) when adoption, architectural critique, industry-classification proposals, or translation work has begun.

---

## Versioning of this document

| Version | Date | Notes |
|---|---|---|
| v1.0 | May 2026 | First publication. Repository created public; certification trigger recorded; source code held until UniCORE.GVB certification; industry-classified sibling repositories created at certification time. |

Revisions tracked in git history.

---

## Contact

- **Public discussion:** [GitHub Discussions](https://github.com/bryanunitek/UniCORE.GVB/discussions)
- **Private contact / connection request:** [LinkedIn](https://www.linkedin.com/in/bryan-fred-02209753/)

— Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom, May 2026.
