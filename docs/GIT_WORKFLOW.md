# Git workflow

The user requested that project changes be committed to GitHub and synchronized back into the working copy. This agreement applies during active project sessions. No background synchronization is configured.

## Initial remote setup

The connected account is `sanath265`. The repository is https://github.com/sanath265/sar-drafting-assistant and the default branch is `main`. The user made the repository public and granted connector write access.

GitHub connector commits are available. Use authenticated Git transport when available for push/fetch/pull. If transport is unavailable, use the connector for remote changes and explicitly report the local synchronization limitation.

The original local planning commit is preserved in the starter package's Git bundle. GitHub was initialized separately through the connector; preserve the original local branch when aligning the working copy with remote history.

## Each work session

1. Read `AGENTS.md`, the plan, decisions log, and `git status`.
2. Fetch the configured remote and inspect incoming commits.
3. Fast-forward only when the working branch is clean and the update is safe.
4. Preserve user changes. Resolve divergence deliberately; never use automatic hard resets or force pushes.
5. Work on a focused feature/documentation branch and run relevant checks.
6. Commit the completed change with a clear message.
7. Push the branch and provide the commit or pull-request link.
8. After an authorized merge, fast-forward the local main branch and verify the resulting SHA.

When Git transport is unavailable but connector writes work, report exactly which files and remote commits were created. Reconcile local history later; do not describe file materialization as a successful Git pull.
