# GitHub setup and submission guide

These commands are a guide. They do not create a repository, commits, pull request, merge, or release until you run them and verify the results in your GitHub account.

## 1. Create a public repository
Create a repository named `cleantrack-community-web-app` on GitHub. Set visibility to **Public**. Do not initialize it with a README if you already have the local project files.

## 2. Initialize and push the project
Run these commands from the project folder:

```bash
git init
git branch -M main
git add index.html README.md PROMPT_LOG.md PROJECT_BRIEF.md GIT_GUIDE.md TESTING.md VIDEO_DEMO_SCRIPT.md
git commit -m "chore: add CleanTrack project structure"
git remote add origin https://github.com/YOUR-USERNAME/cleantrack-community-web-app.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

## 3. Make at least six small meaningful commits
Use separate commits for real changes. Example sequence:

```bash
git add index.html
git commit -m "feat: add missed collection report form"

git add index.html
git commit -m "feat: validate report fields"

git add index.html
git commit -m "feat: save reports in localStorage"

git add index.html
git commit -m "feat: display and delete saved reports"

git add index.html
git commit -m "style: make report page responsive"

git add README.md PROJECT_BRIEF.md
git commit -m "docs: add project brief and FR-01"

git add PROMPT_LOG.md TESTING.md VIDEO_DEMO_SCRIPT.md GIT_GUIDE.md
git commit -m "docs: add prompt log and submission guides"

git push
```

For the requirement, make sure the repository history shows at least six small commits. Do not create empty or misleading commits. If you already committed all files at once, make genuine improvements in separate commits instead of pretending the example commits happened.

## 4. Create and merge one pull request
Create a feature branch and make a genuine change:

```bash
git checkout -b docs/add-project-usage
```

Edit `README.md`, for example by adding verified screenshots or clarifying the setup steps. Then:

```bash
git add README.md
git commit -m "docs: improve project usage instructions"
git push -u origin docs/add-project-usage
```

On GitHub:
1. Open the repository.
2. Select **Compare & pull request**.
3. Set the base branch to `main`.
4. Review the changed files and create the pull request.
5. Merge the pull request.
6. Confirm its status says **Merged**.

Do not merge without reviewing the changes.

## 5. Create release v0.1.0
After the accepted project version is on `main`:

```bash
git checkout main
git pull
git tag -a v0.1.0 -m "CleanTrack first lab release"
git push origin v0.1.0
```

On GitHub, open **Releases**, choose the `v0.1.0` tag, add release notes, and publish. Verify the release page shows `v0.1.0`.

## 6. Verify submission evidence
- Repository visibility is Public.
- Commit history shows at least six meaningful commits.
- Pull request page shows Merged.
- Release page shows v0.1.0.
- README and PROMPT_LOG are present.
- Video link opens and runs for 2–3 minutes.
