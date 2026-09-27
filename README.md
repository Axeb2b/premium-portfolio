# premium-portfolio

A central portfolio repo for organizing, standardizing, and consolidating Axeb2b's public work.

This repo documents the cleanup plan, the active canonical projects, the consolidation candidates, and the quality bar for premium repositories.

## Mission

- Merge or consolidate overlapping repositories only after validating build and runtime compatibility.
- Remove dead or redundant code only when it is proven to be unused and disposable.
- Upgrade each active repo to premium standards: docs, tests, security, CI, and maintainable structure.
- Archive stale or duplicate repos instead of deleting them abruptly.

## Active repository strategy

### Canonical repos
- Axeb2b/MINTO.uno
- Axeb2b/Wsng
- Axeb2b/exoincdeep
- Axeb2b/apk-signer

### Consolidation candidates
- Axeb2b/minto + Axeb2b/MINTO.uno + Axeb2b/mintouno
  - Keep one canonical frontend.
  - Merge compatible code and features only after code review.
- Axeb2b/Wsng + Axeb2b/wsngpannel
  - Keep a single product repo and archive the empty clone if it adds no unique value.
- Axeb2b/apk-bot + Axeb2b/apk-download-redirect
  - Combine only if the redirect logic is genuinely part of the bot's workflow and not a separate utility or landing page.

### Review before archive
- Axeb2b/aezee
- Axeb2b/cloaking-bot
- Axeb2b/tgbotb
- Axeb2b/kilocode
- Axeb2b/Parivahan-Panel-Sync
- Other low-activity or one-off experiments

Do not archive based only on repo names or inactivity. Every archive decision should be backed by source review, build status, and a migration note.

## Roadmap

### Phase 1: Inventory and quality baseline
- audit every public repo
- validate active work and branches
- identify duplicates and stale projects
- document migration notes for any merge candidates

### Phase 2: Canonical repo standardization
- clean README and project overview
- install a consistent folder structure
- add env example files
- standardize scripts and config
- document security and deployment steps

### Phase 3: Quality bars
- CI: lint, test, typecheck, build
- dependency hygiene and lockfile management
- security scanning and secret checks
- code review standards and PR flow

### Phase 4: Consolidation and archive
- merge compatible repos
- remove unused branches carefully
- archive dead or replaced repos
- keep redirects and migration notes

## Premium repo checklist

Every active repo should include:

- clear product explanation and use cases
- consistent README structure
- LICENSE
- CONTRIBUTING.md
- SECURITY.md
- CHANGELOG.md
- .env.example
- project-specific docs folder
- accessible, production-quality frontend/UI patterns
- typed config and environment validation
- tests, linting, and build checks
- no secrets or generated artifacts committed
- clean dependency graph

## Documentation

- [Repo audit](./docs/repo-audit.md)
- [Premium standards](./docs/premium-standards.md)
- [Cleanup roadmap](./docs/cleanup-roadmap.md)

## Next actions

1. Review `MINTO.uno`, `minto`, and `mintouno` for actual overlap.
2. Review `Wsng` and `wsngpannel` for duplicate app structure.
3. Review `apk-bot` and `apk-download-redirect` before merging.
4. Create a standard README template for all active repos.
5. Archive only repos with confirmed replacement or no meaningful active source.

## Important note

The objective is to improve the portfolio without destroying working historical repos. Consolidation should be evidence-based, and any archiving should include a migration notice and the original repository preserved for reference.
