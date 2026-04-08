Git Workflow — Team Reference
Quick reference guide for push, pull, PR, and team best practices.

Push Procedure
1. git status  — check what has changed
2. git fetch origin && git rebase origin/main  — sync before push
3. git add <files> && git commit -m "type(scope): message"
4. git push origin feature/your-branch

Pull / Fetch
git fetch origin  — download changes, nothing merged yet
git pull --rebase origin main  — fetch + rebase (cleaner history)
git stash / git stash pop  — temporarily shelve local changes
On conflict: edit files, git add, git rebase --continue

Creating a PR / MR
Rebase branch on main before opening: git rebase origin/main
PR description: what changes, why, how to test, screenshots
Review comments: use nit: / blocker: / question: prefixes
Merge strategy: prefer Squash merge for clean main history

Team Best Practices
Branch naming: feature/ fix/ chore/ docs/ refactor/
Commits: Conventional Commits format — feat(scope): description
Keep PRs small — max ~400 changed lines
Never push directly to main — always via branch + PR
Review within 24h — waiting for review is the #1 bottleneck
CI must pass before merge — no merging red pipelines
Daily rebase of feature branches to minimize conflicts
