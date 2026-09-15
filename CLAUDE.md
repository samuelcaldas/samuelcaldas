# Repository guidance

## Repository purpose

This is Samuel Caldas's GitHub profile repository (`samuelcaldas/samuelcaldas`).
It contains no application code or local build/test framework.
GitHub renders `README.md` on the account's profile page.

## Structure

- `README.md` — Portuguese biography, contact links and profile widgets.
  Images use github-readme-stats, github-readme-streak-stats, skillicons.dev,
  shields.io and komarev.com. Account-specific widgets use `samuelcaldas`.
  The activity link opens GitHub's native profile instead of an external graph.
- `.github/workflows/cobrinha.yml` — "Generate Datas" uses the SVG-only
  `Platane/snk` action and publishes to `output` with
  `crazy-max/ghaction-github-pages`, preserving history and skipping empty commits.
  The account comes from `github.repository_owner`; actions use immutable SHAs.
- `LICENSE` — MIT license; preserve the copyright attribution.

## Automation state

The snake workflow is manually disabled on GitHub. Its configuration offers
manual dispatch and a schedule at minute 17 every 12 hours (UTC), but must remain
disabled unless the owner explicitly requests restoration. Do not dispatch it or
add its image to the README as part of profile maintenance.

## Validation

Preserve the Portuguese biography and contact URLs. Adapt only GitHub widget
identities when copying the profile; never substitute another account's data.
Omit a language card when its provider reports no language data.

Run pinned actionlint and Markdown lint tools through the `docker-dev` context,
plus `git diff --check`. Allow deliberate inline HTML, long widget URLs and the
profile's heading placement when linting Markdown. Check embedded image HTTP
responses and SVG contents; an HTTP 200 error card is not a successful widget.
Preview GitHub Markdown on desktop and mobile before publication. Keep all
screenshots in gitignored `.playwright-mcp/` directories. Static workflow
validation does not require enabling or executing the workflow.
