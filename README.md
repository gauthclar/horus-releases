# Horus — Releases

**Public download channel and auto-update feed for [Horus](https://github.com/gauthclar/Horus)** — a fast desktop app for developers who juggle many Git repositories: switch projects, manage worktrees, review & push, run commands, browse databases, and track Azure DevOps work items.

[![Latest release](https://img.shields.io/github/v/release/gauthclar/horus-releases?label=latest&color=2a9d96)](https://github.com/gauthclar/horus-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/gauthclar/horus-releases/total?color=2a9d96)](https://github.com/gauthclar/horus-releases/releases)
[![Source](https://img.shields.io/badge/source-gauthclar%2FHorus-24292f?logo=github)](https://github.com/gauthclar/Horus)

This repository hosts the **published Windows binaries** and the **`latest.json`** update manifest. The **source code, issues and documentation** live in the main repository: **[github.com/gauthclar/Horus](https://github.com/gauthclar/Horus)**.

---

## Install (Windows)

1. Open the **[latest release](https://github.com/gauthclar/horus-releases/releases/latest)**.
2. Under **Assets**, download **`setup.exe`**.
3. Double-click it. If Windows SmartScreen appears (the installer isn't code-signed yet, see the [code signing policy](#code-signing-policy)): **More info → Run anyway**.

Per-user install — **no admin rights** — and a Desktop shortcut is created automatically.
Full step-by-step guide & troubleshooting: **[docs/INSTALL.md](https://github.com/gauthclar/Horus/blob/master/docs/INSTALL.md)**.

## Automatic updates

Since **v0.11.0**, Horus keeps itself up to date. On launch it reads the **`latest.json`** manifest attached to the latest release here; when a newer version is available, the app shows an **"Update"** banner and installs it in one click (via the signed Tauri updater). You can also trigger a check manually from the version indicator inside the app.

## What's in a release

| Asset | Purpose |
|-------|---------|
| `setup.exe` | NSIS installer (per-user) — **this is what you download to install** |
| `latest.json` | Update manifest read by the in-app auto-updater; it carries the minisign signature of `setup.exe`, verified by the app before installing |

## Code signing policy

**Status: application to the [SignPath Foundation](https://signpath.org) pending.** Releases are not code-signed yet.

Once the project is accepted, the Windows binaries of every release, `horus-gui.exe` and the `setup.exe` installer, will be signed. Free code signing provided by [SignPath.io](https://signpath.io), certificate by [SignPath Foundation](https://signpath.org).

Every release is built by GitHub Actions from the [source repository](https://github.com/gauthclar/Horus) and each signing request is approved by hand. Team roles and the privacy policy: **[code signing policy in the main README](https://github.com/gauthclar/Horus#code-signing-policy)**.

## For maintainers

Releases here are **built and published by GitHub Actions** in [gauthclar/Horus](https://github.com/gauthclar/Horus) when a `vX.Y.Z` tag is pushed: the workflow builds the installer, signs the update payload, writes `latest.json` and uploads both to a fresh `vX.Y.Z` release in this repo. Procedure: [docs/RELEASING.md](https://github.com/gauthclar/Horus/blob/master/docs/RELEASING.md).

---

<sub>📦 Downloads live here · 🛠️ Source code & issues → <a href="https://github.com/gauthclar/Horus">gauthclar/Horus</a></sub>
