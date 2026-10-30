# Technical notes

## Scope

The package overrides one Puerts module:

`../../../ProjectPBZ/Content/JavaScript/UI/Widget/Map.js`

The original module was read from the local running game. The patch targets Steam App 4115450, Build 26266538.

## Changes

- Remove the traversal charm inventory gate in `MapInterface.runTeleportGates`.
- Remove the nearby-bell gate from the regular-map path.
- Replace `confirmAndConsumeCharm` with a direct call to the existing `doCharmTeleport`, preserving the final flow-critical-section check.
- Add an in-flight guard and reset it on map initialization or a failed teleport request.
- Preserve the remaining map module and use the existing destination, loading, teleport and save flow.

The source difference is available in [Map.patch](../patches/Map.patch). Only map entries already supplied by the game can be selected; the mod does not change bell activation or reveal hidden map entries.

## Container layout

The `.pak` uses the V11 format with mount point `../../../`. Its only entry is the modified JavaScript module. In this game build, mounting also requires matching IoStore companions.

The `.utoc` and `.ucas` use the installed game's empty-container layout. They contain no game assets. Their container IDs were changed consistently, and the container-header chunk's 20-byte BLAKE3 hash was recalculated.

Container ID bytes: `266628a5177a249a`.

## Verification boundary

The 17 behavior checks run the actual original and modified modules in a mocked JavaScript environment. They verify the changed gates and call path but do not simulate Unreal's level streaming or persistence.

The modified source was separately observed in a restarted game process, and direct regular-map travel was confirmed by the player on 2026-10-30. Cross-region travel and loading a save after travel have not been separately confirmed.

The public archive contains the three Mod files and installation documentation. Local save backups, runtime memory inspection output and tooling caches are not part of the repository.
