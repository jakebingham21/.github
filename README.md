# .github

Special GitHub repo for @jakebingham21.

- `profile/README.md` - operator dashboard shown on the GitHub profile page
- `.github/workflows/stale_repos.yml` - monthly cron that flags inactive repos (>365 days) as GitHub issues, honoring `keep` and `template` topic exemptions

## Setup (one-time)

1. Generate a PAT with `repo` scope at:
   https://github.com/settings/tokens/new?scopes=repo&description=STALE_REPOS_TOKEN
2. Add it as a repository secret named `STALE_REPOS_TOKEN` on this repo:
   https://github.com/jakebingham21/.github/settings/secrets/actions
3. Run the workflow manually (Actions tab, Stale Repos, Run workflow) to verify it posts an issue correctly.
