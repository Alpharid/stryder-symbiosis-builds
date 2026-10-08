# Stryder Symbiosis - builds

Public release channel of **Stryder Symbiosis**, a 1-8 player co-op game where the players are Symbiotes
living on the body of a giant that never stops walking (Godot 4.7). This repository only carries
**binaries** (as GitHub Releases); the source code lives in a private repository.

## Play

1. Download **`StryderLauncher.exe`** once from the release tagged `launcher` and keep it
   (Windows 10/11 64-bit, Vulkan or Direct3D 12 GPU). Windows SmartScreen may warn because the exe is
   not code-signed: *More info* > *Run anyway*.
2. Start it, pick **PROD** (stable) or **PREPROD** (newest features, may break), press *Play*.
   The launcher downloads and verifies the build, updates itself and the game, and never needs to be re-sent.
3. In the game: *Host* (you can start alone) or *Join* (the host's address). Everybody in a run must run
   the **same build** (same channel and version).

## Releases

| tag | what |
|---|---|
| `launcher` | the launcher (`StryderLauncher.exe`, self-updating) |
| `v<version>` | **PROD** builds |
| `preprod-<version>-<commit>` | **PREPROD** builds (prereleases, the last few are kept) |
| `runtime-<hash>` | the shared game engine binary used by builds (downloaded automatically) |

See [HANDOVER.md](HANDOVER.md) for how this repository is produced and consumed.