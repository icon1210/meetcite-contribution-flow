# MeetCite project history

This page separates the product's earlier release history from the history of this public repository. The project milestones below come from the original repository, [`icon1210/meetcite`](https://github.com/icon1210/meetcite), which is private. The commit and tag links require access to that repository.

## Releases in the original repository

The project record maps the original tags to these product versions. The tag names are preserved as they were created, including the early `v1.x` names that do not match the semantic version numbers in the first column.

| Product version | Original tag | Commit date | Main commit | Milestone |
|---|---|---|---|---|
| 0.1.0 | [`v0.1-prototype`](https://github.com/icon1210/meetcite/tree/v0.1-prototype) | 13 Oct 2026 | [`cc4aaca`](https://github.com/icon1210/meetcite/commit/cc4aacacaab962457889838cbf8db9ee49e6e2d9) | First working prototype: meeting upload, transcripts, cited minutes, decisions, actions and the AI check. The prototype was prepared before Git history began. |
| 0.2.0 | [`v0.2-meetcite`](https://github.com/icon1210/meetcite/tree/v0.2-meetcite) | 13 Oct 2026 | [`38b95de`](https://github.com/icon1210/meetcite/commit/38b95de906190c82fba3044a7fab9bd5ad02e707) | Renamed from MeetMind to MeetCite; group documents and recordings were kept out of the server package. |
| 0.3.0 | [`v1.0-live`](https://github.com/icon1210/meetcite/tree/v1.0-live) | 20 Oct 2026 | [`bed2b35`](https://github.com/icon1210/meetcite/commit/bed2b35fd8a9ba3c67ff5d5c476b0c733634d3b8) | First deployment, HTTPS and nightly backups. |
| 0.4.0 | [`v1.1-responsive`](https://github.com/icon1210/meetcite/tree/v1.1-responsive) | 20–21 Oct 2026 | [`ec742a1`](https://github.com/icon1210/meetcite/commit/ec742a195c93b4d4c51ede5fcf52b5fa487dc548) | Fixed phone layout problems and added checks across 11 screen widths. |
| 0.5.0 | [`v1.2-attention`](https://github.com/icon1210/meetcite/tree/v1.2-attention) | 21 Oct 2026 | [`9bc1d36`](https://github.com/icon1210/meetcite/commit/9bc1d367d1061b618728ada845d16bd882e622f2) | Added the dashboard's “Needs attention” panel and filter. |
| 0.6.0 | [`v1.3-ethics-ready`](https://github.com/icon1210/meetcite/tree/v1.3-ethics-ready) | 21 Oct 2026 | [`7ba24b3`](https://github.com/icon1210/meetcite/commit/7ba24b31003f4e06ee16b717d40e12304504b254) | Redesigned the proposed usability study so participants are not recorded; ethics approval is still required before the study starts. |

The original project record credits Olayinka Williams Ajibola (`icon1210`) with directing and implementing releases 0.1.0–0.6.0. It also states that Claude Code was used extensively to generate and refine the code. The project aims, product choices, testing priorities and deployment decisions were human-led. The other members' assigned areas are documented in [team contributions](TEAM_CONTRIBUTIONS.md); an assigned role alone is not evidence that code was shipped. Work outside Git should be recorded with its own evidence.

## This repository

The public `meetcite-contribution-flow` repository was created on 24 Nov 2026 from a ZIP of the project. That ZIP did not include `.git`, so the earlier commits and tags are not part of this repository's Git history. The initial GitHub commits identify the account that created the repository and uploaded the snapshot; they do not reconstruct who authored each earlier file.

The uploaded application is still version **0.6.0**. The 24 Nov snapshot is a repository import, not a new product release. Future work will use issues, branches and reviewed pull requests. When a pull request is merged, the **Show merged contribution** workflow displays the author and change in the GitHub Actions run summary. See [the development workflow](DEVELOPMENT_WORKFLOW.md) and [release process](RELEASE_PROCESS.md).

## Planned milestones

These are plans from the project record, not releases:

- **0.7.0:** first team pull requests.
- **0.8.0:** AMI evaluation results.
- **1.0.0:** after ethics approval and the user study with real users.

