<div align="center">

# Hi, I'm Collins — `@unccllin`

### Systems & Security Engineer · Device Trust · Applied AI

I build software that operates **below the application layer** — device-owner agents,
secure-boot provisioning, remote lockdown platforms — and ship full products on top of it.

`Python` · `TypeScript` · `Node.js` · `React / Next.js` · `Java (Android)` · `Flask / FastAPI` · `PostgreSQL` · `Docker`

</div>

---

## 🔒 Remote Device Lockdown System
**Anti-theft platform for field devices — flag a stolen laptop, encrypt its data, lock the screen. Reversible on recovery.**

A fleet-management product built end to end, from the silicon up:

- **Server** — Node.js / Express + PostgreSQL, JWT auth, RBAC, OpenAPI spec, serves the dashboard on one origin
- **Dashboard** — React + Vite + Tailwind admin UI with two-step confirmation on destructive actions
- **Device agent** — Python background service; encrypts only the designated folder, key escrowed server-side, TLS-pinned
- **Firmware layer** — Secure Boot keygen & enrollment, TPM PCR sealing, UEFI variable handling, BitLocker PBA recovery runbook, signed boot images
- **Desktop app** — Electron installer bundling server + dashboard + agent-installer generator, auto-updates via GitHub Releases
- **Deployment** — Docker Compose production stack (Postgres + Caddy auto-HTTPS), GDPR LIA, DR runbook, E2E & load-test docs

> 319 commits of iterative hardening — including command-injection and checksum fail-open fixes found through self-audit.

`Node.js` `Express` `PostgreSQL` `React` `Python` `Electron` `Secure Boot` `TPM` `Docker` `Caddy`

---

## 🛡️ SentinelGuard
**Device-Owner Android app that kills adware before it runs — and removes what's already there.**

Built to solve a real problem: adware (wallpaper/launcher hijackers, ByteDance-SDK "cleaner" apps, short-video spam) exploits the gap that normal apps *cannot* watch other installs. SentinelGuard closes it with enterprise MDM powers:

- `DISALLOW_INSTALL_UNKNOWN_SOURCES` — blocks sideloaded APKs at the OS level
- `PACKAGE_ADDED` + `setPackagesSuspended()` — freezes a malicious package **within milliseconds** of install
- Silent uninstall via `PackageInstaller` — adware can't hijack the uninstall UI
- `ThreatEngine` — signature/heuristic verdicts on known adware families; boot receiver re-arms hardening after every reboot

`Java` `Android Device Owner / MDM` `PackageInstaller` `ADB provisioning`

---

## 🗺️ Land Site
**Production marketplace for a Kenyan land seller — real client, real users.**

- Next.js 14 (App Router) + plain CSS design tokens, Leaflet plot maps, WhatsApp / phone / site-visit lead flows
- Flask + SQLAlchemy REST API on Neon Postgres, Flask-Login auth, multi-company listings with per-company admins
- Ships with honest engineering docs: `DECISIONS.md`, `HANDOFF.md`, OpenAPI spec, QA checklist

`Next.js` `Flask` `PostgreSQL (Neon)` `Leaflet` `Vercel`

---

## 🤝 Open Source Contributions

**[pi-agent](https://github.com/earendil-works/pi-agent)** — coding-agent harness (TypeScript monorepo).
Maintained a fork with installer & packaging work: offline builds, extension-manifest patching, peer-dependency fixes, a curated extension set, a Devin bridge, and a one-command upstream-sync script.

---

<details>
<summary><b>More projects</b> — fintech & applied AI</summary>

<br>

**📈 `bnbot` — gated algorithmic trading pipeline** `Python`
Layered architecture where *no layer acts on its own*: regime → rotation → entry → risk → execution, each output passing a contract gate before the next layer sees it. Kill switch, drawdown halts, regime-switched entries validated on real history. `graph.mermaid` generated from the same declarations that drive the runtime — it can't drift.

**📓 Meridian — trading journal** `FastAPI` `Next.js` `PostgreSQL`
ICT confluence scoring, candlestick trade replay, AI insights over trade data, MetaTrader 5 auto-sync bridge, Docker Compose deploy.

**🎬 ClipForge — retention-engineered video generation** `Python`
Beat-driven pipeline on top of MoneyPrinterTurbo's render layer: psychology-tagged beat plans (hooks, curiosity gaps, disguised CTAs, loop closers), per-beat clip resolution, SFX interrupts, TTS + subtitles.

</details>

---

## ⚙️ How I work

- **Security is a feature you build, not a patch you apply** — escrowed keys, signed boot chains, OS-level policy, fail-closed scorers
- **Docs are part of the product** — ADRs, runbooks, threat models, handoff notes ship with the code
- **Gates over trust** — pipelines that refuse to run on invalid state beat careful code every time

<div align="center">

📫 **mainacollins196@gmail.com** · GitHub: [@Unccllin](https://github.com/Unccllin)

</div>
