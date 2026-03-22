# Proof Bundle Standard

Every issue-linked PR should publish a proof comment on the issue containing:

1. PR URL
2. Full 40-char commit SHA
3. Validation summary (tests/build/lint/typecheck as relevant)

## Example

- PR: https://github.com/org/repo/pull/123
- Commit SHA: aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
- Validation: `npm run lint`, `npm test`, `npm run build`
