# Claude Usage Tracker

> **Fork Notice:** This is a personal fork of [hamed-elfayome/Claude-Usage-Tracker](https://github.com/hamed-elfayome/Claude-Usage-Tracker).
> Before pulling upstream changes, always review the diff first:
> ```bash
> git fetch upstream && git diff HEAD...upstream/main
> ```
> Do NOT merge upstream changes without a security review of the delta.

Native macOS menu bar app for tracking Claude usage across Claude.ai, API, and CLI.

## Tech Stack
Swift, SwiftUI, Xcode, Sparkle (auto-updater disabled in this fork)

## Security Notes
- **Auto-updater disabled** — Sparkle's `startingUpdater` set to `false` to prevent network calls to upstream appcast
- **Script permissions hardened** — `~/.claude/fetch-claude-usage.swift` and `~/.claude/statusline-command.sh` set to `0o700` (owner-only) instead of `0o755`
- **Known issue**: Credentials (session keys, OAuth tokens) stored in plaintext UserDefaults instead of Keychain. The `KeychainService` exists but is unused. Architectural fix deferred.

## Build
Open `Claude Usage.xcodeproj` in Xcode and build.
