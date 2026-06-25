# AI Compliance

**What this document covers:** the UniCORE.GVB AI compliance infrastructure — the architectural posture, the EU AI Act Annex III alignment, and the governance primitives for the Global Virtual Bridge substrate-services layer.

**What this document does not cover:** Vertical CORE-specific AI regulatory filings, jurisdiction-specific AI compliance business processes, or AI compliance for workloads running on the GVB infrastructure. Those are the responsibility of the Vertical CORE running on GVB and its operating jurisdiction.

---

## Status

This document describes the **Tier-3 AI Compliance** infrastructure as implemented in the UniCORE.GVB substrate-services layer. The EU AI Act service modules (Articles 11, 12, 13, 14, 15, 17, 72, and Annex IV technical documentation) are provided by the UniCORE substrate that underpins the GVB layer.

The 2026-08-02 date for Annex III §8(a) obligations is noted below.

---

## GVB AI compliance model

UniCORE.GVB is a **substrate-services layer** — it provides infrastructure services (mail, file transfer, DNS, federation, tenancy, node operations) to Vertical Solutions running on top of it. AI compliance obligations for AI systems operating within those Vertical Solutions are the responsibility of the Vertical CORE producer.

However, the UniCORE.GVB substrate itself incorporates the UniCORE governance primitives, which include the Nine Invariants and the badge certification infrastructure. A Vertical Solution running on GVB that also incorporates the UniCORE substrate inherits the full AI compliance service suite.

### Two-layer model

| Layer | Owner | AI compliance responsibility |
|---|---|---|
| **UniCORE.GVB substrate-services** | Unitek Systems USA Inc | Infrastructure posture; GVB-level badge and governance; no AI decision-making |
| **Vertical CORE on GVB** (e.g. UniCORE.Law) | Vertical CORE producer | Full EU AI Act compliance for the AI system; Annex III obligations |

GVB's substrate-services do not themselves constitute an AI system under the EU AI Act. The AI systems that engage Annex III obligations are the Vertical Solutions running on GVB.

---

## EU AI Act context

The EU AI Act classifies AI systems used in **law firms and legal practice** as **high-risk** under **Annex III §8(a)**. Any Vertical CORE built on UniCORE and deployed on GVB that supports legal practice is subject to Annex III §8(a) from **2026-08-02**.

The GVB layer does not provide AI compliance services directly — it provides the infrastructure on which a compliant Vertical CORE can run. Vertical CORE producers who deploy on GVB are responsible for ensuring their AI systems are compliant with the obligations that apply to their specific use case and jurisdiction.

---

## The badge certification on GVB

UniCORE.GVB implements its own badge certification check (`IBadgeConformanceCheck` in the `UniCORE.GVB.Governance` namespace), separate from the UniCORE substrate layer. This is the GVB layer's own attestation surface.

The GVB badge check verifies:

1. **AttributionService wired** — `ITrueAiAttributionService` is resolvable in DI.
2. **Canonical tagline match** — attribution text contains "UniCORE" before "TrueAI" in the sanctioned forms.
3. **About info populated** — `IGvbAboutInfoService` surfaces ProductName, Version, Copyright, HostingEntity.
4. **Compile-time floor active** — `UniCoreGvbClawCompileTimeFloor` is present in the loaded assembly set.
5. **Programme description published** — the about info references the Nine Invariants and governance context.

A GVB deployment that passes all five criteria can assert:

> Powered by UniCORE AI · Built on the TrueAI Foundation

This badge claim is distinct from — and composes with — the badge claim of a Vertical CORE running on GVB.

---

## Relationship to the UniCORE substrate

UniCORE.GVB is built on the UniCORE substrate. The AI compliance service modules (Articles 11, 12, 13, 14, 15, 17, 72, Annex IV) are part of the UniCORE substrate and are available to any Vertical CORE that incorporates UniCORE.

A Vertical CORE that incorporates UniCORE and runs on GVB gets:

- The GVB infrastructure services (mail, file, DNS, federation, etc.)
- The UniCORE governance primitives (Nine Invariants, compile-time floor)
- The UniCORE AI compliance service modules (Articles 11–17, 72, Annex IV)
- The GVB badge certification infrastructure

This means the full EU AI Act compliance posture for a Vertical CORE on GVB is a composition of the GVB layer's badge check and the UniCORE substrate's AI compliance modules.

---

## GVB-specific governance

### Infrastructure sovereignty

GVB is a private cloud infrastructure operated by Unitek Systems USA Inc. The infrastructure is not a shared multi-tenant environment — each GVB deployment is isolated. This isolation is reflected in the Nine Invariants' infrastructure-sovereignty rule.

### Node federation

GVB nodes are federated across geographic regions (LA, NJ, UK; Phase II Geneva planned). Cross-region communication uses the UniCORE federation protocol. The badge handshake (runtime attestation that both sides of a connection carry the badge) applies to all cross-node communication.

### Breach notification

The GVB infrastructure maintains its own breach notification obligations under applicable data protection law. The UniCORE.GVB substrate does not implement breach notification for Vertical CORE data — that is the Vertical CORE producer's responsibility.

---

## Relationship to the Book of Unitek Systems Limited

Operational GVB AI compliance posture and the jurisdictional position for GVB deployments are documented in the Book of Unitek Systems Limited, Chapter A3, §GVB Infrastructure.

---

## Version

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | First publication. Describes the GVB AI compliance model, badge certification infrastructure, and relationship to the UniCORE substrate. |
