# Release process

## Versioning

MeetCite uses [semantic versioning](https://semver.org): `MAJOR.MINOR.PATCH`.

| Part | When it goes up | Example |
|---|---|---|
| MINOR | New features | 0.7.0 adds MOV/MKV uploads |
| PATCH | Fixes only | 0.7.1 fixes an export bug |
| MAJOR | 1.0.0 = first stable release; later, breaking changes | — |

**1.0.0** is reserved until the user study is complete and the short-term items in [ROADMAP.md](ROADMAP.md) are
closed.

Tags from now on are named `vMAJOR.MINOR.PATCH` (e.g. `v0.7.0`). The six earlier tags (`v0.1-prototype` …
`v1.3-ethics-ready`) keep their original names. Their semantic versions (0.1.0–0.6.0) are given in
[VERSION_HISTORY.md](VERSION_HISTORY.md) and on their GitHub Releases. No tag is ever backdated or moved, except
during the documented student-ID removal on 13 November 2026.

## Who

The **repository owner** (icon1210) and the **deployment owner** (Emmanuel) create releases and deploy. The
**Group Lead** agrees what goes into each release.

## Steps

1. **Scope.** All pull requests for the release's milestone are merged, and CI on `main` is green.
2. **Changelog.**
   * In a pull request, move the `Unreleased` items in [CHANGELOG.md](../CHANGELOG.md) under the new version and
     date.
   * Each line names its pull request and author, for example `Accept MOV and MKV uploads (#14, @username)`.
   * Add a matching section to [VERSION_HISTORY.md](VERSION_HISTORY.md), with test results and known limitations.
3. **Tag.** After that pull request merges:

   ```bash
   git switch main
   ```

   ```bash
   git pull
   ```

   ```bash
   git tag -a v0.7.0 -m "MeetCite 0.7.0"
   ```

   ```bash
   git push origin v0.7.0
   ```

4. **GitHub Release.** Create it from the tag, using the changelog section as the notes:

   ```bash
   gh release create v0.7.0 --title "MeetCite 0.7.0" --notes-file notes.md
   ```

   "Generate release notes" on GitHub lists every merged pull request and its author, which is a good check.
5. **Deploy.** Run the update command on the server, as in [DEPLOYMENT.md](DEPLOYMENT.md):

   ```bash
   cd /opt/meetcite && git pull && docker compose -f docker-compose.cloud.yml up -d --build
   ```

   Then check that https://meetcite.com.ng loads, sign-in works and a short test upload completes.
6. **Close** the milestone and move its cards to Done.

## Hotfixes

For an urgent fix on the live site:
1. Branch `fix/…` from `main` and open a pull request as usual. Review can be quick but is still required.
2. Release it as a PATCH version (e.g. `v0.7.1`).

## Rolling back

Run this on the server:

```bash
cd /opt/meetcite && git checkout v0.7.0 && docker compose -f docker-compose.cloud.yml up -d --build
```

If data is affected, restore the latest backup ([DEPLOYMENT.md](DEPLOYMENT.md) §7). Afterwards, fix the problem on
`main` through a pull request.
