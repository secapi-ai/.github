## Summary

<!-- What changed and why. One paragraph max. Link issues with "Closes #". -->

Closes #

## Scope

<!-- Check ALL areas this PR touches. Reviewers and CI use this to gauge blast radius.
     This is the org-default template. Repos with their own `.github/pull_request_template.md`
     override this; if you're seeing this in a PR for a specific repo, please replace it with
     that repo's own checklist. -->

- [ ] Source / library code
- [ ] Tests
- [ ] Examples
- [ ] Dependencies / packaging metadata
- [ ] Documentation (README, docs site, examples)
- [ ] `.github/` — CI/CD workflows, templates, automation
- [ ] Release / publish config

## Changes

<!-- Bullet points grouped by area. Be specific — diffs are for code, this is for intent. -->

-
-

## Verification

<!-- What you ran locally. Paste actual commands and their outcomes.
     Choose the appropriate stack for the repo: -->

```bash
# Go
go build ./... && go test ./... && go vet ./...

# JS/TS
bun install && bun run typecheck && bun run test && bun run build

# Python
uv sync && uv run pytest && uv run ruff check . && uv run mypy

# Rust
cargo check && cargo test && cargo clippy --all-targets -- -D warnings

# Homebrew
brew audit --strict --online Formula/<name>.rb && brew test <name>
```

## Deployment Impact

<!-- Skip this section entirely for code-only changes with no release impact. -->

- [ ] New version bump required
- [ ] Breaking API/CLI change (semver major)
- [ ] Publish required (npm / PyPI / crates.io / Homebrew tap)
- [ ] Docs updated to match
- [ ] Companion docs PR in org docs site
- [ ] Secrets / env vars added or changed

## Completion Attestation

<!-- You MUST select one. This is a binding statement of delivery status. -->

- [ ] **100% complete, 100% functional.** All code is written, tested, builds cleanly, and works end-to-end against live SEC API. No outstanding work remains.
- [ ] **Not fully complete or functional.** Deltas listed below.

### Deltas (only if attesting incomplete)

<!-- Short bullets. Items intentionally deferred from this PR's stated scope. -->

-

## Screenshots / Demo

<!-- Terminal output, CLI snippets, or API response examples. Delete section if not applicable. -->

---

<details>
<summary>Agent Context</summary>

<!-- This section is for AI coding agents that may continue or review this work.
     Fill in what's relevant; delete what isn't. -->

**Key files to read first:**
<!-- List the 3-5 most important files for understanding this PR's changes. -->
-

**Decisions made:**
<!-- Non-obvious choices and why. Agents should not re-litigate these. -->
-

**Relevant docs:**
- https://docs.secapi.ai
- https://secapi.ai/developers

**Conventions applied:**
<!-- Language idioms, error handling, response metadata preservation. -->
-

</details>
