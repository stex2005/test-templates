# test-templates

Sandbox for the Automation Team PR + Test Plan + Test Report templates.

## What's here

- `.github/PULL_REQUEST_TEMPLATE.md` — auto-fills the PR body on every new PR.
- `.github/TEST_REPORT_TEMPLATE.md` — empty Test Report scaffold to copy as a PR comment after running the matrix.
- `.github/workflows/post-test-plan-template.yaml` — `workflow_dispatch` action that posts the empty Test Plan template as a comment on a given PR.

## How to test

1. Edit any file on a feature branch, push, open a PR against `main` → confirm the PR body auto-populates with the PR template.
2. Run the workflow:
   - UI: Actions → "Post Test Plan template" → Run workflow → enter PR number.
   - CLI: `gh workflow run post-test-plan-template.yaml -f pr_number=<N> --repo stex2005/test-templates`
   - Confirm a comment appears on the PR.
3. Copy `TEST_REPORT_TEMPLATE.md` into a new PR comment to scaffold the report.
# sandbox change
Trivial edit to open a smoke-test PR.
