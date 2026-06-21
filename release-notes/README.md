# Release Notes

All notable changes to Terra Concordia are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/).

---

## [Unreleased]

Future release notes will appear here.

---

## [1.1.0] — 2026-06-20

📄 **Official notes (PDF):** [English](v1.1.0/ReleaseNotes-EN.pdf) · [Português](v1.1.0/ReleaseNotes-PT.pdf) · [Español](v1.1.0/ReleaseNotes-ES.pdf)

First post-launch update — a big one.

### Added
- **Unique civilization abilities** (passive, active in every mode):
  - **Solaris (red)** — constructions and wonders cost 2 fewer resources.
  - **Mariteia (blue)** — explores ocean & island without spending a worker, and reveals +1 hex per Explore.
  - **Verdantis (green)** — Restore yields double (+1 extra global sustainability and +1 extra VP).
  - **Aurífera (yellow)** — +1 gold on every market trade and 1 extra Trade action per round (4 instead of 3).
  - Detailed in the Tutorial (Civilizations tab) and the Civilopedia.
- **13 procedural music tracks** (Settings → Sounds) — 7 beatless orchestral ambiences (Serene, Epic, Mystic, Pastoral, Oceanic, Twilight, Ceremonial) + 6 with distinct rhythms (March, Tribal, Pulse, Festival, Tavern, Gallop). New-player default: March.
- **12 background color palettes** for the whole game (board, panels, top bar, modals, menus): Classic, Nocturne, Bronze, Forest, Wine, Slate, Ember, Midnight, Jade, Rose, Obsidian, Plum.
- **Animated end-of-game scoreboard** — category-by-category count-up (~700 ms each); the winner and fanfare appear only at the very end (suspense to the last number); no blank rows.
- **Redesigned in-hex icons** at a uniform size (house / hard-hat worker / boat), with the VP badge, owner marker, influence disc and wonder repositioned so they never overlap; sidebar workers shown as emojis (green = free, dimmed = placed/exhausted).
- **AI feedback & pacing** — every AI action now plays its sound, effect and message for all players (solo & MP); the AI waits 3s before each action so you can follow it (and you can no longer act "for the AI" during that wait).
- Wonder reveal: the hex animation plays first, then the fullscreen video opens.
- **In-game release notes** (Help → "Release Notes & Latest Updates"), "Manuals & Website" + "Discord" main-menu buttons, version/build-date badge, redesigned frameless main menu, **full keyboard play** + new tutorial tabs (Shortcuts / VP Breakdown / Strategy), golden-star unexplored hexes, animation pack, larger AI difficulty selector and Research card zoom on hover.

### Multiplayer
- **Shared feedback** — sounds and on-screen messages for every action (collect, build, trade…) now play for ALL players, not just the actor; phase summaries (Planning/Production/Maintenance) are identical for host and guests.
- **History in each player's language** — the match log is re-translated per player (guests used to see the host's language); phase-summary titles localized too.
- **Turn alert** — a sound + on-screen notice when it's your turn (at 57s and again at 10s remaining).
- "Join match" now lists waiting matches before you create one (Steam); MP stats (hosted time / reconnection / no-AFK) no longer overwritten on the guest; guest builds no longer flicker at the 3-builds-per-round limit; extra anti-cheat hardening; turn timer respects disconnect pauses; the host reliably ends the match on disconnect (heartbeat) with a "who left" notice; **chat removed** (store content policy).

### Achievements
- Win-only achievements unlock **only on an actual win** — never when losing in solo (scenario goal respected), losing to another player, or by ecological collapse. Winning by forfeit (an opponent leaving/dropping) no longer counts.
- Civilization achievements unlock when winning with that civilization in any mode.
- "Perfect Balance": win with Global and Individual Sustainability at 10. "Diplomat" and "Path of Peace" now track the Influence action.
- "Hard Mode Win" requires AI in the match; "Diplomacy (4 players)" uses the initial human count.

### Card & balance fixes
- **Critical objective-scoring fix** — "Admiral" and "Prodigy Scientist" measured the wrong metric (could change the winner); fixed alongside "Guardian of Nature", "Council of Sages", "Ancient Inscriptions", the "most production" objective and the "Ancient Map" card's missing +1 VP.
- **Immediate build/research bonuses no longer apply twice** (e.g. CON-19 gave +4 influence instead of +2; some wonders/techs doubled gains).
- Many cards now do exactly what their text says: TRB-01 / PRO-15 (1 free build per round), EXP-10 (true free research), CON-19 (+1 VP per Influence), CON-03 (Granary +5 storage), COM-02 (+4 gold), COM-08 (guaranteed +8 gold), INF-06, EXP-07, INF-08, and per-round cards (Embassy, Silk Road, Natural Spring, Abandoned Mine); Metallurgy / Energy Crystals discounts applied; Alchemy/Workshop/Medicine/Royal Road effects aligned.
- Alliance exploit closed (+3 gold paid only on a peaceful end); wonders no longer count toward the upkeep tax; stealing a card with a full hand returns it instead of destroying it; resource-overflow-to-gold summed correctly; EN/ES card texts and target-picker labels (Embargo/Boycott/Partnership/Spy) synced to the real effects.
- **AI rebalanced** — now stronger (plays its cards with the fixed discounts/income), so its starting VP head start was reduced to Easy +10 / Normal +30 / Hard +50 (was 20/45/70); plays beneficial hand cards; explores in random directions; a solo freeze (human passing first) is fixed.

### Other fixes
- **Scoring** — an achieved secret objective now adds its VP (was 0 before); conditional card VP (per alliance / per player with less influence) computed without double-counting; the end-of-game winner reveal is guaranteed even across multiplayer resyncs.
- **End-of-game videos** — defeat/collapse video for every losing player, victory video only for the winner (any mode); game audio is muted while a video plays.
- **Player-interaction cards** implemented/fixed: Embargo, Boycott, Partnership, Monopoly, Trade Routes, Military Alliance.
- **Saves** moved to `Terra Concordia\saves` (Steam Cloud compatible; older saves auto-migrated).
- Solo / vs-AI deck filtering; unexplored hexes show fog (instead of "?"); correct "Public Objective Led" icon; action buttons no longer stuck in focus; "show owner inside hex" starts off; each mode runs its correct number of rounds; intro/victory videos updated.
- Manuals, physical manual, solo manual and Civilopedia (PDF + DOCX, PT/EN/ES) plus the in-game tutorial regenerated with the updated values; many PT/EN/ES translations.

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
