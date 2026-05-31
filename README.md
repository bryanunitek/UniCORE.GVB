UniCORE is the public foundation for advanced AI.

We design the governance, write the code, and train the people who can do both. The foundation is gifted to humanity under permissive licences. The producers who maintain it earn their authority through a 30-year apprenticeship: not bought, not granted, earned.

The result is infrastructure no single company can monopolise, built and maintained by people from every background.

The future is coming. Advanced AI will shape the world ahead, whether we are ready or not. The question is who builds it, who controls it, and who benefits. UniCORE answers all three the same way: humanity does.

If you want to spend a career building advanced AI for humanity rather than for shareholders, UniCORE is the path.

A 30-year programme from apprentice to certified producer. A public foundation given away under permissive licences. No monopoly. The work belongs to everyone, including you.

---

*This is **UniCORE.GVB**, the substrate-services layer of UniCORE. The Global Virtual Bridge — the production-grade substrate-services that any Vertical Solution may run on. Sister repositories: [UniVERSE](https://github.com/bryanunitek/UniVERSE) (the programme), [TrueAI](https://github.com/bryanunitek/TrueAI) (the immutable Foundation), [UniCORE-AI](https://github.com/bryanunitek/UniCORE-AI) (the 12-level reference architecture), [UniCORE](https://github.com/bryanunitek/UniCORE) (the implementation reference).*

*New to producing on the public gift surface? Start with [UniVERSE/GETTING_STARTED.md](https://github.com/bryanunitek/UniVERSE/blob/main/GETTING_STARTED.md).*

---

# UniCORE.GVB — Global Virtual Bridge

**The substrate-services layer of UniCORE.**

Author: Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom
First published: May 2026
Status: Public. Given, not sold. Irrevocable.

---

## What is UniCORE.GVB?

UniCORE.GVB is the **substrate-services layer** that any Vertical Solution may run on top of: mail, file transfer, secure delivery, DNS, federation, tenancy, topology, FTP, Outlook integration, web disk, calendar/contacts, server profiles, node operations, bandwidth and storage reporting, jurisdictional posture, and inter-node bridging across geographic regions.

It is **one codebase** that is **classified for specific industries** — the same substrate parameterised by the [UniCORE AI 12-Level Governance Model](https://github.com/bryanunitek/UniCORE-AI) for the industry it serves.

Industry classifications (open list, defined as the programme expands):

| Classification | Industry served |
|---|---|
| `UniCORE.GVB.Law` | Law firms — global and regional |
| `UniCORE.GVB.Accounting` | Accounting firms |
| `UniCORE.GVB.Banking` | Banking |
| `UniCORE.GVB.Healthcare` | Healthcare |
| `UniCORE.GVB.Government` | Government and public sector |
| `UniCORE.GVB.Space-Industry` | Space industry — Harmony, Peace, Space Exploration, for Humanity |

The **same code** runs in every classification. The classification token determines the governance parameters applied through the 12-Level model. The industry list is open; new classifications are added as the programme expands. **Military is intentionally absent** — the [UniCORE Positioning Principle](#unicore-positioning-principle) is Harmony, Peace, Space Exploration, for Humanity.

When UniCORE.GVB is **certified Powered by UniCORE AI / built on the TrueAI Foundation**, this repository and every industry-classified repository (`UniCORE.GVB.Law`, `UniCORE.GVB.Accounting`, etc.) is published under CC BY 4.0.

---

## Why this repository exists today

This repository exists today as the **canonical public home** for UniCORE.GVB — the place where its identity, licence, roadmap, naming rules, and industry classifications are recorded.

**The source code is not yet published here.** Source code is published when UniCORE.GVB is certified Powered by UniCORE AI / built on the TrueAI Foundation. See [ROADMAP.md](ROADMAP.md) for the trigger condition and what arrives at that point.

What is published here today:

- **The licence** — CC BY 4.0, irrevocable, the same terms as the rest of the programme. See [LICENSE.md](LICENSE.md).
- **The licensing reference with worked scenarios** — plain-English guidance for Partners, Clients, and Software Providers, with worked examples per industry. See [LICENSE_EXAMPLES.md](LICENSE_EXAMPLES.md).
- **The naming and claims rules** — what can and cannot be claimed about the UniCORE.GVB name. See [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md).
- **The roadmap** — what arrives at certification and in what shape. See [ROADMAP.md](ROADMAP.md).
- **The AI authorship disclosure** — same disclosure form as the Foundation triad. See [AI-AUTHORSHIP.md](AI-AUTHORSHIP.md).
- **The agent rules** — how Claws working on this repository conduct themselves. See [AGENTS.md](AGENTS.md).

The repository will accumulate documentation between now and certification. Source code arrives at certification, simultaneously across this repository and the industry-classified sibling repositories.

---

## The substrate-services scope

UniCORE.GVB provides the production-grade infrastructure that a Vertical Solution needs in order to run as a multi-tenant service across geographic regions, without each Vertical CORE having to re-derive the substrate from scratch.

The scope is comprehensive. It covers every layer from hypervisor to application-services, governed by the 12-Level Governance Model throughout.

### Compute and virtualisation

- **Hypervisor management** — virtual machine lifecycle (create, start, stop, snapshot, clone, live-migrate), resource pools, storage repositories, high-availability clustering, rolling updates
- **VM templates and provisioning** — template library, rapid deployment, cloud-init / unattended configuration, resource allocation policies
- **Host management** — physical host inventory, firmware/BIOS configuration, hardware health monitoring, power management, maintenance mode
- **Storage** — local and shared storage backends, thin provisioning, snapshot management, replication, tiered storage policies
- **Networking (virtual)** — virtual switches, VLANs, SDN integration, network isolation per tenant, bonding, SR-IOV passthrough

### Multi-tenant platform management

- **Tenancy** — tenant provisioning, suspension, termination; cross-tenant boundary guards; governance attestation per tenant
- **Resource quotas and packages** — disk, bandwidth, mailbox, database, and compute quotas; resource packages; overage policies
- **Account lifecycle** — customer-account creation, modification, suspension, transfer between nodes; account-level audit trail
- **Reseller and delegation** — reseller account hierarchy, delegated administration, white-label capability, per-reseller resource limits
- **Billing integration** — usage metering, invoice-period snapshots, integration points for external billing systems

### Mail services

- **SMTP** — outbound and inbound mail transfer, queue management, rate limiting, IP-reputation management, warm-up state machine
- **IMAP and POP3** — mailbox access protocols, folder management, shared mailboxes
- **Mailboxes, aliases, and forwarders** — per-tenant mailbox provisioning, alias routing, auto-responders, catch-all configuration
- **Mailing lists** — list creation, subscription management, moderation, archiving
- **DKIM / SPF / DMARC** — DNS-based email authentication, key rotation, policy enforcement, aggregate and forensic reporting
- **Spam and greylisting** — server-side spam filtering, greylisting policies, per-tenant thresholds, quarantine management
- **Sieve filtering** — server-side mail rules, per-user and per-tenant filter scripts
- **Webmail** — browser-based mail client, address book, calendar integration
- **Outlook integration** — plug-in for "send via GVB" workflow, profile auto-configuration
- **Auto-config / Autodiscover** — automatic mail-client configuration delivery (Thunderbird autoconfig, Outlook autodiscover, Apple config profiles)

### File transfer and secure delivery

- **Secure file delivery** — encrypted file transfer with governance attestation, expiry policies, download tracking, audit trail
- **Filedrop pages** — branded upload portals for external parties, per-drop access control
- **FileLinks** — shareable download links with expiry, password protection, download limits, revocation
- **File requests** — single-use upload tickets for inbound document collection
- **Emaildrop** — email-to-filedrop processor, attachment extraction, policy-based routing
- **Upload scanning** — antivirus, malware detection, file-type validation, content inspection policies
- **File-transfer policy** — retention periods, maximum file sizes, allowed file types, geographic restrictions
- **Rate limiting and brute-force protection** — per-account and per-IP throttling, lockout policies, CAPTCHA integration

### DNS

- **Authoritative DNS** — zone management, record sets (A, AAAA, CNAME, MX, TXT, SRV, CAA, TLSA), DNSSEC signing
- **DNS clustering** — multi-node DNS synchronisation, zone transfer, split-horizon
- **Reverse DNS** — PTR record management for IP pools, delegation

### FTP and file access

- **FTP / SFTP** — FTP account provisioning, SFTP-only enforcement, chroot jails, bandwidth limits
- **Web disk** — WebDAV-based cloud-storage shares, per-user and per-tenant quotas, client auto-mount

### Calendar and contacts

- **CalDAV** — calendar server, shared calendars, free/busy lookup, scheduling, delegation
- **CardDAV** — contact server, shared address books, vCard import/export

### Web hosting and application services

- **Web server management** — virtual host configuration, TLS termination, HTTP/2 and HTTP/3, reverse proxy, load balancing
- **PHP / runtime management** — per-tenant PHP version selection, handler configuration, resource limits, extension management
- **Database management** — database provisioning (PostgreSQL, MySQL/MariaDB), per-tenant isolation, user management, remote access control, backup scheduling
- **Application deployment** — one-click application installers, staging environments, deployment pipelines
- **Cron / scheduled tasks** — per-tenant scheduled job management, execution logging, failure alerting

### Site builder and content

- **Native site builder (UniCORE.GVB.SiteBuilder)** — native site-builder engine; per-tenant site provisioning; content store; page tree; assets; pages and blocks; publish pipeline; multi-locale; status lifecycle (draft / staged / published)
- **Plugins and themes** — plugin registry, theme registry, plugin/theme descriptors, plugin kinds, install/upgrade lifecycle, governance attestation per plugin
- **Editor surface** — page-tree management, block-level edits, asset upload, page preview, scheduled publish, publish-history tracking
- **Two-substrate parity** — native site-builder is the Windows-substrate-side counterpart to embedded third-party site-builder integration on the Linux substrate; control surface (Cross-Platform API; governance journal) is invariant across the two

### Security and certificates

- **TLS certificate management** — certificate provisioning (ACME / Let’s Encrypt), renewal automation, CSR generation, private key storage, certificate deployment across services
- **Certificate authority integration** — internal CA for node-to-node trust, client certificate issuance, CRL/OCSP
- **Firewall and access control** — per-node and per-tenant firewall rules, IP blocking, country-level geo-blocking, port management
- **Intrusion detection** — brute-force detection, fail2ban-equivalent policies, real-time alerting
- **SSH access management** — key management, per-tenant shell access policies, session logging
- **Two-factor authentication** — TOTP-based 2FA for administrative and tenant access, recovery codes, hardware-key support

### Backup and disaster recovery

- **Backup policy** — full and incremental backups, per-tenant backup schedules, retention policies, off-site replication
- **Restore** — full-account restore, per-service restore (mail only, files only, databases only), point-in-time recovery
- **Disaster recovery** — cross-node failover, backup verification, recovery-time objectives per tenant tier

### Monitoring, reporting, and observability

- **Bandwidth reporting** — per-tenant, per-service, per-node bandwidth metrics; historical trends; overage alerting
- **Storage reporting** — disk usage per tenant, per service, per mailbox; growth projections; quota-approach warnings
- **Service health** — per-service uptime monitoring, latency metrics, error-rate tracking
- **Audit trail** — administrative action logging, tenant-action logging, immutable audit records, compliance export
- **Log management** — centralised log aggregation, per-tenant log isolation, retention policies, search

### Topology and multi-node operations

- **Node registry** — node identity, geographic location, jurisdiction, capability declaration
- **IP pool management** — /24 block allocation, per-tenant IP assignment, reputation segregation, warm-up scheduling
- **Inter-node federation** — the Global Virtual Bridge itself: cross-node mail routing, file delivery, DNS synchronisation, tenant migration
- **Tenant-node pinning** — data-residency enforcement, jurisdictional pinning, failover preferences
- **Live migration** — tenant migration between nodes (planned maintenance, jurisdiction change, capacity rebalancing)

### Node operations and administration

- **Server profiles** — per-node configuration profiles, role assignment, capability flags
- **Jurisdictional posture** — per-node data-sovereignty rules, cross-border transfer policies, regulatory compliance flags
- **Update preferences** — per-node update scheduling, maintenance windows, rollback policies
- **Runtime tweaks** — per-node performance tuning, service-specific configuration overrides
- **Software management** — package installation, version pinning, security patching, EOL tracking

### Federation and identity

- **SAML 2.0 SSO** — service-provider implementation, external IdP integration, attribute mapping, session management
- **External authentication** — LDAP/AD integration, OAuth2 federation, SCIM provisioning
- **External user identity model** — partner/counterparty/counsel identity, cross-tenant identity federation, guest access

### Industry classification and governance

- **12-Level Governance parameterisation** — per-industry governance profiles, level-specific policy enforcement, compliance attestation
- **Industry-isolated networks** — network-level isolation between industry classifications on shared infrastructure
- **Classification tiers** — industry-specific resource tiers, SLA differentiation, regulatory-requirement mapping

---

UniCORE.GVB is the substrate-services layer. It does not carry industry-specific Business Objects; those live in each Vertical CORE. The scope above is the full substrate — from hypervisor to application-services, governed throughout.

**Two-substrate parity at the customer-account-and-content layer.** UniCORE.GVB ships as one codebase that runs on either a Linux substrate or a Windows substrate. The two branches are co-equal at the control-surface layer (same governance, same Cross-Platform API surface, same evidence trail, same attestation shape). They differ at the third-party-integration layer: the Linux branch embeds established open / industry-standard reference products at the customer-account-and-content layer; the Windows branch combines third-party reference products at the hosting-account layer with a **native UniCORE.GVB.SiteBuilder** at the site-and-content layer. SiteBuilder is the first substrate-services component met by Unitek-original code rather than by wrapping a reference product. The scope above is invariant across both substrates.

---

## UniCORE.Desktop — client applications

UniCORE.Desktop provides the desktop client applications for the UniCORE family. These applications connect to services running on UniCORE.GVB and/or UniCORE. They are not products for sale — they are included with the UniCORE.GVB licence (CC BY 4.0), part of the same gift.

UniCORE.Desktop must independently pass the "Powered by UniCORE AI / built on TrueAI Foundation" certification gate.

Client applications (scope — the full list of desktop-side counterparts to the substrate-services above):

- **File transfer client** — secure file send/receive, filedrop upload, filelink management, download tracking
- **FTP / SFTP client** — file access to GVB-hosted storage, bookmark management, transfer queue
- **Mail configuration** — auto-configuration of desktop mail clients against GVB mail services
- **Calendar and contacts sync** — CalDAV/CardDAV client integration, offline sync, conflict resolution
- **Office integration** — document workflows connecting desktop productivity suites to GVB services
- **AI Chat** — governed AI assistant operating under TrueAI governance, connected to UniCORE AI services
- **Identity and authentication** — desktop-side identity provider, certificate-based authentication, 2FA integration
- **GVB API client** — typed HTTP client for the UniCORE.GVB substrate API, used by all other desktop applications
- **VPN / tunnel client** — secure connectivity to GVB nodes, jurisdictional routing
- **Backup client** — desktop-side backup agent connecting to GVB backup services
- **Admin console** — desktop administration interface for node operators and tenant administrators
- **VM management client** — desktop interface for hypervisor operations (VM lifecycle, snapshots, migration)
- **DNS management client** — zone and record management interface
- **Monitoring dashboard** — desktop-side observability client (bandwidth, storage, service health)

UniCORE.Desktop is documented in both this repository and [`bryanunitek/UniCORE`](https://github.com/bryanunitek/UniCORE) because the applications serve both layers. At certification, UniCORE.Desktop publishes as its own repository (`bryanunitek/UniCORE.Desktop`) with cross-references from both.

The working repository is `bryanunitek/UniCORE.Desktop-Claw` (private until certification).

---

## UniCORE Positioning Principle

The programme is positioned as **Harmony, Peace, Space Exploration, for Humanity**.

Industries and uses that align with this positioning are welcome. Those that do not are not. **Military uses are intentionally absent** from the programme and will not be added.

**The "Powered by UniCORE AI" and "built on TrueAI Foundation" certifications must not appear on any military use.** The badge is part of the gift, and the gift is meant for Harmony, Peace, Space Exploration, for Humanity — using the badge to brand weapons-class systems would invert the gift principle. The positioning closes that route.

This is a structural choice, not a marketing choice. The programme exists to keep critical decision systems available to humanity as gift.

---

## Related repositories

**The Foundation triad:**
- [`UniVERSE`](https://github.com/bryanunitek/UniVERSE) — The civilisational-scale programme.
- [`TrueAI`](https://github.com/bryanunitek/TrueAI) — The immutable Foundation. Nine Invariants.
- [`UniCORE-AI`](https://github.com/bryanunitek/UniCORE-AI) — The 12-Level reference architecture.

**The implementation layer:**
- [`UniCORE`](https://github.com/bryanunitek/UniCORE) — The implementation reference. Sister to this repository. Same certification gate. Same gift principle.

**The Vertical CORE family (working repositories — private until certification):**
- `bryanunitek/UniCORE.Law-Claw` — First Vertical CORE, Law sector.
- Future Vertical COREs as additional industries are produced.

**The substrate-services working repository (private until certification):**
- `bryanunitek/UniCORE.GVB-Claw` — Working repository for this layer. The contents become public on certification, distributed across this repository and the industry-classified siblings.

---

## Attribution

> Powered by UniCORE AI.
> Built on the TrueAI Foundation.

Attribution required wherever UniCORE.GVB, UniCORE, UniCORE AI, the TrueAI Foundation, or the 12-Level Governance Model is referenced, implemented, or extended.

---

## Licence

Given, not sold. The substrate-services layer is public, open, and free. The TrueAI Foundation cannot be modified, forked, commercialised, patented, or proprietarily captured. See [LICENSE.md](LICENSE.md) for full terms; see the canonical [`UniVERSE/IRREVOCABLE-LICENCE-DECLARATION.md`](https://github.com/bryanunitek/UniVERSE/blob/main/IRREVOCABLE-LICENCE-DECLARATION.md) for the formal irrevocability declaration that covers the whole programme.

— Bryan Fred, Unitek Systems Limited, Bedford, United Kingdom, May 2026.

---

## AI authorship

This repository is produced with AI assistance operating under TrueAI governance. The full disclosure is at [AI-AUTHORSHIP.md](AI-AUTHORSHIP.md).

---

## Discuss and contribute

Programme-level debate, adoption questions, translation, and corrections belong in [GitHub Discussions](https://github.com/bryanunitek/UniCORE.GVB/discussions). What is in scope: questions about UniCORE.GVB's role as the substrate-services layer, the industry classifications, the certification gate, the gift principle as it applies to substrate-services. What is out of scope: implementation specifics that belong inside a particular Vertical CORE's own repository.

For Foundation-level debate, use [UniVERSE](https://github.com/bryanunitek/UniVERSE/discussions), [TrueAI](https://github.com/bryanunitek/TrueAI/discussions), or [UniCORE-AI](https://github.com/bryanunitek/UniCORE-AI/discussions) Discussions as appropriate.

---

## Classification, brand, and claims

UniCORE.GVB is the substrate-services layer of governed AI. It is not a product, platform, SaaS offering, tool category, or brand for sale. See [STATEMENT-ON-CLAIMS.md](STATEMENT-ON-CLAIMS.md) for binding rules on how the UniCORE.GVB name may and may not be used.

---

## Contact

- **Public discussion:** [GitHub Discussions](https://github.com/bryanunitek/UniCORE.GVB/discussions) (see [DISCUSSIONS.md](DISCUSSIONS.md))
- **Private contact / connection request:** [LinkedIn](https://www.linkedin.com/in/bryan-fred-02209753/)
