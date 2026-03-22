# Governance CI Validation Plan (Issue #9)

This document defines the fail/pass validation scenarios for governance checks.

## Checks under validation
- `.github/workflows/pr-issue-link.yml`
- `.github/workflows/ci-guardrails.yml`

## Scenario matrix

### 1) Missing issue link in PR body
- Expected: `require-issue-link` fails
- Fix: add `Closes #<issue>`
- Expected after fix: pass

### 2) Missing required PR evidence sections
- Expected: `require-issue-link` fails with missing sections
- Fix: add sections:
  - Summary
  - Why
  - Tests
  - Risk & Rollback
  - Security & Data
- Expected after fix: pass

### 3) Out-of-scope files for issue `area:*`
- Expected: `area-label-scope-check` fails and lists disallowed files
- Fix: remove/split out-of-scope changes or update issue area label appropriately
- Expected after fix: pass

### 4) Missing proof-bundle issue comment
- Expected: `proof-artifact-comment-check` fails
- Fix: post issue comment containing:
  - PR URL
  - full 40-char commit SHA
  - Validation summary (`Validation: ...`)
- Expected after fix: pass

## Evidence format
For each scenario, capture:
- failing run URL
- passing run URL
- short note with root cause and fix
