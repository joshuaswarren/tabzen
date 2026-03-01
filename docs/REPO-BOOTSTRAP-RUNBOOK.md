# TabZen Repository Bootstrap & Fallback Runbook

## Repository Status

**Canonical Repository Path:** `/root/repos/tabzen`

**Remote:** `git@github.com:joshuaswarren/tabzen.git`

**Default Branch:** `main`

**Current Status:** Active ✓

---

## Bootstrap Information

### CT130 Runner Setup

The TabZen repository is bootstrapped on CT130 for automated coding tasks:

- **Location:** `/root/repos/tabzen`
- **Owner:** `root` (runner user has full read/write access)
- **Initialized:** March 1, 2026
- **Clone Method:** Git SSH (GitHub)

### Branch Strategy

- **Primary Branch:** `main` - All production-ready code merges here
- **Feature Branches:** `feature/*` - For new feature development
- **Bugfix Branches:** `bugfix/*` - For bug fixes
- **Hotfix Branches:** `hotfix/*` - For urgent production fixes

All feature/bugfix work should be done on branches and merged via pull requests to `main`.

---

## Fallback Behavior

### Fallback Location

If `/root/repos/tabzen` becomes unavailable or inaccessible, the runner will fall back to:
- **Fallback Path:** `/root/repos`
- **Fallback Trigger:** Repository verification failure (permissions, missing directory, git errors)

### Fallback Limitations

When operating in fallback mode (`/root/repos`):
- Code should be moved to canonical path as soon as possible
- Git operations may reference incorrect repository context
- Branch switching operations may fail
- Repository-specific hooks and configurations may not apply

### Recovery from Fallback

To recover from fallback mode:

1. **Verify canonical path exists:**
   ```bash
   ls -la /root/repos/tabzen
   ```

2. **Verify git repository status:**
   ```bash
   cd /root/repos/tabzen && git status
   ```

3. **Verify remote configuration:**
   ```bash
   cd /root/repos/tabzen && git remote -v
   ```

4. **If repository is corrupted, reclone:**
   ```bash
   cd /root/repos
   rm -rf tabzen
   git clone git@github.com:joshuaswarren/tabzen.git tabzen
   ```

---

## Troubleshooting

### Common Issues

**Issue: Permission Denied**
- **Symptom:** Cannot write to `/root/repos/tabzen`
- **Remediation:** Check directory ownership with `ls -la /root/repos/tabzen`
- **Owner:** Platform Operations

**Issue: Remote Not Configured**
- **Symptom:** `git remote -v` returns empty
- **Remediation:** `git remote add origin git@github.com:joshuaswarren/tabzen.git`
- **Owner:** Repository Maintainer

**Issue: Network/SSH Authentication**
- **Symptom:** Cannot push/fetch from origin
- **Remediation:** Verify SSH keys are configured for GitHub access
- **Owner:** Platform Operations

**Issue: Wrong Branch Checked Out**
- **Symptom:** Not on `main` branch when expected
- **Remediation:** `git checkout main` followed by `git pull origin main`
- **Owner:** Developer/Runner

---

## Maintenance Notes

- **Last Verified:** March 1, 2026
- **Verification Command:** `cd /root/repos/tabzen && git status && git remote -v`
- **Health Check:** Run verification command before any major deployment

---

## Contact

For issues with this repository bootstrap or fallback behavior:
- **Repository Owner:** Joshua Warren
- **Platform Contact:** Platform Operations Team
