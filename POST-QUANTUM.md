# UniCORE.GVB — Post-Quantum Cryptography Posture

*Status: DRAFT v0.01 · substrate-services layer · public gift surface (CC BY 4.0)*

Sister documents: [ROADMAP.md](ROADMAP.md) · [REGULATORY-ALIGNMENT.md](REGULATORY-ALIGNMENT.md) · [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md)

---

## Why this document exists

Advanced AI runs on infrastructure, and that infrastructure runs on cryptography. A large-scale quantum computer would break the public-key cryptography (RSA, elliptic-curve) that today protects almost every encrypted connection and digital signature on the internet. The symmetric ciphers that protect data at rest (AES-256) are largely unaffected; the public-key layer is not.

UniCORE.GVB is the substrate on which governed Vertical Solutions run. Some of those Solutions — law firms, and the evidence-bound, decision-critical work UniCORE exists to serve — produce records that must remain trustworthy for **decades**, potentially defensible in a courtroom long after they were created. That long lifetime is what makes the quantum question urgent *now*, not at some future deadline.

This document states plainly: **what is coming, what UniCORE.GVB does about it today, the roadmap, and the timeline.** It follows the same honesty discipline as the rest of this repository — where something is not built yet, it says so.

---

## What is coming — the threat, in plain terms

A **cryptographically-relevant quantum computer (CRQC)** does not exist today. When one does, it would be able to:

- **Break public-key key exchange** (RSA, ECDH) — the mechanism that negotiates the secret keys protecting a TLS/HTTPS connection.
- **Forge public-key digital signatures** (RSA, ECDSA, EdDSA) — the mechanism that proves a certificate, a document, or a record is authentic and unaltered.

Two consequences matter for a substrate like GVB:

1. **"Harvest now, decrypt later" (HNDL).** An adversary can record encrypted traffic *today* and simply store it until a CRQC exists, then decrypt it retroactively. This means the protection deadline for any *long-lived confidential data* is not the arrival of the quantum computer — it is **now**. Anything sensitive we transmit today under classical-only key exchange is already exposed to a patient adversary.

2. **Signature forgeability breaks long-lived records.** A signature that is unforgeable today becomes forgeable once a CRQC exists. For records whose entire value is that they are demonstrably authentic and unaltered years later — evidence chains, provenance records, ratification trails — a classical signature is a time-limited guarantee. This is the sharpest risk for UniCORE specifically, because the integrity of the record *is* the product.

### The standards that answer it

In **August 2024**, the U.S. National Institute of Standards and Technology (NIST) finalised the first post-quantum cryptography (PQC) standards:

| Standard | Algorithm | Purpose |
|---|---|---|
| **FIPS 203** | ML-KEM (formerly CRYSTALS-Kyber) | Key encapsulation — replaces RSA/ECDH key exchange in TLS |
| **FIPS 204** | ML-DSA (formerly CRYSTALS-Dilithium) | Digital signatures — general-purpose |
| **FIPS 205** | SLH-DSA (formerly SPHINCS+) | Digital signatures — hash-based, conservative |
| **FIPS 206** | FN-DSA (Falcon) | Digital signatures — in development |

NIST's published migration guidance is to **begin transitioning away from RSA and elliptic-curve cryptography before 2030, and to disallow them by 2035**. Major browser and platform vendors (including Google/Chrome) are already deploying **hybrid** key exchange — classical plus post-quantum together — with deprecation of classical-only key exchange signalled for the **2029–2030** window.

These dates are industry and government targets for *tooling*. The data-protection deadline for anything sensitive-and-long-lived, because of HNDL, is earlier — effectively immediate.

---

## What UniCORE.GVB does today — honest status

GVB's public front door terminates TLS with a standards-current, auto-renewing certificate and modern TLS 1.3 cipher suites. Symmetric data-at-rest protection uses AES-256, which is already considered quantum-resistant at the relevant security level.

String (NVARCHAR) data across the substrate is governed by the four-mode **NVarchar Data Mode** posture — **Scrambled** (default) / **Open** / **Encrypted** (reserved) / **Quancrypted** (reserved). **Quancrypted** is the data-at-rest quantum-safe end-state: the same field-level encryption as Encrypted, but with post-quantum key protection (ML-KEM / FIPS 203 key encapsulation), so a harvested field cannot be decrypted later by a quantum computer. Today, fields can be *tagged* for Encrypted/Quancrypted and the persistence seam carries the mode, but the cryptographic implementations of those two modes are **not yet shipped**.

**What is NOT yet done, stated plainly:**

- Hybrid post-quantum **key exchange** (X25519 + ML-KEM) is **not yet enabled** on the public TLS front door. It is deployable in the current reverse-proxy stack and is the first concrete migration step.
- A **post-quantum signature path** for the internal certificate authority and, most importantly, for **long-lived record signatures** (evidence, provenance, ratification) is **not yet built**. It is the highest-priority item on the roadmap below.
- No production traffic or record is currently PQC-protected. Anyone reading this should understand the posture as *designed and roadmapped*, not *shipped*.

This honesty is deliberate. Claiming "quantum-safe" before it is true would be exactly the kind of unfounded claim UniCORE exists to make impossible.

---

## Migration priority order — why signatures come first

Most quantum-migration guidance leads with TLS. For UniCORE, the order is deliberately different, because of what UniCORE *is*:

1. **Long-lived record signatures (highest priority).** The integrity of the governed record is the whole point of a UniCORE Solution. Any signature that must remain unforgeable for years must move to a post-quantum signature scheme (ML-DSA / SLH-DSA), or a hybrid classical+PQC signature, as early as possible. A forgeable historical record is a broken product.

2. **Public TLS key exchange (HNDL surface).** Move the public front door to hybrid key exchange (X25519 + ML-KEM) so that traffic recorded today cannot be decrypted later. Near-term, config-and-version driven.

3. **The certificate authority itself.** Where GVB operates an internal CA for service identity, design its signing path to be post-quantum-capable rather than retrofit it later.

4. **Transport/administrative keys (SSH and equivalents).** Move to post-quantum-hybrid key exchange when convenient. Lower urgency — short-lived sessions are not the decades-long HNDL target.

**Principle across all four: hybrid first, not pure post-quantum.** Combining a classical algorithm with a post-quantum one means the result is no weaker than today even if a young post-quantum algorithm is later found wanting, while still defeating "harvest now, decrypt later." This mirrors the posture of major platform vendors.

---

## Roadmap

The build is phased and gated. Each phase is honest about being design, build, or shipped.

| Phase | Scope | State |
|---|---|---|
| **P0 — Posture (this document)** | State the threat, standards, priority, timeline publicly and in the canonical record | **This document** |
| **P1 — Long-lived signature seam** | Define a signature abstraction for evidence/provenance/ratification records that can carry classical, hybrid, or post-quantum signatures without changing the record model | Designed / building |
| **P2 — Hybrid TLS front door** | Enable X25519 + ML-KEM hybrid key exchange on the public reverse proxy | Ready to build (config/version) |
| **P3 — PQC-capable CA** | Stand up / configure the internal certificate authority with a post-quantum signature path | Design |
| **P4 — Quancrypted data-at-rest** | ML-KEM key protection on the `Quancrypted` NVarchar mode (Encrypted/classical-wrap as interim) | Mode declared, crypto not shipped |
| **P5 — Transport keys** | Post-quantum-hybrid key exchange for administrative/SSH access | Later |
| **P6 — Verify & attest** | Independent verification that shipped PQC matches the posture, recorded in the canonical evidence chain | Later |

Nothing above is claimed as shipped except P0.

---

## Timeline

Anchored to the published NIST and industry clock, not to internal optimism.

- **Now (immediate):** HNDL means the *risk* is present today. P0 posture published. P1 (long-lived signature seam) prioritised because record integrity has the longest lifetime and the least tolerance for retroactive forgery.
- **Near term:** P2 hybrid TLS enabled on the public front door, following the same hybrid posture browser vendors already ship.
- **Before 2030:** substrate-wide transition away from classical-only public-key cryptography, in step with NIST's "begin before 2030" guidance and the industry ~2029–2030 classical-KEX deprecation window.
- **By 2035:** classical-only RSA/ECC fully retired from the substrate, in step with NIST's "disallow by 2035" guidance.

The programme deliberately moves ahead of the tooling deadlines for the surfaces where data lifetime is longest — because for a courtroom-grade record, the deadline is set by how long the record must last, not by when the tools deprecate.

---

## What readers can do today

- **Producers building on GVB:** design record and document formats so the *signature algorithm is a replaceable field*, not a hard-coded assumption. A record model that can carry a post-quantum signature tomorrow without a schema change is the single most valuable thing you can do now.
- **Anyone transmitting long-lived confidential data:** treat "harvest now, decrypt later" as a present risk and prefer hybrid post-quantum key exchange wherever your stack supports it.
- **Reviewers:** hold this document to its own honesty rule. If a future version claims "quantum-safe," check it against shipped, verified code — not against this roadmap.

---

*This document is part of the UniCORE public gift surface, given under CC BY 4.0. It is a posture and roadmap, not a claim of completed protection. Where it describes future work, that work is not yet shipped.*

*Time horizon: this is a decades-long substrate. The quantum transition is one chapter of that horizon, sequenced against a clock that is now public and shared across the whole industry.*

---

## Document history

- 2026-07-01 (ea6bcce) — Add POST-QUANTUM.md: PQC posture, roadmap & timeline (public gift surface)
- 2026-07-01 (a5ebc5e) — Add Quancrypted as 4th NVarchar Data Mode (PQC data-at-rest end-state)

*Back-filled from git log on 2026-07-10 21:34 UTC. Kind 2 versioning (dated change notes) — see HORIZON.md § Evolution and versioning. Kind 1 (formal `Version:` bumps) remains OFF until first GitHub Discussion.*
