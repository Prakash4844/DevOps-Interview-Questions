#### Here are Some Resources: 

1. [Simplilearn - Top 100+ Git Interview Questions and Answers](https://www.simplilearn.com/tutorials/git-tutorial/git-interview-questions)
2. [InterviewBit - Git Interview Questions](https://www.interviewbit.com/git-interview-questions/)
3. [intellipaat - Top Git Interview Questions And Answers](https://intellipaat.com/blog/interview-question/git-interview-questions-answers/)
4. [Edureka - Top Git Interview Questions](https://www.edureka.co/blog/interview-questions/git-interview-questions/)
5. [JavaTpoint - GIT Interview Questions](https://www.javatpoint.com/git-interview-questions)
6. [Mindmajix - Git Interview Questions](https://mindmajix.com/git-interview-questions-answers)
7. [Guru99 - Top 45 Git Interview Questions and Answers](https://career.guru99.com/top-40-interview-questions-on-git/)
8. [Shiksha - Top 50 Git Interview Questions and Answers](https://www.shiksha.com/online-courses/articles/top-git-interview-questions-and-answers/)
9. [Toptal - 13 Essential Git Interview Questions](https://www.toptal.com/git/interview-questions)

**NOTE** - Above resources are not mine and belong to their owners, questions may overlap.

## Table of Contents

1. [General Questions](#questions)
2. [Scenario-based Questions](#some-scenario-based-devops-question)

# Questions

## Essentials

1. **What is Git, and why is it important in software development?**

   - **Git** is a distributed version control system (DVCS) used to track changes in source code and collaborate on software development. It's important because it enables version control, collaboration, branching, and code history tracking, enhancing development efficiency and code quality.

2. **Explain the difference between Git and GitHub.**

   - **Git** is the version control system itself, while **GitHub** is a web-based platform for hosting and collaborating on Git repositories. GitHub provides features like issue tracking, pull requests, and project management in addition to Git's version control capabilities.

3. **What is a Git repository, and what does it contain?**

   - A **Git repository** is a directory where Git stores all the files, history, and configuration related to a project. It contains:
     - **Working Directory**: The current version of project files.
     - **Index (Staging Area)**: A snapshot of changes to be committed.
     - **Commit History**: A record of all commits and changes made to the project.

4. **How do you create a new Git repository?**

   - To create a new Git repository, navigate to the project's root directory and run `git init`. This initializes an empty Git repository.

5. **What is a commit in Git, and how do you create one?**

   - A **commit** in Git represents a snapshot of changes to the project. To create a commit, use `git commit -m "Commit message"` after staging changes with `git add`. This permanently records changes in the commit history.

6. **Explain what a Git branch is, and why are branches used?**

   - A **Git branch** is a separate line of development that allows you to work on features, bug fixes, or experiments without affecting the main codebase. Branches help isolate changes, collaborate simultaneously, and merge features systematically.

7. **How do you create and switch between Git branches?**

   - To create a new branch, use `git branch branch_name`. To switch to a branch, use `git checkout branch_name` or `git switch branch_name`. A shorter way to create and switch to a new branch is `git checkout -b branch_name`.

8. **What is a merge conflict in Git, and how do you resolve it?**

   - A **merge conflict** occurs when Git is unable to automatically merge changes from different branches due to conflicting edits to the same lines of code. To resolve a merge conflict, you must manually edit the conflicting files, choose the desired changes, and then commit the resolved files.

9. **Explain the purpose of the `git clone` command.**

   - The `git clone` command is used to create a copy of a remote Git repository on your local machine. It not only downloads the repository but also sets up a link to the remote repository, allowing you to fetch updates and contribute to the project.

10. **What is a remote in Git, and how is it related to repositories?**

    - A **remote** in Git refers to a copy of a repository hosted on a different location, such as on GitHub or a server. Remotes allow users to collaborate by fetching and pushing changes to and from the central repository.

11. **How do you push changes from a local Git repository to a remote repository?**

    - To push changes to a remote repository, use `git push remote_name branch_name`. For example, `git push origin master` pushes changes from the local `master` branch to the remote repository named `origin`.

12. **What is a Git pull request, and how does it facilitate code review and collaboration?**

    - A **pull request (PR)** is a request to merge changes from one branch into another, typically from a feature branch to the main branch. It facilitates code review by allowing team members to discuss and review code changes before merging them into the main codebase.

13. **Explain the purpose of Git tags and how they differ from branches.**

    - **Git tags** are references to specific commits in the Git history, typically used to mark release points or significant milestones. Unlike branches, tags are not meant for ongoing development but for marking specific points in the commit history.

14. **What is Gitignore, and why is it useful in a Git repository?**

    - A **.gitignore** file specifies patterns of files or directories that should be ignored by Git. It's useful for excluding build artifacts, temporary files, and sensitive data from being committed to the repository.

15. **How do you revert a commit in Git without losing history?**

    - To revert a commit without losing history, use `git revert commit_hash`. This creates a new commit that undoes the changes introduced by the specified commit, preserving a record of the reversal.

16. **Explain the purpose of the `git rebase` command and how it differs from `git merge`.**

    - `git rebase` is used to rewrite the commit history by moving, combining, or editing commits. It replays your local commits on top of the updated branch, creating a linear history. In contrast, `git merge` integrates changes from one branch into another without modifying commit history, resulting in a merge commit.

17. **What is Git bisect, and how can it help locate a bug in the commit history?**

    - **Git bisect** is a binary search tool in Git used to find the specific commit that introduced a bug. By marking known good and bad commits, Git bisect helps narrow down the faulty commit through an efficient process of elimination.

18. **Explain the purpose of Git hooks and provide examples of when they can be used.**

    - **Git hooks** are scripts that run automatically at specific points in Git workflows. Examples include:
      - **pre-commit**: Running linting or code formatting checks before committing.
      - **post-receive**: Triggering deployment scripts after receiving changes on a remote server.
      - **prepare-commit-msg**: Automatically adding issue numbers or tags to commit messages.

19. **What is Git cherry-pick, and how is it used?**

    - `git cherry-pick` allows you to select a specific commit from one branch and apply it to another branch. This is useful when you want to pick and apply individual commits without merging entire branches.

20. **How can you undo the last Git commit if you haven't pushed it to a remote repository yet?**

    - To undo the last Git commit (locally), use `git reset HEAD~1` to move the branch pointer back one commit. This leaves your changes in the working directory but not staged. If you want to discard the changes completely, use `git reset --hard HEAD~1`. Note that this should be used with caution as it discards changes permanently.

---
---


## Some scenario-based DevOps question.

**1. Scenario:** You've made several commits on a feature branch but realize that one of the earlier commits introduced a critical bug. How would you fix this?

**Answer:** I would use the `git bisect` command to find the commit that introduced the bug. Here's what I would do:

1. Start the bisecting process: `git bisect start`.
2. Mark the current commit as bad: `git bisect bad`.
3. Mark an earlier commit as good, where you know the bug didn't exist: `git bisect good <earlier-commit>`.
4. Git will automatically check out a commit in between, and I'll test it.
5. Repeat steps 3 and 4 until Git identifies the specific commit that introduced the bug.
6. Once the bad commit is identified, I'll fix the issue and make a new commit.
7. Finally, I'll run `git bisect reset` to exit the bisecting mode.

**2. Scenario:** You've been working on a local branch and want to update it with changes from the remote branch. How do you do this?

**Answer:** To update my local branch with changes from the remote branch, I would follow these steps:

1. First, ensure I'm on my local branch: `git checkout my-branch`.
2. Fetch the latest changes from the remote repository: `git fetch origin`.
3. Merge the remote branch into my local branch: `git merge origin/my-branch`.

Alternatively, I can use `git pull` to combine the fetch and merge operations into one step:

1. `git checkout my-branch`
2. `git pull origin my-branch`

**3. Scenario:** You accidentally committed sensitive information (e.g., passwords) to a Git repository. How would you remove it from the commit history?

**Answer:** To remove sensitive information from the commit history, I would use the following steps:

1. First, ensure I've saved a backup of the sensitive data.
2. Use the `git filter-branch` command to rewrite the commit history, excluding the sensitive file or folder:

```bash
git filter-branch --tree-filter 'rm -f path/to/sensitive/file' HEAD
```

3. After the filtering process, force-push the updated branch to the remote repository:

```bash
git push origin <branch-name> --force
```

This will overwrite the remote branch with the updated commit history, effectively removing the sensitive information.

**4. Scenario:** You're working on a feature branch, and a critical production bug needs to be fixed immediately. How do you incorporate the bug fix into your feature branch without losing your work?

**Answer:** To incorporate the bug fix into my feature branch without losing my work, I would follow these steps:

1. Commit my current changes on the feature branch: `git commit -m "Feature changes"`
2. Check out the main branch or the branch with the bug fix: `git checkout main`
3. Create a new branch from the main branch for the bug fix: `git checkout -b bugfix-branch`
4. Make the necessary bug fixes and commit them: `git commit -m "Bug fix"`
5. Switch back to the feature branch: `git checkout feature-branch`
6. Merge the bugfix-branch into the feature branch: `git merge bugfix-branch`
7. Resolve any merge conflicts if they occur.
8. Continue working on the feature, incorporating the bug fix.

This way, the bug fix is included in the feature branch, and you can continue working on your feature without losing any progress.

**5. Scenario:** You've just cloned a Git repository and want to start working on a new feature. What are the steps you would follow to create and work on a new feature branch?

**Answer:** To create and work on a new feature branch, I would do the following:

1. Clone the Git repository: `git clone <repository-url>`.
2. Navigate to the repository: `cd <repository-name>`.
3. Create a new feature branch and switch to it: `git checkout -b feature/new-feature-name`.
4. Make my changes on this branch.
5. Commit my changes: `git commit -m "Implemented new feature"`.
6. Push the feature branch to the remote repository: `git push origin feature/new-feature-name`.

**6. Scenario:** You're working on a team project with multiple developers. How do you handle merge conflicts when trying to merge your feature branch into the main branch?

**Answer:** To handle merge conflicts during the process of merging a feature branch into the main branch, I would follow these steps:

1. Fetch the latest changes from the main branch: `git fetch origin main`.
2. Ensure I'm on the feature branch: `git checkout feature-branch`.
3. Merge the main branch into the feature branch: `git merge main`.
4. If there are merge conflicts, Git will indicate the conflicting files.
5. Open the conflicting files in a text editor and resolve the conflicts manually by choosing the desired changes.
6. After resolving the conflicts, add the resolved files: `git add <conflicted-file>`.
7. Continue the merge process: `git commit -m "Merge branch 'main' into feature-branch"`.
8. Finally, push the updated feature branch with resolved conflicts to the remote repository: `git push origin feature-branch`.

**7. Scenario:** You accidentally deleted a file in your working directory, but you haven't committed the deletion yet. How can you recover the deleted file?

**Answer:** To recover a deleted file that hasn't been committed yet, I would use the following Git command:

```bash
git checkout -- path/to/deleted/file
```

This command retrieves the deleted file from the latest commit and restores it to your working directory.

**8. Scenario:** You want to share a specific commit with a colleague without pushing it to the remote repository. How can you do this?

**Answer:** To share a specific commit with a colleague without pushing it to the remote repository, you can create a patch file and send it to them. Here's how:

1. Identify the commit hash you want to share.
2. Create a patch file for that commit: `git format-patch -1 <commit-hash>`.
3. Share the generated `.patch` file with your colleague using a file-sharing method of your choice.
4. Your colleague can apply the patch using the `git apply` command: `git apply <patch-file>`.

This allows your colleague to apply the changes from the commit locally without it being pushed to the remote repository.
