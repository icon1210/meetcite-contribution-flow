# MeetCite roadmap

What is finished and what is planned. Nothing in "Planned" is built yet. Owners are the Group 8 members assigned
to each area; see [TEAM_CONTRIBUTIONS.md](TEAM_CONTRIBUTIONS.md).

## Completed (version 0.6.0, November 2026)

**Capture and transcripts**
* Upload and in-browser recording.
* Speaker-labelled transcript and speaker name suggestions.
* Live captions with quick notes.

**Minutes and evidence**
* C1 (plain) and C2 (cited) minutes, decisions and action items.
* The AI check (supported, partly supported, not supported) and human claim review.
* "Ask" questions about a meeting.

**Follow-up**
* Series memory: open actions carried over, and changed decisions flagged.
* Agenda coverage, follow-up email, calendar reminders.
* TXT, DOCX and PDF exports.

**App and operations**
* Dashboard with a "needs attention" panel.
* Layout that fits every screen.
* Sign-up code and login rate limit.
* Live deployment with HTTPS and nightly backups.
* CI, plus 85 backend, 34 unit and 6 browser tests.

## Short term (before the dissertation deadline)

| Area | Planned work | Owner |
|---|---|---|
| Research | Ethics approval, then the user study (SUS and tasks) | Chinonye, with the group |
| AI summarisation quality | C1 vs C2 evaluation on the AMI corpus: unsupported-claim rate, human labels, Cohen's kappa | Pascal, Olayinka |
| Transcription accuracy | Measure word error rate and speaker error on AMI; tune alignment | Pascal |
| Media | Accept MOV and MKV uploads | Emmanuel |
| Data protection | In-app account deletion; written retention policy | Kenneth |
| Testing and reliability | Uptime check and error alerts; load test on the VPS | Emmanuel |
| Accessibility | WCAG 2.2 AA audit and fixes | Olayinka, Chinonye |
| Exports | Supervisor-meeting minutes in the UWS template | Chinonye |
| Process | All changes through reviewed PRs; first team release (0.7.0) | Everyone |

## Medium term (after submission)

* **Evidence verification:** show *why* a claim was flagged, and let reviewers fix the claim inline.
* **Performance:** faster local mode on CPU-only servers; queue several jobs at once.
* **Backups:** off-server, encrypted copies.
* **User experience:** shared team workspaces; search across meetings.
* **Data protection:** a data processing agreement and an EU data region for cloud mode.

## Long term (product goals)

* **Scalability:** PostgreSQL and object storage; more than one worker server.
* **Integrations:** calendars and video platforms (bring recordings in automatically).
* **Languages:** support beyond English.
* **Pilot:** real teams and organisations, with consent, measuring time saved and errors caught.
* **Independent review:** security and accessibility testing by outside reviewers.

Reaching **1.0.0** means the user study is complete and the known short-term gaps above are closed.
