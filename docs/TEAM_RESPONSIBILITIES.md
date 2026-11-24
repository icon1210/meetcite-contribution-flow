# Team responsibilities

Who **owns** each part of MeetCite. These are **assigned responsibilities**, not completed work. Completed work
that can be checked is recorded separately in [TEAM_CONTRIBUTIONS.md](TEAM_CONTRIBUTIONS.md) and
[CONTRIBUTORS.md](../CONTRIBUTORS.md).

An owner:
* plans the work in their area as issues;
* does or coordinates that work;
* reviews pull requests that touch their area (requested automatically through `.github/CODEOWNERS`);
* keeps that area's documentation current.

| Member | GitHub | Role | Area | Main folders and files | Label |
|---|---|---|---|---|---|
| Olayinka Williams Ajibola | icon1210 | Project Design Lead; repository owner | Product direction, AI pipeline (summaries, verification, series memory), interface and UI/UX | `backend/app/pipeline/summarize_llm.py`, `verify.py`, `continuity.py`, `frontend/src/` | `area: pipeline`, `area: ui` |
| Oguanya Kenneth Ifeanyi | oguanyak (invitation pending) | Group Lead | Database, authentication, data protection, backups | `backend/app/models.py`, `backend/alembic/`, `security.py`, `routers/auth.py`, `deploy/cloud/meetcite-backup.sh` | `area: database` |
| Iloanugo Onyeka Pascal | Pasilo01 | AI Evaluation Lead | Transcription, speakers, C1 vs C2 evaluation | `pipeline/transcribe.py`, `cloud_transcribe.py`, `diarize.py`, `align.py`, `names.py`, `research/` | `area: transcription`, `area: research` |
| Emmanuel Chieji | to be confirmed | Testing, Security and Deployment Lead | Media processing, tests, CI, deployment, monitoring | `pipeline/preprocess.py`, `backend/tests/`, `frontend/e2e/`, `.github/workflows/`, `docker-compose.cloud.yml`, `deploy/` | `area: media`, `area: testing`, `area: deployment` |
| Chinonye Linda Nwanya | lillyv01 | Exports and Usability Lead | Exports, follow-up tools, usability, user study | `backend/app/export.py`, follow-up and calendar code, `research/user_study/` | `area: exports`, `area: research` |

## Current assigned issues

See the [issue list](https://github.com/icon1210/meetcite-contribution-flow/issues) and the project board. As of 13 November 2026:

| Member | Issues |
|---|---|
| Olayinka | #10 prompt versioning · #11 accessibility audit |
| Kenneth | #1 account deletion · #2 data retention *(to be assigned once he has access)* |
| Pascal | #3 transcription accuracy on AMI · #4 C1 vs C2 evaluation |
| Emmanuel | #5 MOV/MKV uploads · #6 uptime monitoring · #7 browser tests in CI *(to be assigned once he has access)* |
| Chinonye | #8 UWS supervisor-meeting export · #9 user-study materials |

## Shared responsibilities

* **Everyone:** reviews at least one teammate's pull request each week; keeps their own issues on the board up to
  date.
* **Group Lead (Kenneth):** chairs planning, agrees release scope, keeps the group's project records.
* **Repository owner (Olayinka):** repository settings, access, releases and deployment, together with Emmanuel.

Changes to this table are agreed in a group meeting and made through a pull request.
