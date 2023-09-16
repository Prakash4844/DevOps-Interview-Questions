
##### Here are Some Resources: 

[Prepinsta - GitHub Interview Questions and Answers](https://prepinsta.com/interview-preparation/technical-interview-questions/github-interview-questions-and-answers/)<br>
[MindMajix - GitHub Interview Questions](https://mindmajix.com/github-interview-questions)

**NOTE** - Above resources are not mine and belong to their owners, questions may overlap.

## Table of Contents

1. [General Questions](#questions)
2. [Scenario-based Questions](#some-scenario-based-devops-question)

# Questions

## Essentials

1. **What is GitHub, and how does it differ from Git?**

   - **GitHub** is a web-based platform that provides hosting for Git repositories, along with collaboration and project management features. It enhances Git by offering a central place for code hosting, issue tracking, pull requests, and team collaboration.

2. **What is the purpose of a GitHub repository, and how can it be used in software development?**

   - A **GitHub repository** serves as a central location to store, version control, and collaborate on code. It facilitates collaboration by allowing multiple users to clone, make changes, and contribute to a project. Repositories are used for code hosting, version history tracking, and collaboration.

3. **Explain the difference between a public and a private repository on GitHub.**

   - A **public repository** is accessible to anyone, and the code and project details are visible to the public.
   - A **private repository** is restricted to authorized users or collaborators. Code and project details are not visible to the public unless specifically shared.

4. **What is a README.md file in a GitHub repository, and why is it important?**

   - A **README.md** file is a markdown-formatted document that provides information about a project. It typically contains a project's description, installation instructions, usage guidelines, and other important information. It serves as the project's documentation and helps users and contributors understand the project.

5. **Explain what a Git branch is in the context of GitHub and how branching is used in collaborative development.**

   - A **Git branch** in GitHub represents an independent line of development within a repository. Branching allows collaborators to work on features, bug fixes, or experiments separately from the main codebase. It facilitates parallel development and easy integration through pull requests.

6. **How do you create a new branch in a GitHub repository?**

   - To create a new branch in a GitHub repository, follow these steps:
     1. Navigate to the repository on GitHub.
     2. Click on the "Branch" dropdown menu.
     3. Enter a branch name and click "Create branch."

7. **What is a pull request in GitHub, and how does it facilitate code review and collaboration?**

   - A **pull request (PR)** in GitHub is a request to merge changes from one branch into another, typically from a feature branch to the main branch. It facilitates code review and collaboration by allowing team members to review proposed changes, comment on them, and discuss modifications before merging.

8. **Explain the purpose of GitHub issues and how they are used in project management.**

   - **GitHub issues** are used to track tasks, bugs, enhancements, and discussions related to a project. They serve as a central place for project management, allowing team members to assign tasks, set priorities, and track progress. Issues can be linked to pull requests, making it easy to connect code changes with specific tasks.

9. **What is the difference between forking a repository and cloning a repository in GitHub?**

   - **Forking** a repository creates a copy of another user's repository on your GitHub account. It's used when you want to contribute to a project without direct write access to the original repository.
   - **Cloning** a repository downloads a copy of a GitHub repository to your local machine. It's used when you want to work on a project locally and have the ability to push changes back to the original repository if you have permission.

10. **How do you contribute to an open-source project hosted on GitHub?**

    - To contribute to an open-source project on GitHub, follow these general steps:
      1. Fork the project's repository to your GitHub account.
      2. Clone your forked repository to your local machine.
      3. Create a new branch for your changes.
      4. Make your desired changes and commit them.
      5. Push your changes to your GitHub repository.
      6. Create a pull request from your branch to the original project's repository.

11. **Explain what GitHub Actions are and how they can be used in a GitHub repository.**

    - **GitHub Actions** are workflows that automate various tasks in a GitHub repository. They can be used for tasks like continuous integration (CI), continuous delivery (CD), running tests, deploying applications, and more. GitHub Actions are defined using YAML files and can be triggered by events like pushes, pull requests, or scheduled intervals.

12. **What is the purpose of a GitHub organization, and how does it differ from a user account?**

    - A **GitHub organization** is a group of users or collaborators who can manage and work on repositories collectively. It provides centralized control over repositories, teams, and access permissions. Organizations are typically used for businesses, open-source projects, or community efforts. In contrast, a **user account** represents an individual GitHub user.

13. **Explain the concept of GitHub Gists and how they are used.**

    - **GitHub Gists** are a way to share and manage code snippets, notes, and small scripts. They are publicly accessible and can be used for quick code sharing, collaboration, or personal reference. Gists support multiple files and can be embedded in web pages.

14. **What are GitHub project boards, and how can they be used for project management?**

    - **GitHub project boards** are tools for managing and organizing work within a GitHub repository. They allow you to create task cards, track progress, set priorities, and categorize work items. Project boards can be customized to fit various project management workflows, including Agile methodologies.

15. **Explain the purpose of GitHub Pages and how they can be used for hosting websites.**

    - **GitHub Pages** is a feature that allows you to host static websites directly from your GitHub repository. It's commonly used for personal websites, documentation sites, and project landing pages. GitHub Pages automatically builds and deploys your site when you push changes to the `gh-pages` branch or other designated branches.

16. **What is the "Contributions" graph on a GitHub user's profile, and how is it generated?**

    - The "Contributions" graph on a GitHub user's profile shows a summary of their activity on GitHub over time. It includes contributions like commits, pull requests, issues, and more. The graph is generated based on the user's actions within repositories and organizations.

17. **Explain the role of GitHub Discussions in fostering community engagement and communication.**

    - **GitHub Discussions** is a feature that enables community members to have open and threaded discussions related to a project. It serves as a platform for broader conversations, questions, and announcements beyond code-related issues and pull requests. Discussions can help build a strong and collaborative community around a project.

18. **How can you protect a branch in a GitHub repository, and why might you want to do so?**

    - You can **protect a branch** in a GitHub repository by enabling branch protection rules. This restricts who can push to the branch and enforces specific checks, such as requiring status checks or reviews, before merging changes. Branch protection is often used to safeguard critical branches like the main branch from accidental or unauthorized changes.

---
---


## Some scenario-based DevOps question.

1. **Scenario**: You've just created a new repository on GitHub and want to add your existing project to it. What steps do you follow?

   **Answer**: 
   1. Go to GitHub and log in to your account.
   2. Click the "+" icon in the top right corner and select "New repository."
   3. Fill in the repository name, description, and other settings.
   4. Click "Create repository."
   5. Follow the instructions in the "…or push an existing repository from the command line" section on your repository's page. It typically involves running `git remote add origin <repository URL>` and `git push -u origin master` if you're using Git.

2. **Scenario**: You want to collaborate with others on a GitHub project. How can you fork a repository and create a pull request to contribute changes?

   **Answer**:
   1. Navigate to the repository you want to contribute to on GitHub.
   2. Click the "Fork" button in the top right corner. This creates a copy of the repository under your GitHub account.
   3. Clone your forked repository to your local machine using `git clone <forked repo URL>`.
   4. Create a new branch for your changes using `git checkout -b <branch-name>`.
   5. Make and commit your changes using `git commit -m "Your commit message"`.
   6. Push your changes to your forked repository using `git push origin <branch-name>`.
   7. Go to the original repository and click "New Pull Request." GitHub will compare your forked branch to the original repository's master branch.
   8. Add a title and description for your pull request, then click "Create Pull Request."

3. **Scenario**: You're working on a collaborative project, and your pull request has received feedback. How can you make changes and update the pull request?

   **Answer**:
   1. Go to your forked repository on GitHub.
   2. Switch to the branch associated with your pull request.
   3. Make the necessary changes to your code.
   4. Commit the changes using `git commit -m "Your updated commit message"`.
   5. Push the changes to your branch on GitHub with `git push origin <branch-name>`.
   6. Return to your pull request in the original repository.
   7. GitHub will automatically update the pull request with your new changes.

4. **Scenario**: You want to keep your forked repository in sync with the changes made in the original repository. How can you do this?

   **Answer**:
   1. Add the original repository as a remote using `git remote add upstream <original-repo-URL>`.
   2. Fetch the changes from the original repository with `git fetch upstream`.
   3. Check out your local master branch with `git checkout master`.
   4. Merge the changes from the original repository's master branch into your local master branch with `git merge upstream/master`.
   5. Push the updated master branch to your fork on GitHub with `git push origin master`.

5. **Scenario**: You accidentally pushed sensitive information, like API keys or passwords, to a public GitHub repository. What steps should you take to remove or protect this sensitive data?

   **Answer**:
   1. Immediately remove the sensitive data from your code.
   2. Create a `.gitignore` file if you haven't already to prevent further commits of sensitive files.
   3. Use the `git filter-branch` or `git filter-repo` command to remove the sensitive data from the repository's history.
   4. Force push the updated repository to GitHub using `git push --force`.
   5. Consider rotating any compromised secrets (e.g., API keys) to ensure security.

6. **Scenario**: You want to set up a continuous integration (CI) workflow for your GitHub repository. How can you configure GitHub Actions to automatically run tests on each push?

   **Answer**:
   1. Create a `.github/workflows` directory in your repository.
   2. Inside this directory, create a YAML file (e.g., `ci.yml`) to define your CI workflow.
   3. Configure the workflow to specify when it should run (e.g., on every push to a specific branch).
   4. Define the steps in your workflow, such as setting up the environment, installing dependencies, and running tests.
   5. Commit and push the YAML file to your repository.
   6. GitHub Actions will automatically detect and run the workflow according to your configuration.

7. **Scenario**: You're experiencing merge conflicts when trying to merge a pull request. How can you resolve these conflicts and complete the merge?

   **Answer**:
   1. Pull the latest changes from the base branch (e.g., `main` or `master`) into your feature branch using `git pull origin main`.
   2. Resolve any merge conflicts in your local code by editing the conflicted files. Git will mark conflict lines with `<<<<<<<`, `=======`, and `>>>>>>>`.
   3. After resolving conflicts, commit the changes.
   4. Push the updated branch to your fork on GitHub.
   5. Go to the pull request on GitHub and click the "Resolve conflicts" button.
   6. GitHub will detect your new push and allow you to complete the merge.

8. **Scenario**: You want to protect the main branch of your repository from direct pushes and require that changes are made through pull requests. How can you set branch protection rules?

   **Answer**:
   1. Go to your repository on GitHub.
   2. Click on "Settings" > "Branches."
   3. Under "Branch protection rules," select the main branch (or the desired branch).
   4. Enable "Require pull request reviews before merging."
   5. You can also add other rules like requiring status checks and branch administrators' approval.
   6. Save the changes.
