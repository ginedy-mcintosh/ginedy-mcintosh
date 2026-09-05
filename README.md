<!--
  DELIVERABLE 2 — PROFILE README
  Repo name must EXACTLY match your GitHub username, e.g. github.com/ginedy-mcintosh/ginedy-mcintosh
  File path: README.md (root)
-->

<div align="center">

# Ginedy McIntosh

### Lead Software Developer · Systems Architect · AI Integration Engineer

**Houston, Texas** · Building multi-tenant SaaS, telephony, and cross-platform streaming systems since 2014

<br/>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PHP](https://img.shields.io/badge/PHP_8.3-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel_12-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Roku](https://img.shields.io/badge/Roku_SceneGraph-662D91?style=for-the-badge&logo=roku&logoColor=white)

![MySQL](https://img.shields.io/badge/MySQL_/_MariaDB-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Asterisk](https://img.shields.io/badge/Asterisk_PBX-F60?style=for-the-badge&logo=asterisk&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu_Server-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![systemd](https://img.shields.io/badge/systemd-30B980?style=for-the-badge&logo=linux&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

</div>

---

## What I actually do

I own the full lifecycle — architecture, code, Linux infrastructure, deployment, and post-launch incident response — for a portfolio of production systems that carry real revenue and real phone calls. No handoff to an ops team. If it pages at 2am, it pages me.

| Domain | What I ship |
|---|---|
| **Multi-tenant SaaS** | Laravel 12 / PHP 8.3 platforms with strict tenant isolation, encrypted credential vaults, audit trails, and Stripe billing under idempotent webhook handling |
| **Real-time telephony** | Asterisk 20 PBX with AGI-driven AI voice answering, per-tenant dialplans, holiday/schedule routing, and sub-second turnaround budgets |
| **AI integration** | LLM-backed lead scoring, quote generation, and voice agents — with provider fallback chains, structured-output validation, and cost ceilings |
| **Cross-platform apps** | Published and maintained consumer streaming apps on Apple TV/iOS, Android, Roku (SceneGraph/BrightScript), Fire TV, and Samsung Tizen |
| **Linux infrastructure** | Bare-metal and VPS fleet on Ubuntu — systemd services and timers, logrotate, nginx, DNS authority, TLS, SSH-based CI/CD |

---

## Featured work

These repositories are **documentation-first showcases**. Production source is proprietary and stays private; what's public here is the architecture, the reasoning, the trade-offs, and sanitized illustrative snippets.

| Repository | Focus | Stack |
|---|---|---|
| **[Streaming & Mobile Ecosystem](https://github.com/ginedy-mcintosh/Streaming-Mobile-Ecosystem)** | Cross-platform apps shipped to 6 storefronts, shared media API, platform review workflows | SceneGraph · Swift · Kotlin · Tizen · FastAPI |
| **[MediosPlano-CAD-Engine](https://github.com/ginedy-mcintosh/MediosPlano-CAD-Engine)** | Parametric CAD engine: transcribed plans → 10-sheet permit sets + reconciled material takeoff | Python · ezdxf · Shapely · FastAPI |
| **[Medioscore-AI-PBX](https://github.com/ginedy-mcintosh/Medioscore-AI-PBX)** | Multi-tenant Asterisk PBX with real-time AI receptionist | Asterisk 20 · PHP-FPM · AGI · MariaDB |
| **[MediosBilling-CRM](https://github.com/ginedy-mcintosh/MediosBilling-CRM)** | Secure multi-tenant billing/CRM, server-authoritative money math | Laravel 12 · MySQL · Stripe |
| **[Ameritechwebs-AI-Lead-Engine](https://github.com/ginedy-mcintosh/Ameritechwebs-AI-Lead-Engine)** | AI prospecting: finds under-served local businesses, audits them, auto-quotes | PHP 8.2 · Places/PageSpeed APIs · LLM |
| **[Dargratia-Church-Suite](https://github.com/ginedy-mcintosh/Dargratia-Church-Suite)** | Hierarchical church-finance SaaS with regulated remittance math | Laravel · MySQL · PDF/e-sign |

---

## How I evaluate AI-generated code

I use LLM assistance daily across all of the above, which means I spend as much time *reviewing* generated code as writing it. My review order is deliberate:

1. **Correctness of the invariant, not the syntax.** Generated code compiles almost always. The failure is semantic — money computed client-side, a tenant scope silently dropped from a query, a webhook handler that isn't idempotent.
2. **Concurrency and signal behavior.** The bugs that survive review are the ones that only appear under a hangup, a retry, or a race. Static reading catches these; test suites usually don't.
3. **Does the metric mean what the name says?** I've shipped fixes where a monitoring field named `totalConnections` counted internal packaging objects, not users. Plausible-looking output that is confidently wrong is the expensive failure mode — in monitoring and in models.
4. **Blast radius on failure.** What breaks, who notices, and can it be reverted without a restore?

Each showcase repo below includes a **`Code Review Notes`** section documenting a real defect class I found and the reasoning that surfaced it.

---

## Engineering principles I hold to

> **Server-authoritative money.** Any total a customer can see is recomputed server-side before it is stored or charged. Client math is a display convenience, never a source of truth.

> **Idempotency by default.** Webhooks, fulfillment jobs, and provisioning routines are safe to replay. Payment providers retry; the system must be boring about it.

> **Tenant isolation is a schema property, not a controller habit.** Global scopes and foreign-key constraints, so a forgotten `where` clause fails closed.

> **No fabricated data — ever.** I've declined to build an inflated audience counter for an ad-supported product. Invented numbers put customer relationships and store listings at risk, and they are indefensible the moment someone audits them.

> **Trilingual from line one.** Every product ships English, Spanish, and Portuguese with full key parity. Retrofitting i18n costs 5× what building it in does.

---

## Currently

- Architecting a shared multi-company API backbone so one CRM core serves telephony, hosting, and services products instead of four parallel billing systems.
- Expanding real-time AI voice handling on the PBX side — barge-in, intent capture, and safe hand-off to a human queue.
- Available for **contract work in AI code evaluation, technical writing, and complex problem solving.**

---

<div align="center">

### Reach me

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ginedy.mcintosh@gmail.com)

<br/>

![](https://github-readme-stats.vercel.app/api?username=ginedy-mcintosh&show_icons=true&hide_border=true&theme=tokyonight&hide=issues)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=ginedy-mcintosh&layout=compact&hide_border=true&theme=tokyonight)

</div>
