# Playbook: Task Intake & Routing

## Purpose
Route each issue to the correct execution playbook with zero ambiguity.

## Routing rules
- `area:frontend` -> `10-frontend-delivery.md`
- `area:backend` -> `20-backend-api.md`
- `area:db` -> `30-database-migrations.md`
- `area:infra` -> `40-ci-cd.md`
- `area:sre` -> `50-sre-ops.md`
- `area:security` -> `60-security-compliance.md`
- `area:release` -> `70-release-management.md`

## Required preflight
1. Confirm repo root
2. Confirm working branch
3. Read selected playbook before edits
4. Write a short constraints-understood checklist

## Required proof outputs
- selected playbook
- changed files
- validation commands + results
- commit SHA
- PR URL
- issue comment URL
