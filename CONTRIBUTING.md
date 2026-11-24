# Contributing to MeetCite

How Group 8 works on MeetCite so that every change is reviewed, tested and **credited to the person who made it**.
The full step-by-step guide, including the project board, is [docs/DEVELOPMENT_WORKFLOW.md](docs/DEVELOPMENT_WORKFLOW.md).
Who owns what is in [docs/TEAM_RESPONSIBILITIES.md](docs/TEAM_RESPONSIBILITIES.md).
After each merge, GitHub Actions shows the PR author and change in the run summary. See [Team contribution activity](docs/CONTRIBUTION_ACTIVITY.md).

## Rules

1. **Use your own GitHub account**, with your own name and email in Git. Never commit for someone else, and never
   change author names or dates.
2. **Every change goes through a pull request.** `main` is protected: one approval and passing CI are needed.
3. **Start from an issue.** It must have an owner, a description and completion criteria (use the issue templates).
   Link it in the pull request with "Closes #N".
4. **One topic per pull request.** Small pull requests get reviewed faster.
5. **Say if you used AI.** Fill in the "AI assistance" section of the pull request template. Using AI is allowed;
   hiding it is not. You must understand and be able to explain everything you submit.
6. **Never commit secrets or personal data:** no `.env` files, keys, recordings, databases, or documents with
   student IDs. Check `git status` before every commit.

## One-time setup

```bash
git clone https://github.com/icon1210/meetcite-contribution-flow.git
```

```bash
cd meetcite
```

```bash
git config user.name "Your Full Name"
```

```bash
git config user.email "ID+username@users.noreply.github.com"
```

Copy the noreply address from GitHub → Settings → Emails. Then follow "Running it locally" in the
[README](README.md).

## Branch names

`feature/…`, `fix/…`, `docs/…`, `test/…`, `research/…`. Examples: `feature/export-system`, `fix/mobile-layout`.

## Commit messages

Use the imperative mood and say what the change does: `Add MOV and MKV to accepted upload types`.
Avoid messages like `update` or `final fix 2`.

## Before opening a pull request

```bash
cd backend && ruff check app tests && ruff format --check app tests && mypy app && pytest -q
```

```bash
cd frontend && npm run lint && npm run typecheck && npm test && npm run build
```

```bash
cd frontend && npx playwright test
```

For the last one (browser tests), stop the local API on port 8000 first.

## Reviewing

* Pull the branch and try it.
* Make sure you understand the code; ask if not.
* Check the tests and that no secrets are included.
* Comment specifically and kindly, then **Approve** or **Request changes**.

## After merging

Add your pull request to [CONTRIBUTORS.md](CONTRIBUTORS.md), [docs/TEAM_CONTRIBUTIONS.md](docs/TEAM_CONTRIBUTIONS.md)
and the `Unreleased` section of [CHANGELOG.md](CHANGELOG.md). Releases follow
[docs/RELEASE_PROCESS.md](docs/RELEASE_PROCESS.md).
