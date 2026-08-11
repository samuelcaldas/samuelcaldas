# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This is Samuel Caldas's GitHub profile README repo (`samuelcaldas/samuelcaldas`). It has no application code, no build/lint/test tooling. The only rendered artifact is `README.md`, shown on the user's GitHub profile page.

## Structure

- `README.md` — profile content, in Portuguese. Uses external badge/stat services (readme-typing-svg, github-readme-stats, github-readme-streak-stats, github-readme-activity-graph, shields.io, komarev.com) that render live from the `samuelcaldas` GitHub username.
- `.github/workflows/cobrinha.yml` — GitHub Actions workflow (name "Generate Datas") that runs the `Platane/snk` snake-animation action and publishes to the `output` branch via `crazy-max/ghaction-github-pages`.

## Known issue

`.github/workflows/cobrinha.yml` still hardcodes `github_user_name: rafaballerini` — stale from before the profile was renamed to `SamuelCaldas` (see commit `eb564ee`). If touching this workflow, update the username to match, or confirm with the user whether the snake workflow is still wanted at all (README history shows a prior "Remove snake" commit `19eb748`).

## Working in this repo

Changes are almost always edits to `README.md` prose/badges or to the workflow YAML — no code to test. Preview markdown rendering before committing; verify any new badge/image URLs actually resolve.
