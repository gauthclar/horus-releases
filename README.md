# Horus — Releases

**Public download channel and auto-update feed for [Horus](https://github.com/gauthclar/Horus)** — a fast desktop app (and TUI) for developers who juggle many Git repositories: switch projects, manage worktrees, review & push, run commands, browse databases, and track Azure DevOps work items.

[![Latest release](https://img.shields.io/github/v/release/gauthclar/horus-releases?label=latest&color=2a9d96)](https://github.com/gauthclar/horus-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/gauthclar/horus-releases/total?color=2a9d96)](https://github.com/gauthclar/horus-releases/releases)
[![Source](https://img.shields.io/badge/source-gauthclar%2FHorus-24292f?logo=github)](https://github.com/gauthclar/Horus)

This repository hosts the **published Windows binaries** and the **`latest.json`** update manifest. The **source code, issues and documentation** live in the main repository: **[github.com/gauthclar/Horus](https://github.com/gauthclar/Horus)**.

---

## Install (Windows)

1. Open the **[latest release](https://github.com/gauthclar/horus-releases/releases/latest)**.
2. Under **Assets**, download **`setup.exe`**.
3. Double-click it. If Windows SmartScreen appears (the app isn't code-signed yet): **More info → Run anyway**.

Per-user install — **no admin rights** — and a Desktop shortcut is created automatically.
Full step-by-step guide & troubleshooting: **[docs/INSTALL.md](https://github.com/gauthclar/Horus/blob/master/docs/INSTALL.md)**.

## Automatic updates

Since **v0.11.0**, Horus keeps itself up to date. On launch it reads the **`latest.json`** manifest attached to the latest release here; when a newer version is available, the app shows an **"Update"** banner and installs it in one click (via the signed Tauri updater). You can also trigger a check manually from the version indicator inside the app.

## What's in a release

| Asset | Purpose |
|-------|---------|
| `setup.exe` | NSIS installer (per-user) — **this is what you download to install** |
| `latest.json` | Update manifest read by the in-app auto-updater |
| `*.sig` | Minisign signature of the update artifact (verified before installing) |

## For maintainers

Releases here are **produced from the main repository**: running `./release.ps1` (in [gauthclar/Horus](https://github.com/gauthclar/Horus)) builds the installer and the signed update artifacts, then uploads them to a fresh `v<version>` release in this repo. See the [main README](https://github.com/gauthclar/Horus#readme) for the release workflow.

---

<sub>📦 Downloads live here · 🛠️ Source code & issues → <a href="https://github.com/gauthclar/Horus">gauthclar/Horus</a></sub>
