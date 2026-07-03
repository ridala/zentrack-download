# ZenTrack

ZenTrack is a local-first desktop time tracker for client and project work.

This public repository is the download and release-notes surface for alpha releases. The application source code remains private.

## Current Release

- Version: `0.0.1 alpha`
- Release tag: `v0.0.1`
- Download page: [Latest release](https://github.com/ridala/zentrack-download/releases/latest)

## Install with Homebrew (recommended)

```sh
brew tap ridala/zentrack
brew trust ridala/zentrack
brew install --cask ridala/zentrack/zentrack
xattr -dr com.apple.quarantine /Applications/ZenTrack.app
open /Applications/ZenTrack.app
```

ZenTrack is currently unsigned and not notarized. The `xattr` command clears the macOS quarantine flag that would otherwise show a damaged-app warning for this alpha build.

To update after a new release:

```sh
brew update
brew upgrade --cask zentrack
xattr -dr com.apple.quarantine /Applications/ZenTrack.app
```

To uninstall: `brew uninstall --cask zentrack` (add `--zap` to remove app data too).

## Direct Download

Download the `.dmg` from the [latest release](https://github.com/ridala/zentrack-download/releases/latest) and drag ZenTrack into Applications.

Because the alpha build is unsigned, macOS Gatekeeper blocks the first launch of a direct download. Either:

- open **System Settings → Privacy & Security**, scroll down, and click **Open Anyway** next to the ZenTrack message, or
- clear the quarantine flag in Terminal:

  ```sh
  xattr -dr com.apple.quarantine /Applications/ZenTrack.app
  ```

## What ZenTrack Includes

- overview timer flow: start, pause, resume, stop
- clients and projects with full CRUD
- project software rules and ignored-time filtering
- history with day-grouped review, manual entries, overnight sessions, and app-usage detail
- reports with totals, by-client, by-day, and by-project rows
- CSV export from the reports page and the native menu
- tray access for timer state, open-main, and stop-timer actions
- settings for idle detection and auto-pause
- native activity tracking on macOS

## Installers

Release assets are uploaded to GitHub Releases instead of being committed into this repository.

Check the assets attached to this release tag for the actual artifacts published for this build.

### macOS

- `ZenTrack-0.0.1-macos-arm64.dmg` — Apple Silicon

## Notes

- ZenTrack is a macOS desktop app
- alpha release builds are unsigned and not notarized
- public README images use stable repo-relative paths
- this repository should never contain source code, secrets, or build caches
