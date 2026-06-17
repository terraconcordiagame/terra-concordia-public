# Release Notes

All notable changes to Terra Concordia are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/).

---

## [Unreleased]

Future release notes will appear here.

---

## [1.1.0] — 2026-06-17

First post-launch update.

### Added
- **In-game version notes:** Help → "Version notes & latest updates" opens a PDF (PT/EN/ES) with the fix/update history.
- **Main menu buttons:** "Manuals & Website" (opens `ncbgames.com/manuals`) and "Discord invite".
- **3 new procedural music tracks** — Serene, Epic, Mystic — selectable in Settings → Sounds (new-player default: Mystic).
- **Version + build-date badge** on out-of-game screens.

### Fixed
- **End-of-game videos:** victory video only for the winner; defeat/collapse video for everyone who lost (any mode). Fixes the solo case that showed the victory video on a loss.
- **Victory achievements only unlock on an actual win** — not on a solo-scenario loss, a loss to another player, or ecological collapse.
- **Videos no longer play over music/SFX** — audio is muted while a video plays and restored afterward.
- **Multiplayer:** turn timer respects disconnect pauses (no more auto-passing under a dropped player); residual match state (discard/timeline) resets each new game; the winner uses the full ranking (host/guest aligned); anti-cheat discard validation; clearer alliance-error feedback; ecological collapse ignores players who left.
- **Achievements:** "Hard Mode Win" requires AI in the match; "4p Diplomacy" uses the initial human count; MP counters no longer inflate on the end screen.
- More translations (HUD, sustainability alerts, end-of-game warnings, history log).

### Changed
- Global Sustainability bar slightly taller; Settings window much wider.
- New-player defaults: SFX 80%, music 30%, Mystic track, Slow animation speed, intro video on.

### Animations
- Floating resource/sustainability numbers, worker "pop" on placement, animated hex reveal, pulsing ring on the active player + glow on the selected action, and shake (critical zone) / spark (at 10) on the Sustainability bar. Unexplored hexes now show a "locked" look (embossed padlock with a subtle shimmer).

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
