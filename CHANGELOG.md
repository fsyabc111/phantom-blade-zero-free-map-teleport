# Changelog

## 1.0.1 — 2026-10-30

- Allow regular-map travel to activated bells without the traversal charm inventory check, item-cost dialog or charm consumption.
- Allow the regular-map path when standing near an activated bell.
- Retain the existing player-state, story, restricted-area and destination checks, including the final story-critical-section recheck.
- Prevent repeated clicks from starting duplicate travel requests; reset the guard when the map reopens or travel fails.
- Include matching `.utoc` and `.ucas` companion files with a unique container identity and updated BLAKE3 chunk hash, fixing mounting in Steam Build 26266538.
- Confirm modified script loading and successful direct map travel in game.

## 1.0.0 — Local prototype

The initial pak-only package did not load in the game. It was superseded by 1.0.1 and is not distributed here.
