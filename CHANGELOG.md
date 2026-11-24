# Changelog

All notable changes to MeetCite. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and
the project uses [semantic versioning](https://semver.org). Each line from 0.7.0 onwards names its pull request
and author.

The earlier tags keep their original names: semantic version → tag in brackets. Their commit dates are below; the
tags themselves were created on 12 November 2026. More detail is in
[docs/VERSION_HISTORY.md](docs/VERSION_HISTORY.md).

## [Unreleased]

### Added
- Project documentation: architecture, development log and timeline, version history, AI usage declaration,
  roadmap, team responsibilities and contributions, development workflow, release process.
- Contribution workflow: pull request and issue templates, CODEOWNERS, Dependabot configuration.

### Changed
- Clarified that the 0.1.0–0.6.0 release records belong to the original repository; the public contribution-flow
  repository begins with a ZIP snapshot on 24 November 2026 and does not contain that earlier Git history.
- Expanded the AI-use declaration to distinguish the original project's development history from the new repository snapshot.
- `docs/MeetMind_Viva_Guides.pdf`, which contained student ID numbers, removed from the repository and its history
  (13 Nov 2026).

## [0.6.0] (`v1.3-ethics-ready`): 2026-10-21
### Changed
- User study redesigned so no participant is recorded; consent form and protocol match the ethics application.

## [0.5.0] (`v1.2-attention`): 2026-10-21
### Added
- "Needs attention" panel, filter and card reasons on the home page; `review_needed_count` and `change_count` on
  meetings.
### Fixed
- Ambiguous list name in a browser test.

## [0.4.0] (`v1.1-responsive`): 2026-10-21
### Added
- Swipeable card rows on phones; screen-size test across 11 widths.
### Fixed
- Dashboard overflow on phones; cramped series actions.

## [0.3.0] (`v1.0-live`): 2026-10-20
### Added
- Deployment at https://meetcite.com.ng with automatic HTTPS; nightly backups with restore steps.
- All Group 8 members credited on the site; README rewritten.

## [0.2.0] (`v0.2-meetcite`): 2026-10-13
### Changed
- Renamed from MeetMind to MeetCite.
### Fixed
- Group documents and recordings excluded from the server package.

## [0.1.0] (`v0.1-prototype`): 2026-10-13
### Added
- First working prototype:
  - upload and record meetings;
  - speaker-labelled transcripts;
  - C1 and C2 minutes, decisions and action items;
  - the AI check;
  - series memory;
  - live captions;
  - exports and calendar reminders;
  - dashboard;
  - local and cloud AI modes;
  - automated tests and CI.

The code to 0.6.0 was written with Claude Code, under the direction of icon1210. See
[docs/AI_USAGE_AND_DECLARATION.md](docs/AI_USAGE_AND_DECLARATION.md).

