# TabZen Repository Runbook

## Repository Bootstrap

This repository was bootstrapped on 2026-03-01 by Claude Runner for the TabZen project.

### Location
- **Canonical Path**: `/root/repos/tabzen`
- **Default Branch**: `main`

### Bootstrap Steps Performed
1. Created directory `/root/repos/tabzen`
2. Initialized git repository (`git init`)
3. Renamed default branch to `main`
4. Created initial commit with README.md

### Permissions
- Owner: root
- Permissions: rwxr-xr-x (755)
- Runner user has full read/write access

### Branch Strategy
- **main**: Primary branch for stable code
- **Feature branches**: Create from main, merge back via PR or direct merge
- **Naming convention**: `feature/<name>`, `fix/<name>`, `chore/<name>`

### Fallback Policy
If `/root/repos/tabzen` is unavailable:
1. Check if path exists and is writable
2. Verify git repository is initialized (`git status`)
3. If missing, re-bootstrap using steps above

### Remote Configuration
**Status**: Not configured (local-only repository)

The remote GitHub repository URL is not yet configured. This is a known limitation.

**Blocker**: GitHub CLI (`gh`) is not authenticated on CT130 runner.
- **Remediation Owner**: System administrator / DevOps
- **Steps to resolve**:
  1. Run `gh auth login` on the runner host
  2. Or set `GH_TOKEN` environment variable with a valid GitHub PAT
  3. Then configure remote: `git remote add origin git@github.com:<org>/tabzen.git`

**Current Behavior**: Repository functions as local-only git repo. All commits are local until remote is configured and pushed.

## Claude Runner Notes
- Repository is ready for coding tasks
- All future TabZen development should use this canonical path
- Previous fallback to `/root/repos` should no longer be necessary

## Verification Checklist
- [x] Directory exists at `/root/repos/tabzen`
- [x] Git repository initialized
- [x] Default branch is `main`
- [x] Write permissions confirmed for runner user
- [ ] Remote configured (blocked - requires GitHub auth)
- [x] Runbook documented
