# Branch Naming Standard

All work must be done in branches. Do NOT code directly on main.

## Branch Types

### 1) dev (shared staging)
- main integration branch before main

### 2) feature branches (new systems / subsystems)
Format:
`feature/<short_feature_name>`

Example:
`feature/sentry_roles`
`feature/game_loop_engine`
`feature/fact_pool`
`feature/complexity_metrics`

### 3) fix branches (bug fixes)
Format:
`fix/<what_is_broken>`

Example:
`fix/input_validation_crash`

---

## Workflow Summary

1. main → stable final build only
2. dev → active team integration
3. all members create feature branches off dev
4. PRs must merge into dev (not main)
5. only dev → main merges happen once stable + playtested
