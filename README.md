# Stryder Symbiosis

![Stryder Symbiosis](https://raw.githubusercontent.com/Alpharid/ACH/main/web/assets/filiales/stryder-1.webp)

A 2,500-metre colossus, the **Stryder**, walks without ever stopping through a procedural world.
Up to 8 players (or just one) play **Symbiotes**, tiny creatures living on its body: they feed it, heal it,
hunt its Parasites and build everything on it with real physics. A run ends when the colossus dies.

This repository is the game's **public distribution channel**: it only carries binaries, published as
GitHub Releases. The source code is private.

## Features

- Fully physical building: pieces, nails, hinges, ropes, winches, wheels, carving wood and stone,
  felling trees.
- Simulated matter: heat, fire, electricity, water, steam, cooking.
- A living colossus: hunger, wounds, Parasites, wildlife on its back; vultures and the Swarm on its heels.
  No on-screen gauge: the Stryder growls when it lacks something.
- Symbiote creator and spatial voice chat.
- Online co-op for 1 to 8 players, rejoin mid-run, automatic saves.

## Status

Playable alpha (0.6.0-alpha.33 as of 26 October 2026), released very often. Expect frequent changes
and bugs.

## Play

1. Download **`StryderLauncher.exe`** once from the
   [`launcher`](https://github.com/Alpharid/stryder-symbiosis-builds/releases/tag/launcher) release and keep it.
   Windows SmartScreen may warn because the exe is not code-signed: *More info* > *Run anyway*.
2. Start it, pick the **Main** (stable) or **Unstable** (newest features, may break) build, then
   *Install* / *Play*. The launcher downloads and verifies the build, updates itself and the game:
   it never needs to be re-sent.
3. In the game: *Host* (you can play alone) or *Join* (the host's address). Everybody in a run must have
   **the same build** (same channel, same version).

## System requirements

- Windows 10/11 64-bit.
- Vulkan or Direct3D 12 capable GPU.

## Releases

| tag | what |
|---|---|
| `launcher` | the launcher (`StryderLauncher.exe`, self-updating) |
| `v<version>` | **Main** builds (stable) |
| `preprod-<version>-<commit>` | **Unstable** builds (prereleases, only the last few are kept) |
| `runtime-<hash>` | the shared game engine binary used by builds (downloaded automatically) |

To take over this repository (AI or developer): [HANDOVER.md](HANDOVER.md).

A subsidiary of [Alpharium](https://alpharid.github.io/ACH/#filiale/stryder) — α Games division.
