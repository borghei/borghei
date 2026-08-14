# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0] - 2026-08-14

### Changed

- Replace the "What I'm Building" repo pin cards with a self-contained markdown table. The cards
  were served by a public `github-readme-stats` Vercel instance that had exhausted its GitHub API
  quota, so all four rendered as "Something went wrong! ... add an env variable called PAT_1".
- Show each project as a linked name, a one-line description, and a live star-count badge from
  shields.io, which needs no token and degrades to alt text instead of a full-width error card.

### Added

- `CHANGELOG.md` and `VERSION` to track releases of the profile README.
