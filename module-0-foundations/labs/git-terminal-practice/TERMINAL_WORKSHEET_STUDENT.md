# Lab — Git & Terminal Guided Practice

## Set Up a Fresh Practice Folder

*Complete the TODOs below as you work through this step.*

```bash
mkdir git-practice
cd git-practice
pwd
```

## Initialize and Add a README

*Complete the TODOs below as you work through this step.*

```bash
git init
echo "# Git Practice" > README.md
git add README.md
git status
```

## Make Three Real, Separate Commits

*Complete the TODOs below as you work through this step.*

```bash
git commit -m "Add initial README"
# continue: make 2 more separate, well-messaged commits
```

## Create a GitHub Remote and Push

*⚠️ Not auto-validated: <your-repo-url> is a placeholder every Fellow swaps for their own real GitHub URL - not runnable as literally written, so not automatable.*

*Context: <your-repo-url> is a placeholder — each Fellow creates their own empty GitHub repo first, then swaps in the real URL.*

*Complete the TODOs below as you work through this step.*

```bash
git remote add origin <your-repo-url>
git push -u origin main
git log --oneline
```
