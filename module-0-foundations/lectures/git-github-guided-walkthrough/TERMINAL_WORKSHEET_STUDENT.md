# Git & GitHub, Guided Walkthrough

**Module 0: Foundations**

**Learning Objectives:**
- Initialize a local git repository from the terminal
- Make a well-messaged commit, step by step
- Create a matching GitHub remote and push your first commit

## Scenario

You just finished your first real line of analysis code, and you really don't want to lose it. Today you'll set up version control the way it's actually used on the job: turn a folder into a git repository, make a commit that explains itself, and push it to GitHub so the work exists somewhere safer than just your own laptop.

> **How to use this worksheet:** each shaded block below (the ones starting with three backtick marks and the word "bash") contains real commands - type them into your own terminal, one line at a time. The backtick fence marks themselves aren't something you type, they just tell this file "this is code." A `# TODO:` line means: replace it with the real command.

## Start Tracking a Project

*Context: git init creates a hidden .git folder — that's where all the history actually lives.*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
$ mkdir my-first-repo
$ cd my-first-repo
# TODO: turn this folder into a git repository
```

## Stage and Check Status

*Context: git status is the single most useful command in git — run it constantly, it never changes anything, it just tells you what's going on.*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
# TODO: stage README.md so git tracks it
$ git status
```

## Make Your First Commit

*Context: The -m flag lets you write the commit message inline. Make it describe WHAT changed, not "update" or "stuff."*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
# TODO: commit with a specific, descriptive message
$ git commit -m ""
```

## See Exactly What Changed

*Context: git diff only shows changes to files git is already tracking — README.md is tracked now that it's been committed once, so this edit shows a real +/- line diff.*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
$ echo "More notes coming soon." >> README.md
# TODO: see exactly what changed since the last commit
```

## Link and Push

*⚠️ Not auto-validated: <your-repo-url> is a placeholder you swap for your own real GitHub URL - not runnable as literally written, so not automatable.*

*Context: <your-repo-url> is a placeholder — swap in the real URL GitHub just gave you, it's different for everyone.*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
# TODO: connect your local repo to the GitHub remote you just created
$ git remote add origin <your-repo-url>
# TODO: push your first commit up to that remote
$ git push -u origin main
```

## See Your Own History

*Context: --oneline shows one line per commit instead of the full detailed view — easier to scan.*

**AI Mode:** Try Without AI, Then Tutor If Stuck

*Complete the TODOs below as you work through this step.*

```bash
# TODO: view your commit history, one line per commit
```
