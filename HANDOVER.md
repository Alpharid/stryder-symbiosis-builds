# HANDOVER - stryder-symbiosis-builds

> Last updated: 2026-10-08. Owner: Alpharid (French speaker; docs in English). Game repo: `C-Chafik/Stryder-Symbiosis` (private).

## What this repository is
The **public distribution channel** of the private game repo `C-Chafik/Stryder-Symbiosis` (Godot 4.7.2,
co-op game "Stryder Symbiosis"). It contains **no source and no binaries in git**: only this documentation.
All artifacts live in **GitHub Releases** and are produced by the publish tool of the private repo
(`sandbox/launcher/tools/publish.py` during the exploration phase). Nothing here is edited by hand.

## Contract with the launcher (private repo, `sandbox/launcher/`)
The launcher reads `GET https://api.github.com/repos/Alpharid/stryder-symbiosis-builds/releases` (anonymous) and picks:
* PROD = newest non-prerelease whose tag starts with `v`; assets `manifest.json` + `game.pck.zip`
* PREPROD = newest release whose tag starts with `preprod-`
* launcher update = release tagged `launcher` (`launcher-manifest.json`, `StryderLauncher.zip`, plus the bare `StryderLauncher.exe` for first download)
* `runtime-<sha8>` releases hold `runtime.zip` (the engine exe shared by builds); a build manifest names the release it needs (`files[].release`).

`manifest.json` schema 1: `channel, version, commit, built_at, build_id ("<version>|<channel>|<commit>"), engine, min_launcher, files[{name, asset, release?, shared?, size, zip_size, sha256, zip_sha256}]`.
The launcher verifies every sha256 and writes its own `manifest.json` into the build folder last.

## Rules
* Never delete a `runtime-*` release that a still-listed build manifest references; only `preprod-*` releases are pruned (last 3 kept).
* Never rename tags or asset names: the launcher relies on them.
* Repo stays public (the launcher downloads anonymously); do not put secrets or source here.

## History
* 2026-10-08: repository created (pattern copied from `Alpharid/oddyseus-fst-builds`), no release yet.