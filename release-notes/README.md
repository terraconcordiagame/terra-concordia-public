# Release Notes

All notable changes to Terra Concordia are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/).

---

## [Unreleased]

Future release notes will appear here.

---

## [1.1.0] — 2026-06-18

First post-launch update — a big one.

### Added
- **Unique civilization abilities** (passive, active in every mode):
  - **Solaris (red)** — constructions and wonders cost 2 fewer resources.
  - **Mariteia (blue)** — explores ocean & island without spending a worker, and reveals +1 hex per Explore.
  - **Verdantis (green)** — Restore yields double (+1 extra global sustainability and +1 extra VP).
  - **Aurífera (yellow)** — +1 gold on every market trade and 1 extra Trade action per round (4 instead of 3).
  - Detailed in the Tutorial (Civilizations tab) and the Civilopedia.
- **3 new procedural music tracks** — Serene, Epic, Mystic — selectable in Settings → Sounds (new-player default: Mystic).
- **In-game release notes** — Help → "Release Notes & Latest Updates" (PDF, PT/EN/ES).
- **Main menu buttons** — "Manuals & Website" (opens the site in your language) and "Discord invite".
- **Version + build-date badge** on out-of-game screens.
- **Redesigned main menu** — frameless, reordered buttons with emojis, "Quit" in the bottom-right; the Civilopedia button opens the in-game guide.
- **Full keyboard play** — Tab moves between panels and buttons, Enter/Space activates. New tutorial tabs: "Shortcuts", "VP Breakdown" (how points are counted) and "Strategy" (how to score more).
- **Animation pack** — floating numbers, worker "pop", animated hex reveal, pulsing ring on the active player + glow on the selected action, shake/spark on the Sustainability bar. Unexplored hexes now twinkle with 4-point golden stars and a soft halo (replacing the old dots).
- Larger AI difficulty selector and a more prominent "play against AI" toggle; the Research modal zooms the card on hover.

### Achievements
- Win-only achievements unlock **only on an actual win** — never when losing in solo (scenario goal respected), losing to another player, or losing by ecological collapse. Winning by forfeit (an opponent leaving/dropping) no longer unlocks them either.
- Civilization achievements unlock when winning with that civilization in any mode.
- "Perfect Balance": win with Global and Individual Sustainability at 10. "Diplomat" and "Path of Peace" now track the Influence action.
- "Hard Mode Win" requires AI in the match; "Diplomacy (4 players)" uses the initial human count.

### Fixed
- **End-of-game videos** — defeat/collapse video for every losing player, victory video only for the winner (any mode), shown before the end screen; game audio is muted while a video plays.
- **Scoring** — an achieved secret objective now correctly adds its VP (it was 0 before); conditional card VP (per alliance / per player with less influence) is computed correctly, without double-counting.
- **Player-interaction cards** implemented/fixed: Embargo, Boycott, Partnership, Monopoly, Trade Routes and Military Alliance (immunity to negative events).
- **Multiplayer** — turn timer respects the disconnect pause; residual state (discard/timeline) reset each new game; winner computed via the full ranking (host and guest aligned); anti-cheat on discards; error feedback when accepting an alliance; ecological collapse ignores players who left; a "heartbeat" detects abrupt disconnects so the host reliably ends the match, with a notice of who left. **Multiplayer chat removed** (store content policy).
- **Solo / vs-AI** — cards that depend on other players / human cooperation are removed from the decks; the AI now explores hexes in random directions.
- **Saves** are now written to `Terra Concordia\saves` (Steam Cloud compatible); saves from older versions are migrated automatically.
- Unexplored hexes show fog (instead of "?"); correct icon on the "Public Objective Led" notice; action buttons no longer stay stuck in focus; "show owner inside hex" now starts off.
- Slightly taller Global Sustainability bar; wider Settings window; footer shows the correct version; PT manuals link fixed; each mode runs its correct number of rounds; intro and victory videos updated.
- Many translations (PT/EN/ES): HUD, alerts, history log, turn labels, discard, navigation, diplomacy and end of game.

---

## [1.0.46] — Pre-Launch (Final RC)

### Initial Release Candidate

- 142 hand-crafted cards
- 4 civilizations (Solaris, Verdantis, Mariteia, Aurífera)
- 6 solo scenarios (★ to ★★★★★)
- 6 game variants
- Automa AI with 3 difficulty levels
- Global Sustainability mechanic
- Full Print & Play kit (161 assets)
- LAN multiplayer (WebSocket) + Steam Networking (P2P)
- Full PT/EN/ES UI localization (~1300 i18n keys) — runtime language switch + native Electron menu in player's language
- Native Windows installer (NSIS) + portable
- 38 Steam achievements (30 SP + 8 MP) + 76 icons (unlocked + locked states)
- 4 trailer languages (60s + 90s) with bookends
- 30+ unique animations
- 90 unit tests passing

---

## Roadmap

### v1.0.x — Hot fixes (Launch + 30 days)
Bug fixes based on community feedback.

### v1.1.0 — "Polish & Performance" (T+3 months)
QoL improvements, performance optimizations, new achievements.

### v1.2.0 — "Content Drop" (T+6 months)
1 new solo scenario, 1 new wonder, 5 new technologies.

### v1.3.0 — "Community Choice" (T+9 months)
Content voted by community.

### v2.0.0 — "Multiplayer Online" (T+12 months) ⭐
Steam P2P multiplayer, 2-4 players. Free for all owners.

### v2.X — "Workshop"
Steam Workshop integration. User-created scenarios.

---

For the detailed content roadmap, join our [Discord](https://discord.gg/Xp869eSNWP) — the full roadmap lives in the private development repository.
