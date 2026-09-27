# Repository Audit Report

## Summary
**Total Repos:** 37 (32 public, 5 private)
**Active Projects:** 8
**Consolidation Candidates:** 6
**Dead/Low-Priority:** 23
**Org Repos:** 2

---

## Category A: Active, Production-Ready (Upgrade & Feature)

### 1. MINTO.uno (Canonical)
- **Status:** Active, Featured
- **Language:** JavaScript
- **Type:** Frontend DeFi Dashboard
- **Last Update:** Sept 11, 2026
- **Size:** 130 bytes
- **Action:** 
  - Keep as primary
  - Merge compatible code from `minto` and `mintouno`
  - Add comprehensive docs, tests, CI/CD
  - Deploy to production domain

### 2. Wsng (Canonical)
- **Status:** Active, Generator Output
- **Language:** TypeScript
- **Type:** Web Panel (React + Vite)
- **Last Update:** Sept 25, 2026 (2 days)
- **Size:** 56 bytes
- **Action:**
  - Clean up generator output and boilerplate
  - Archive `wsngpannel` (empty clone)
  - Add real business logic and API contracts
  - Establish CI/CD pipeline

### 3. apk-signer (Standalone)
- **Status:** Active
- **Language:** Python
- **Type:** Utility
- **Last Update:** June 2026
- **Action:**
  - Keep independent (security sensitive)
  - Add docs and tests
  - Create pip package if not already

### 4. exoincdeep (Standalone)
- **Status:** Active
- **Language:** Python
- **Type:** ML/Deep Learning
- **Last Update:** June 2026
- **Action:**
  - Document use cases and examples
  - Add requirements.txt and setup.py
  - Add CI for Python 3.9, 3.10, 3.11

### 5. durable-chat-template (Template)
- **Status:** Template/Reference
- **Language:** TypeScript
- **Type:** Starter kit
- **Action:**
  - Mark as template repo
  - Add comprehensive setup guide
  - Ensure dependencies are current

### 6. hardware-brutalist-hero (Standalone)
- **Status:** Production Project
- **Language:** TypeScript
- **Type:** Hardware showcase
- **Description:** Hardware Brutalist hero — live preview
- **Action:**
  - Document the hardware/design
  - Add live demo link
  - Create dev setup guide

### 7. harryAXE- (Backend)
- **Status:** Active
- **Language:** TypeScript
- **Description:** new server db n management
- **Type:** Backend/API
- **Action:**
  - Rename to professional name (harryAXE → harryaxe-api or similar)
  - Add API documentation
  - Set up database migrations and scripts

### 8. Parivahan-Panel-Sync (Standalone)
- **Status:** Active
- **Language:** TypeScript
- **Description:** Repository for Replit project
- **Type:** Panel/Sync tool
- **Action:**
  - Document API contracts
  - Add deployment guide
  - Create test suite

---

## Category B: Consolidation Candidates (Review & Merge)

### 1. MINTO Variant Cluster
- **minto** (TypeScript, 65 bytes, July 17)
  - Contains: unknown (need to inspect)
  - Action: Audit code, merge with MINTO.uno if compatible

- **MINTO.uno** (JavaScript, 130 bytes, Sept 11)
  - Contains: DeFi dashboard, glass-morphism design, animations
  - Action: KEEP as canonical

- **mintouno** (Empty, July 18)
  - Contains: README only
  - Action: ARCHIVE (no code)

### 2. WSNG Variant Cluster
- **Wsng** (TypeScript, 56 bytes, Sept 25)
  - Contains: React + Vite panel generator output
  - Action: KEEP as canonical, clean up boilerplate

- **wsngpannel** (Empty, Sept 26)
  - Contains: Nothing
  - Action: ARCHIVE (duplicate)

### 3. APK Utility Cluster
- **apk-bot** (575 bytes, Aug 2)
  - Contains: unknown bot implementation
  - Action: Audit, decide if merges with redirect

- **apk-download-redirect** (24 bytes, July 20)
  - Contains: Lightweight redirect utility
  - Action: Audit, merge with apk-bot if related

- **apk-signer** (Standalone Python)
  - Contains: APK signing utility
  - Action: KEEP separate (different purpose)

### 4. Exoincs Cluster
- **exoincs-bot** (24 bytes, June 2, DEAD)
  - Action: ARCHIVE

- **exoincslogs** (24 bytes, June 2, DEAD)
  - Action: ARCHIVE

- **exoincdeep** (Active Python)
  - Action: KEEP

---

## Category C: Dead/Low-Priority (Archive)

### Definitely Archive (No Code/Activity)
1. **mintouno** - empty README
2. **wsngpannel** - empty, duplicate
3. **exoincs-bot** - no real code
4. **exoincslogs** - no real code
5. **aezee** - no description, no code
6. **faaaaaaaaah** - no description, no code
7. **AxeCodi** - Replit reference only
8. **worldliberty** - no activity (private)
9. **WHITE** - HTML static file (private)

### Review Before Archive
1. **tgbotb** (JS Bot)
2. **cloaking-bot** (JS Bot)
3. **aichat** (JS Chat)
4. **codebhai-** (Python)
5. **device-panel** (JS Panel)
6. **AxeSmsSendout** (Python, private)
7. **zpredict-2** (TS, private)
8. **kilocode** - description only
9. **gobob-exchange** (TS, private)
10. **workflows-starter-template** (TS)

### Private/Org Repos (Existing)
- alchiya-panel (Private)
- alchiya-web (Private)
- alchiyapannel (Private, Kotlin)
- parivahan-supabase-api (Private)
- axefinance-wallet/bhaikaai (Org, Private)
- axefinance-wallet/wwww (Org, Public)

---

## Cleanup Actions (Staged)

### Phase 1: Documentation & Standardization
- [ ] Create README template
- [ ] Add premium-standards.md
- [ ] Create CONTRIBUTING.md template
- [ ] Create SECURITY.md template
- [ ] Create .env.example template

### Phase 2: Audit Dead Repos
- [ ] Inspect each "dead" repo for any hidden value
- [ ] Document decision in archive notice
- [ ] Create migration guides for merged repos

### Phase 3: Consolidate & Clean
- [ ] Merge minto code into MINTO.uno
- [ ] Archive mintouno
- [ ] Archive wsngpannel
- [ ] Decide APK consolidation
- [ ] Archive exoincs-bot, exoincslogs

### Phase 4: Upgrade Active Repos
- [ ] Add CI/CD to all active repos
- [ ] Add security scanning
- [ ] Add dependency management
- [ ] Add tests and coverage
- [ ] Add proper documentation

---

## Next Steps

1. Review each consolidation candidate by inspecting actual source
2. Create PRs for cleanup, don't force-push
3. Archive repos with proper redirect notice
4. Update portfolio hub with final status
5. Document all decisions in CHANGELOG
