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
Currently no remote is configured. To add a remote:
```bash
git remote add origin <repository-url>
git push -u origin main
```

## Claude Runner Notes
- Repository is ready for coding tasks
- All future TabZen development should use this canonical path
- Previous fallback to `/root/repos` should no longer be necessary
