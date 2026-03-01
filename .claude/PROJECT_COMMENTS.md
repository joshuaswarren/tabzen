# TabZen Project Comments

## Repository Bootstrap (CT130)

**Date**: 2026-03-01
**Task**: CT130 runner repo bootstrap

### Bootstrap Summary
The TabZen repository has been bootstrapped at `/root/repos/tabzen` for Claude Runner coding tasks.

### Current State
- **Path**: `/root/repos/tabzen` (canonical)
- **Branch**: `main` (default)
- **Remote**: `git@github.com:joshuaswarren/tabzen.git`
- **GitHub**: https://github.com/joshuaswarren/tabzen
- **Status**: Fully operational

### Fallback Policy
1. **Primary**: Always use `/root/repos/tabzen` for TabZen development
2. **Fallback**: If path unavailable, check:
   - Path exists and is writable
   - Git initialized (`git status` works)
   - If missing, re-bootstrap with `git init` and configure `main` branch
3. **Previous fallback** to `/root/repos` is deprecated

### Known Blockers
No current blockers. Repository is fully operational.

### Resolved Issues
| Issue | Resolution | Date |
|-------|------------|------|
| GitHub remote not configured | Resolved by setting `GH_TOKEN` env var and using SSH for git operations | 2026-03-01 |

### Authentication Notes
- GitHub CLI requires `GH_TOKEN` environment variable to be set
- Token stored in `~/.config/gh/hosts.yml` but not auto-loaded
- Git operations use SSH (`git@github.com:`) which works via `~/.ssh/id_rsa`
