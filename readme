# Advanced Git Techniques: Git Rebase & Interactive Rebase

## Overview

This repository demonstrates advanced Git techniques, focusing on:

- **Git Rebase**: Rewriting commit history to create a cleaner, linear project history.
- **Interactive Rebase**: Fine-tuning commits (edit, squash, reword, etc.) for even more control.

Understanding and mastering these techniques can significantly improve project collaboration and repository cleanliness.

---

## Prerequisites

- Basic knowledge of Git (committing, branching, pushing, pulling).
- Git installed locally ([Download Git](https://git-scm.com/)).

---

## Git Rebase

### What is Git Rebase?

Git Rebase is a command that moves or combines a sequence of commits to a new base commit. It is used to:

- Integrate changes from one branch into another.
- Clean up commit history.
- Avoid unnecessary merge commits.

### Basic Usage

```bash
git checkout feature-branch
git rebase main
```

This command re-applies the commits from `feature-branch` onto the latest `main` branch.

### Common Options

- `--continue`: Continue the rebase after resolving conflicts.
- `--abort`: Cancel the rebase and return to the original branch.
- `--skip`: Skip the current patch during a rebase.

### Example Workflow

```bash
git checkout feature-branch
git fetch origin
# Rebase onto the latest main branch
git rebase origin/main

# If conflicts arise:
# Resolve them manually, then:
git add .
git rebase --continue
```

---

## Interactive Rebase

### What is Interactive Rebase?

Interactive Rebase (`git rebase -i`) allows you to edit commits individually. You can:

- Squash multiple commits into one.
- Reorder commits.
- Edit commit messages.
- Drop unnecessary commits.

### Starting an Interactive Rebase

```bash
git rebase -i HEAD~n
```

Where `n` is the number of previous commits you want to edit.

### Commands You Can Use

- `pick`: Use the commit.
- `reword`: Edit the commit message.
- `edit`: Amend the commit (change content).
- `squash`: Combine this commit with the previous one.
- `fixup`: Like squash but discard this commit's message.
- `drop`: Remove the commit.

### Example

```bash
git rebase -i HEAD~3
```

You might see:

```bash
pick a1b2c3 First commit
pick d4e5f6 Second commit
pick g7h8i9 Third commit
```

Modify it to:

```bash
pick a1b2c3 First commit
squash d4e5f6 Second commit
reword g7h8i9 Better message for third commit
```

Then Git will guide you through editing the final commit messages.

---

## Best Practices

- Use rebase for **local branches** that haven't been shared with others yet.
- Avoid rebasing **public branches** to prevent rewriting history others depend on.
- Always **create a backup branch** before performing complex rebases.

```bash
git checkout -b backup-branch
```

---

## Useful Resources

- [Git Documentation - Rebase](https://git-scm.com/docs/git-rebase)
- [Atlassian Git Tutorials - Rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
- [Pro Git Book - Rewriting History](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)

---

## License

This project is licensed under the MIT License.

---

## Contact

For questions or discussions, feel free to open an issue or a discussion thread!

