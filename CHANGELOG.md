# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.2] - 2026-08-14

### Fixed

- Drop the table wrapper around the project cards. It rendered GitHub's markdown table borders as
  grid lines boxing each card, and the filler cell needed to pad the odd third card showed up as an
  empty bordered box. Cards are now plain inline images at 49% width, which wrap two per row on
  their own and carry no table chrome.

## [0.1.1] - 2026-08-14

### Changed

- Restore the visual repo cards in "What I'm Building", replacing the interim markdown table.
  Cards now come from `opengraph.githubassets.com` — the card GitHub itself generates for a repo
  link — so they cannot rate-limit or fail independently of GitHub, unlike the `github-readme-stats`
  instance that broke (its official deployment is currently returning 503).
- Lay the cards out two per row so three 1200x600 cards do not add ~1,300px of scroll.

## [0.1.0] - 2026-08-14

### Changed

- Replace the "What I'm Building" repo pin cards with a self-contained markdown table. The cards
  were served by a public `github-readme-stats` Vercel instance that had exhausted its GitHub API
  quota, so all four rendered as "Something went wrong! ... add an env variable called PAT_1".
- Show each project as a linked name, a one-line description, and a live star-count badge from
  shields.io, which needs no token and degrades to alt text instead of a full-width error card.

### Added

- `CHANGELOG.md` and `VERSION` to track releases of the profile README.
