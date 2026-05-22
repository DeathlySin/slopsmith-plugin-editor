# Changelog

All notable changes to the Arrangement Editor plugin are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.0] - 2026-05-22

### Added
- **Tempo Map editor** — an EOF-style mode for fitting the song-wide beat
  grid to the audio. A new **🎵 Tempo Map** toolbar button (works on both
  sloppak and PSARC) swaps the canvas to a tempo view: the waveform plus a
  draggable vertical "sync-point" pole at every measure downbeat, with each
  measure's BPM and time signature derived from sync-point spacing.
  - **Drag** a sync point to retime — only the two adjacent measures
    recompute their BPM; every other measure stays put.
  - **Insert / delete** sync points (right-click menu, or the Insert /
    Delete keys) to split or merge measures.
  - **Time signature** — `[` / `]` (or the right-click menu) change the
    selected measure's beats-per-measure; the interior grid re-subdivides.
  - **Notes ride the grid** with a user-selectable scope: a "Notes that
    ride the grid" toggle chooses **Drum tab only** (default — never
    disturbs a guitar/bass/keys chart) or **All instruments** (full
    retempo). The beat grid and section markers always move regardless.
    The choice persists in `localStorage`.
  - A dimmed reference layer shows the current arrangement's notes and the
    drum-tab hits at their absolute times, so the grid can be aligned to
    them and the waveform.
  - Every edit is a single undo step (Ctrl+Z / Ctrl+Y).
