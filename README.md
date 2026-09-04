# RRR-CRM Releases

Public release channel for **RRR-CRM / Richard RaceRoom Crew Manager**.

This repository intentionally contains **release artifacts only**. The application source code and development history remain in the private development repository.

## Stable release contract

The normal installed RRR-CRM client only consumes published stable GitHub Releases from this repository via `releases/latest`.

Each installable release must contain both files with exactly matching version numbers:

- `RRR-CRM_Setup_<version>.exe`
- `RRR-CRM_Setup_<version>.exe.sha256`

Example:

- `RRR-CRM_Setup_1.0.0.exe`
- `RRR-CRM_Setup_1.0.0.exe.sha256`

The `.sha256` file must contain either the 64-character SHA-256 hex value only, or the common format:

`<sha256>  RRR-CRM_Setup_<version>.exe`

## Release rules

- Stable releases only for the normal update channel.
- Do not mark production releases as GitHub pre-releases.
- Do not use version suffixes such as `-beta`, `-preview` or `-rc` for the stable channel.
- Publish release notes describing user-visible changes and any migration notes.
- Never publish source-code secrets, GitHub tokens or private repository data here.

## Integrity

RRR-CRM verifies the downloaded installer against the matching SHA-256 asset before installation. Missing, malformed or mismatching checksums cause the update to fail closed: the installer is not started.
