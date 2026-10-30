# Phantom Blade Zero — Free Map Teleport

[简体中文](README.md) · [Download v1.0.1](https://github.com/fsyabc111/phantom-blade-zero-free-map-teleport/releases/tag/v1.0.1)

Open the regular map in a safe outdoor area and travel to an activated bell without owning or consuming a traversal charm. The item-cost confirmation dialog is skipped.

The mod retains combat, airborne/state, story, restricted-area, alternate-space and destination restrictions. It does not activate undiscovered bells. The regular map also works when standing near a bell.

## Compatibility

- Mod version: **1.0.1**
- Platform: **Steam, Windows**
- Steam App ID: **4115450**
- Tested game Build ID: **26266538**

Compatibility must be checked again after game updates. Other map mods replacing `JavaScript/UI/Widget/Map.js` may conflict.

## Installation

1. Exit the game completely and back up your saves.
2. In Steam, right-click the game and choose **Manage → Browse local files**.
3. Download `FreeMapTeleport-1.0.1-Steam-Build26266538.zip` from [Releases](https://github.com/fsyabc111/phantom-blade-zero-free-map-teleport/releases/latest). Use this archive rather than GitHub's automatically generated Source code archives.
4. Extract its **`ProjectPBZ` folder** into the game root directory.
5. Check that all three files below are directly inside `ProjectPBZ/Content/Paks/`, then restart the game.

```text
ProjectPBZ-FreeMapTeleport_999_P.pak
ProjectPBZ-FreeMapTeleport_999_P.utoc
ProjectPBZ-FreeMapTeleport_999_P.ucas
```

**Keep all three files together in the Paks root directory.** This game build requires the matching IoStore container to mount the pak.

Open the regular map, select an activated bell and use the game's existing travel action.

## Uninstall

Exit the game, remove only the three `FreeMapTeleport` files above, and restart the game.

## Validation

- October 30, 2026: the modified map script was observed in the restarted game process, and a player confirmed direct map travel worked.
- 17 script behavior checks passed, including zero charms, retained restrictions, repeated input and failure retries.
- Script syntax, packaged script readback, container identities and content hashes passed verification.
- **Cross-region travel and loading a save after teleporting have not been separately confirmed.**

Checksums are available in [downloads/SHA256SUMS.txt](downloads/SHA256SUMS.txt). A copy of the installation archive is also stored in [downloads](downloads/FreeMapTeleport-1.0.1-Steam-Build26266538.zip).

For bug reports, include the game Build ID, mod version, exact message and any other map mods in use. See [technical notes](docs/TECHNICAL.md), the [patch](patches/Map.patch) and [changelog](CHANGELOG.md) for implementation details.

This is an unofficial mod. Installation requires no Python, Node.js or separate mod loader.
