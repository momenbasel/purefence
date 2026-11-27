# PureFence v0.2.4

PureSnitch is now PureFence. "Little Snitch" is a registered trademark of
Objective Development, and they asked for a name without "Snitch" so that nobody
mistakes this project for theirs. The firewall itself is unchanged.

## Changed

- The app, the helper executable, the DMG, the GitHub repository, the Homebrew
  tap and the cask are now named PureFence / `purefence`. GitHub redirects the
  old repository URLs.
- Bundle identifiers, the helper's launchd label, the `pf` anchor and the
  on-disk state under `/Library/Application Support/PureSnitch` keep their
  existing names, so rules and settings carry over on upgrade.

## Upgrading from PureSnitch

Homebrew users run:

```bash
brew update
brew upgrade --cask purefence
```

`brew update` moves the installed `puresnitch` cask to `purefence`, and the
upgrade replaces `PureSnitch.app` with `PureFence.app`. Open PureFence once
afterwards; if macOS asks again, approve the helper under System Settings >
General > Login Items & Extensions > Allow in the Background, then choose Repair
Helper if the app offers it.

DMG users: quit PureSnitch, delete `PureSnitch.app`, then drag `PureFence.app`
into `/Applications`.

## Install

```bash
brew tap momenbasel/purefence
brew trust --tap momenbasel/purefence
brew install --cask purefence
```

Or download the signed and notarized DMG below and drag PureFence into
`/Applications`.

## Current limitations

The limitations listed in the
[v0.2.2 notes](https://github.com/momenbasel/purefence/releases/tag/v0.2.2)
are unchanged.
