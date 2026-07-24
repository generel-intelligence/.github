# AGENTS.md

## Purpose

This repository owns organization-wide GitHub governance and shared policy
automation.

## Ownership

- `.github/ISSUE_TEMPLATE/` owns default issue forms.
- `.github/PULL_REQUEST_TEMPLATE.md` owns the default pull-request template.
- `.github/workflows/` owns reusable governance and secret-scanning workflows.
- `profile/` owns the public organization profile.

Repository-specific source, commands, CI, and release behavior belong to the
repository that implements them.

## Local Contracts

- Keep shared workflows read-only and safe for untrusted pull requests.
- Use `pull_request`, never `pull_request_target`.
- Pin every external action to a full commit SHA.
- Do not expose secrets or verify suspected credentials against providers.
- Do not add language, build, publishing, or release workflows before a real
  consumer establishes the contract.
- Canonical policies live here; other repositories link to them and add only
  local scope.

## Work Guidance

- Treat policy changes as security-sensitive.
- Keep templates short and applicable across repositories.
- Do not add issue forms for future milestones.

## Verification

- Inspect workflow permissions and triggers.
- Validate workflow and issue-form YAML.
- Run the governance checks through a pull request.
- Confirm the secret scan does not use repository secrets or credential
  verification.

## Child DOX Index

No child `AGENTS.md` files are required at this stage.
