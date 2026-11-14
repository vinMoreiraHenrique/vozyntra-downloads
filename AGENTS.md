# Vozyntra download-channel context

## Purpose and current state

This public repository distributes Vozyntra installers for Linux and Windows. Application development happens in a separate private source repository. The channel was initialized on 14 November 2026. The first compiled public installer release is pending.

The app's startup-update feature is being implemented in source branch `feat/startup-update-checks`. It checks this repository's latest stable GitHub release asynchronously, selects the platform ZIP, and offers a download. Users can disable automatic checks or request a fresh check in Settings. Confirm source PR state before reporting delivery.

## Publication rules

- Keep technical documentation, branches, and Conventional Commits in English. Provide English and Brazilian Portuguese installation instructions for users.
- Use focused branches and PRs for maintenance changes. Return PR links to the user for review and merging.
- Publish only user-approved, verified installer artifacts, release notes, checksums, and distribution documentation.
- The existing private-source ZIPs include Python source files. Public publication requires a compiled distribution build and verification that original Python files, private project material, credentials, recordings, and personal configuration are excluded.
- Build and validate Windows artifacts on Windows and Linux artifacts on Linux. Record actual system versions and remaining acceptance checks.
- Stable release tags use `vMAJOR.MINOR.PATCH`. The updater expects `Vozyntra-MAJOR.MINOR.PATCH-Linux.zip` and `Vozyntra-MAJOR.MINOR.PATCH-Windows.zip`.
- Include `SHA256SUMS.txt`, the recorded private build revision, and a concise validation report. Confirm archive hashes and source-to-build provenance before publication.
- Preserve original media, summaries, transcripts, settings, and shared AI tools through the installer update process. Installation and downloads follow the user's existing authorization requirements.

## Resuming maintenance

Read this file and README.md, then inspect the current branches and GitHub Releases. Coordinate the release version with the private project's maintainer. Keep this status concise and current after publication. Publication of an installer is a separate action from merging its source PR.
