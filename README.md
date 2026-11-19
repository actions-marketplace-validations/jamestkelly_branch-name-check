# GitHub Actions Workflows

Reusable workflows for personal projects.

## Branch Name Check

Call this workflow from a job in `.github/workflows/`:

```yaml
name: Standard PR Checks
on: pull_request
permissions: {}
jobs:
  branch-name:
    uses: jamestkelly/github-actions-workflows/.github/workflows/branch-name-check.yml@v1
```

Use a full commit SHA instead of `v1` to pin the implementation. On pull requests the check validates the source branch, including branches from forks. On other events it validates the ref name.

`main`, `development`, and `staging` are allowed. Other branches need a nonempty name after one of: `feat/`, `feature/`, `fix/`, `bugfix/`, `chore/`, `hotfix/`, `release/`, `revert/`, `refactor/`, `docs/`, `test/`, `ci/`, or `dependabot/`.
