# Cleanup & Consolidation Roadmap

## Executive Summary

Consolidate overlapping repositories, remove dead code, standardize active projects to premium quality, and establish a maintainable portfolio.

**Timeline:** 2 weeks
**Repos to Consolidate:** 6
**Repos to Archive:** 9+
**Repos to Upgrade:** 8

---

## Phase 1: Audit & Review (Days 1-2)

### 1.1 Inspect Consolidation Candidates

#### MINTO Cluster
- [ ] Clone and review `Axeb2b/minto` source
  - Identify: Web3 components, hooks, utilities
  - Check: Dependencies, build compatibility with MINTO.uno
  - Decision: Extract and merge compatible code
- [ ] Confirm `Axeb2b/mintouno` is empty
  - If empty: Schedule for archive
  - If not: Audit and extract any unique code

#### WSNG Cluster
- [ ] Review `Axeb2b/Wsng` source
  - Identify: Generator boilerplate vs. real code
  - Check: What's custom logic vs. default Vite template
  - Decision: Keep and enhance, archive duplicate
- [ ] Confirm `Axeb2b/wsngpannel` is empty or duplicate
  - If empty: Archive with migration notice

#### APK Cluster
- [ ] Review `Axeb2b/apk-bot`
  - Identify: Bot implementation, dependencies, scope
  - Decision: Keep or merge with redirect
- [ ] Review `Axeb2b/apk-download-redirect`
  - Identify: What does it redirect? Is it part of bot workflow?
  - Decision: Merge if related, keep separate if standalone utility

#### Exoincs Cluster
- [ ] Confirm `exoincs-bot` has no real code (24 bytes)
- [ ] Confirm `exoincslogs` has no real code (24 bytes)
- [ ] Keep `exoincdeep` active

### 1.2 Review Dead Repos

For each repo without activity or clear purpose, create an archive plan:
- [ ] tgbotb
- [ ] cloaking-bot
- [ ] aichat
- [ ] codebhai-
- [ ] device-panel
- [ ] kilocode
- [ ] workflows-starter-template
- [ ] Others from Category C

---

## Phase 2: Consolidation (Days 3-6)

### 2.1 MINTO Consolidation

```bash
# Step 1: Create feature branch in MINTO.uno
git checkout -b feat/consolidate-minto-variants

# Step 2: Extract code from minto repo
# (Review, refactor for compatibility)

# Step 3: Integrate into MINTO.uno structure
src/
  ├── features/
  │   ├── dashboard/
  │   ├── wallet/
  │   ├── defi/          # Web3 components from 'minto'
  │   └── analytics/

# Step 4: Update dependencies and build
npm install && npm run build

# Step 5: Create PR, review, merge
# Step 6: Archive 'mintouno' with migration notice
```

### 2.2 WSNG Consolidation

```bash
# Step 1: Clean up Wsng repo
# Remove Vite template boilerplate, keep custom code

# Step 2: Create proper structure
src/
  ├── components/
  ├── pages/
  ├── services/
  ├── types/
  └── App.tsx

# Step 3: Update README with real product info
# Step 4: Archive wsngpannel with redirect
```

### 2.3 APK Consolidation (Decision Tree)

**If apk-bot and apk-download-redirect are related:**
```
packages/
  ├── bot/              # Core bot logic
  ├── download-redirect/ # Redirect module
  └── shared/           # Shared utilities
```

**If independent:**
- Keep both separate
- Add proper READMEs to each
- Link them in premium-portfolio

### 2.4 Archive Dead Repos

For each repo being archived:

1. Create an archive branch
2. Add ARCHIVE.md with:
   ```markdown
   # This repository has been archived
   
   This project is no longer actively maintained.
   
   **Reason:** [Low activity / Superseded by X / Not viable]
   **Last Update:** [date]
   **Successor:** [if applicable]
   
   If you need this code, check the commit history or contact [email].
   ```
3. Push ARCHIVE.md to main branch
4. Archive the repository via GitHub Settings
5. Update premium-portfolio with a link to the archived repo

---

## Phase 3: Standardization (Days 7-10)

For each **active repository**, apply premium standards:

### 3.1 Documentation
- [ ] Write comprehensive README (use template)
- [ ] Add CONTRIBUTING.md
- [ ] Add SECURITY.md
- [ ] Create/update CHANGELOG.md
- [ ] Add .env.example
- [ ] Add LICENSE if missing

### 3.2 Code Quality
- [ ] Set up ESLint/Prettier
- [ ] Add TypeScript (if not already)
- [ ] Run type checks in CI
- [ ] Remove dead code
- [ ] Clean up unused dependencies

### 3.3 Testing & CI
- [ ] Add test suite
- [ ] Set up GitHub Actions workflow
  - Lint
  - Type check
  - Test
  - Build
- [ ] Enable branch protection
- [ ] Set up Dependabot

### 3.4 Security
- [ ] Enable CodeQL scanning
- [ ] Audit dependencies
- [ ] Review for secrets
- [ ] Add security.md policy

### 3.5 Cleanup
- [ ] Remove unused branches
- [ ] Clean up stale issues/PRs
- [ ] Update repository topics
- [ ] Add repository description

---

## Phase 4: Portfolio Hub (Days 11-12)

### 4.1 Update premium-portfolio

```markdown
# Portfolio Status

## Active Projects (Canonical)
- ✅ MINTO.uno - DeFi Dashboard
- ✅ Wsng - Web Panel Framework
- ✅ apk-signer - APK Signing Utility
- ✅ exoincdeep - ML/Deep Learning Library
- ✅ durable-chat-template - Chat Template
- ✅ hardware-brutalist-hero - Hardware Showcase
- ✅ harryAXE- - Backend API
- ✅ Parivahan-Panel-Sync - Panel Sync Tool

## Archived Repositories
- 🗂️ mintouno (merged into MINTO.uno)
- 🗂️ wsngpannel (merged into Wsng)
- 🗂️ exoincs-bot (superseded)
- 🗂️ exoincslogs (superseded)
- ... [list all with reasons]

## Standards Applied
- ✅ Professional READMEs
- ✅ CI/CD pipelines
- ✅ Security scanning
- ✅ Dependency management
- ✅ Test coverage
- ✅ Documentation
```

### 4.2 Create Project Board

Use GitHub Projects to track:
- Repository audit status
- Consolidation progress
- Standardization checklist
- Archive decisions

---

## Phase 5: Verification (Days 13-14)

- [ ] All active repos have green CI checks
- [ ] All archived repos have proper notices
- [ ] Portfolio hub is up to date
- [ ] No secrets leaked in consolidation
- [ ] All documentation is complete
- [ ] Test coverage ≥ 70% for active projects
- [ ] No broken links in README/docs
- [ ] Dependencies are current and secure

---

## Post-Cleanup Maintenance

### Monthly
- [ ] Review open issues and PRs
- [ ] Update dependencies
- [ ] Check security vulnerabilities

### Quarterly
- [ ] Audit repository activity
- [ ] Review code quality metrics
- [ ] Update documentation

### Annually
- [ ] Archive underutilized projects
- [ ] Evaluate new consolidation opportunities
- [ ] Update premium standards if needed

---

## Success Metrics

- [ ] 100% of active repos have premium standards
- [ ] 0 dead repos cluttering portfolio
- [ ] All consolidations documented with migration guides
- [ ] CI/CD passing on all active repos
- [ ] Security scanning enabled everywhere
- [ ] Documentation complete and clear
- [ ] Portfolio hub accurately reflects status
