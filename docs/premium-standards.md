# Premium Repository Standards

Every active repository maintained by Axeb2b must meet these standards.

---

## Documentation

### README.md
- [ ] Clear project title and one-line description
- [ ] Use case and problem solved
- [ ] Links to live demo or deployed version
- [ ] Tech stack clearly listed (languages, frameworks, libraries)
- [ ] Installation / quick start section
- [ ] Configuration and environment variables (.env.example included)
- [ ] Available scripts and commands
- [ ] Project folder structure with annotations
- [ ] Contributing guidelines
- [ ] Security / responsible disclosure
- [ ] License

### CONTRIBUTING.md
- [ ] How to set up development environment
- [ ] How to run tests
- [ ] PR review process
- [ ] Code style and linting requirements
- [ ] Commit message conventions

### SECURITY.md
- [ ] Responsible disclosure policy
- [ ] How to report security issues
- [ ] Security update process
- [ ] Supported versions

### CHANGELOG.md
- [ ] Semantic versioning
- [ ] Dated entries for each release
- [ ] Links to commits and PRs

### LICENSE
- [ ] Clear license file (MIT, Apache, etc.)

---

## Code Quality

### Type Safety
- [ ] TypeScript or equivalent type checking enabled
- [ ] No `any` types without explicit justification
- [ ] Type checking passes in CI

### Linting & Formatting
- [ ] ESLint (JS/TS) or equivalent
- [ ] Prettier (or Biome) for consistent formatting
- [ ] No linting errors in CI
- [ ] Pre-commit hooks configured

### Testing
- [ ] Unit tests for core business logic
- [ ] Integration tests for APIs/workflows
- [ ] Coverage target: ≥ 70%
- [ ] Tests pass in CI
- [ ] Test suite documented

### Security
- [ ] No secrets or API keys committed
- [ ] Dependabot or equivalent enabled
- [ ] Security scanning (CodeQL or similar)
- [ ] No high-severity vulnerabilities

---

## Project Structure

### Standard Folder Layout
```
project/
├── src/                  # Source code
│   ├── components/       # Reusable components (if applicable)
│   ├── services/         # Business logic and utilities
│   ├── types/            # TypeScript types/interfaces
│   └── index.ts          # Entry point
├── tests/                # Test suite
├── docs/                 # Project documentation
├── .github/
│   └── workflows/        # GitHub Actions CI/CD
├── public/               # Static assets (if applicable)
├── .env.example          # Template environment variables
├── .gitignore            # Gitignore (no generated files)
├── package.json          # Dependencies and scripts
├── tsconfig.json         # TypeScript config (if applicable)
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── CHANGELOG.md
├── LICENSE
└── .eslintrc.json        # Lint config (if applicable)
```

---

## Build & Deployment

### Package Management
- [ ] package-lock.json or yarn.lock committed
- [ ] Version pinning where necessary
- [ ] Regular dependency updates (weekly or biweekly)
- [ ] No vendored node_modules or equivalent

### Build Process
- [ ] `npm run build` produces optimized output
- [ ] Build artifacts are reproducible
- [ ] Build passes in CI
- [ ] Clear build output documentation

### Deployment
- [ ] Clear deployment instructions
- [ ] Environment-specific config separation
- [ ] Database migration procedures (if applicable)
- [ ] Rollback strategy documented
- [ ] Monitoring/health check setup

---

## GitHub Configuration

### Repository Settings
- [ ] Description filled in (not null)
- [ ] Topics/tags appropriate to the project
- [ ] Branch protection rules on default branch
  - [ ] Require PR review before merge
  - [ ] Require status checks to pass
  - [ ] Dismiss stale PR reviews
- [ ] Squash merge enabled (optional but recommended)
- [ ] Delete branch on merge enabled

### CI/CD Pipeline
- [ ] Lint check runs on PR
- [ ] Type check runs on PR
- [ ] Tests run on PR
- [ ] Build check runs on PR
- [ ] Security scanning enabled

### Branch Strategy
- [ ] Main/master branch is production-ready
- [ ] No long-lived feature branches
- [ ] Clear naming convention (feat/*, fix/*, etc.)

---

## Performance & Optimization

### Frontend
- [ ] Bundle size monitored
- [ ] Lazy loading for large components
- [ ] Image optimization (WebP, AVIF)
- [ ] Code splitting implemented
- [ ] Accessibility audit (a11y)
- [ ] Mobile-first responsive design
- [ ] Lighthouse score ≥ 80

### Backend
- [ ] API response times documented
- [ ] Database query optimization
- [ ] Caching strategy implemented
- [ ] Rate limiting configured
- [ ] Error handling and logging

---

## Versioning & Release

- [ ] Semantic versioning (MAJOR.MINOR.PATCH)
- [ ] Release notes with highlights
- [ ] GitHub releases with links to commits
- [ ] Tags for each release
- [ ] Deprecation warnings for major changes

---

## Monitoring & Maintenance

- [ ] Error tracking (Sentry or similar)
- [ ] Uptime monitoring
- [ ] Performance metrics
- [ ] Regular security audits
- [ ] Dependency audit reports
- [ ] Issue template for bug reports
- [ ] Response time SLA for issues/PRs

---

## Checklist Template

Copy and use in your repo's issue tracker:

```markdown
## Premium Repository Checklist

### Documentation
- [ ] README complete
- [ ] CONTRIBUTING.md created
- [ ] SECURITY.md created
- [ ] CHANGELOG.md created
- [ ] LICENSE file present
- [ ] .env.example provided

### Code Quality
- [ ] TypeScript enabled
- [ ] ESLint/Prettier configured
- [ ] Tests passing (≥70% coverage)
- [ ] No security vulnerabilities
- [ ] No secrets in repo

### CI/CD
- [ ] GitHub Actions workflows set up
- [ ] Branch protection rules enabled
- [ ] Security scanning active
- [ ] Dependabot configured

### Deployment
- [ ] Deployment guide written
- [ ] Environment config documented
- [ ] Rollback procedure defined
- [ ] Monitoring/alerts set up

### Optimization
- [ ] Performance benchmarks met
- [ ] Bundle size monitored
- [ ] Accessibility audit passed
- [ ] Mobile responsive tested
```
