# INTRODUCTION TO GIT

**[about]:**
<small>_This is a super simplified Git tutorial — like Git for humans, not robots._</small>
<small>_We decode the wizardry of `add`, `commit`, `push`, and other arcane spells._</small>
<small>_Think of branches as alternate universes for your code — no paradoxes, promise._</small>
<small>_You'll learn to clone stuff (legally), stash your mess, and time-travel with commits._</small>
<small>_Merge conflicts? Like sibling fights — awkward, but fixable._</small>
<small>_Basically, it’s Git without the existential crisis. You got this._</small>

---

## Git

Git is a powerful, distributed version control system (VCS) used to track changes in source code during software development. It helps developers manage code, collaborate with teams, and maintain the history of their projects. Let's break down Git into manageable parts to give you a solid understanding.

<small>_Simplified: ..._</small>

---

### 1. **What is Git?**

Git allows multiple developers to work on the same codebase simultaneously without interfering with each other's work. It tracks changes to files and allows you to revert to previous versions if needed. Git is also highly efficient, fast, and can handle large codebases.

### 2. **Version Control Systems (VCS)**

- **Centralized Version Control (CVS)**: One central repository where the code lives. Everyone works on this central copy.
- **Distributed Version Control (Git)**: Every developer has their own local copy (repository) that tracks all changes. Changes are shared by pushing and pulling updates from other developers' repositories.

---

### 3. **Basic Git Concepts**

The following concepts would be explained below:

- Repository
- Working Directory, Staging Area, Repository
- Commit
- Branches
- Push

#### Repositories

- **Repository (Repo)**: A directory that contains all your project files and a `.git` folder which keeps track of your version history.

  - **Local Repository**: The Git repo on your local machine.
  - **Remote Repository**: The Git repo stored online (e.g., GitHub, GitLab, Bitbucket).

#### Staging Area (Index)

- Before committing changes to the repository, you need to stage them. The staging area is where you prepare changes to be committed.

#### Commit

A commit is a snapshot of the project at a specific point in time. It contains:

- The changes made.
- A commit message describing the changes.
- A unique ID (SHA hash).

#### Branches

- A branch is a parallel version of your project. By default, you start with a `main` (or `master`) branch.
- You can create new branches to work on features or fixes, keeping your main branch stable.

#### Remote Repositories

- These are hosted on platforms like GitHub, GitLab, or Bitbucket. You can clone, push, and pull from remote repositories to sync with others.

---

### 4. **Basic Git Commands**

#### 1. **Setup Git**

Before using Git, you need to set your name and email, which Git uses to tag your commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

#### 2. **Initializing a Git Repository**

To create a new Git repository in an existing directory:

```bash
git init
```

This initializes a new Git repository in the directory, creating a `.git` folder.

#### 3. **Cloning a Remote Repository**

To clone an existing remote repository to your local machine:

```bash
git clone https://github.com/username/repository.git
```

#### 4. **Staging Changes**

To add files to the staging area:

```bash
git add filename
```

To stage all changes:

```bash
git add .
```

#### 5. **Committing Changes**

After staging, you commit your changes with a message describing what was done.

```bash
git commit -m "Commit message"
```

#### 6. **Checking Status**

You can check the status of your repository, showing untracked, staged, and unstaged changes:

```bash
git status
```

#### 7. **Viewing Commit History**

To view the commit history:

```bash
git log
```

#### 8. **Pushing Changes to Remote**

To send your local changes to the remote repository:

```bash
git push origin main
```

#### 9. **Pulling Changes from Remote**

To fetch and merge changes from the remote repository:

```bash
git pull origin main
```

#### 10. **Creating and Switching Branches**

To create a new branch:

```bash
git branch new-branch-name
```

To switch to a branch:

```bash
git checkout new-branch-name
```

Or, use the shorthand to create and switch to a branch in one step:

```bash
git checkout -b new-branch-name
```

#### 11. **Merging Branches**

To merge changes from one branch into another:

1. Switch to the target branch (e.g., `main`).

   ```bash
   git checkout main
   ```

2. Merge the branch (e.g., `feature-branch`) into the current branch.

   ```bash
   git merge feature-branch
   ```

#### 12. **Handling Merge Conflicts**

Sometimes, Git can’t merge files automatically. It will flag conflicts and require you to manually fix them in the files. After resolving, stage and commit the changes.

```bash
git add conflicted-file
git commit -m "Resolved merge conflict"
```

#### 13. **Deleting Branches**

Once a branch is merged and no longer needed, you can delete it:

- Locally:

  ```bash
  git branch -d branch-name
  ```

- Remotely:

  ```bash
  git push origin --delete branch-name
  ```

---

### 5. **Working with Remote Repositories**

Git allows you to interact with remote repositories.

#### 1. **Adding a Remote Repository**

To connect your local repository to a remote:

```bash
git remote add origin https://github.com/username/repository.git
```

#### 2. **Fetching Updates from Remote**

This command fetches updates from the remote but doesn’t merge them automatically.

```bash
git fetch origin
```

#### 3. **Pushing Changes to Remote**

Push your local changes to a remote branch:

```bash
git push origin branch-name
```

#### 4. **Pulling Changes from Remote**

To fetch and merge updates from the remote branch:

```bash
git pull origin branch-name
```

---

### 6. **Git Workflow**

Git has different workflows for how teams collaborate, and the most popular ones include:

- **Centralized Workflow**: A single branch is shared between all contributors.
- **Feature Branch Workflow**: Each feature or bug fix has its own branch.
- **Gitflow Workflow**: A structured branching model for larger projects.
- **Forking Workflow**: A common model used in open-source projects where contributors fork a repository and then make pull requests.

---

### 7. **Advanced Git Concepts**

#### 1. **Rebasing**

Rebasing allows you to rewrite commit history. It's often used to maintain a linear project history.

```bash
git rebase main
```

#### 2. **Cherry-picking**

Cherry-picking lets you apply a commit from one branch onto another without merging the entire branch.

```bash
git cherry-pick commit-id
```

#### 3. **Stashing Changes**

If you’re in the middle of work but need to switch branches, you can stash your changes to apply later.

```bash
git stash
```

To apply stashed changes:

```bash
git stash apply
```

#### 4. **Tags**

Tags are used to mark specific points in history as important, often for releases.

```bash
git tag v1.0
```

To push tags to a remote repository:

```bash
git push origin v1.0
```

---

### 8. **Git Best Practices**

- **Write meaningful commit messages**: Explain why the change was made.
- **Commit often, push early**: Regular commits make it easier to track progress and fix issues.
- **Pull before you push**: Always pull the latest changes from the remote before pushing your own.
- **Use branches for features, bugs, and experiments**: Keep `main` clean.

---

### 9. **Git GUI vs. Command Line**

- **Git Command Line**: More flexible and faster once you know the commands.
- **Git GUI Tools**: Tools like GitKraken, SourceTree, and GitHub Desktop provide graphical interfaces for managing repositories.
