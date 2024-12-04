+-------------------------------+---------------------------+----------+
| ![](vertopal_b07192           |                           |          |
| 6bcb3f47808ea7498dee393909/me |                           |          |
| dia/image1.png){width="2.4in" |                           |          |
| h                             |                           |          |
| eight="0.5881944444444445in"} |                           |          |
|                               |                           |          |
| SCHOOL OF INFORMATION AND     |                           |          |
| TECHNOLOGY                    |                           |          |
+-------------------------------+---------------------------+----------+
| NAME: **OLIVAS, CARMIE SOPHIA | DATE PERFORMED: **20 NOV  |          |
| N.**                          | 2024**                    |          |
+-------------------------------+---------------------------+----------+
| Section: **IDC1**             | DATE SUBMITTED: **20 NOV  |          |
|                               | 2024**                    |          |
+-------------------------------+---------------------------+----------+

# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

> Git is a distributed version control system that allows multiple
> developers to work on a project simultaneously while tracking changes
> to the source code. It is important in software development because it
> helps manage changes, supports collaboration, provides a history of
> modifications, and allows for easy rollback to previous versions. This
> enhances productivity and minimizes the risk of losing work.

2.  How does Git track changes in a project?

> Git tracks changes through a mechanism called snapshots. Every time a
> change is committed, Git takes a snapshot of the project at that
> moment. Each snapshot is linked to the previous one, creating a
> history of changes. Git stores this information in a .git directory,
> allowing developers to view the history, compare changes, and revert
> to earlier versions if necessary.

3.  What is the difference between a local repository and a remote
    repository in Git?

> A local repository is a version of the project stored on a
> developer\'s machine, allowing them to work offline and make changes
> without affecting others. A remote repository is hosted on a server
> (e.g., GitHub or GitLab) and serves as a centralized location where
> multiple developers can share and collaborate on code. Changes made in
> a local repository can be pushed to the remote repository, and updates
> from others can be pulled.

4.  What are the basic Git commands?

  -----------------------------------------------------------------------
  COMMAND                  FUNCTION
  ------------------------ ----------------------------------------------
  git status               Shows the status of changes in the repository.

  git push                 Uploads local commits to a remote repository.

  git add                  Stages changes for the next commit.

  git branch               Lists, creates, or deletes branches.

  git commit               Records staged changes to the repository.

  git status               Shows the status of changes in the repository.

  git init                 Initializes a new Git repository.

  git push                 Uploads local commits to a remote repository.

  git checkout             Switches branches or restores working tree
                           files.

  git clone                Copies a repository from a remote source.

  git merge                Combines branches together.

  git pull                 Fetches and integrates changes from a remote
                           repo.

  git log                  Shows the commit history.

  git config               Configures user-level settings.

  git remote               Manages connections to remote repositories.

  git reset                Unstages or reverts changes in the working
                           directory.

  git stash                Temporarily saves uncommitted changes.

  git diff                 Shows changes between commits, branches, or
                           files.

  git                      The main command to interact with Git.

  branch                   Refers to a specific branch within a
                           repository.

  git branch \[branch      Creates a new branch.
  name\]                   

  git commit \--amend      Modifies the last commit message or content.

  git commit -m            Commits changes with a message.
  \"\[message\]\"          

  git fetch                Downloads new data from a remote repository.

  git rebase               Integrates changes by rebasing branches.

  git revert               Reverses a specific commit while keeping
                           history.
  -----------------------------------------------------------------------

5.  How do you check the status of a Git repository?

> **git status**
>
> This command shows the current branch, files that have been staged for
> commit, files with changes that haven\'t been staged, and files that
> are not being tracked by Git.

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

> Branches allow developers to work on features, bug fixes, or
> experiments in isolation from the main codebase (usually the \`main\`
> or \`master\` branch). This facilitates parallel development.
>
> To create a branch, use: **git branch \[branch-name\]**
>
> To switch to a branch, use: **git checkout \[branch-name\]**
>
> You can also create and switch in one command with: **git checkout -b
> \[branch-name\]**

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

> GitLab and GitHub are web-based platforms that provide Git repository
> hosting, collaboration features, and additional tools for project
> management. They are different from Git in that Git is the underlying
> version control system, while GitLab and GitHub offer user-friendly
> interfaces and additional features like issue tracking, pull requests
> (in GitHub), and CI/CD pipelines (in GitLab).

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

> **git remote add origin \[repository-url\]**
>
> This command sets up a new remote called \`origin\` that points to the
> specified URL of the remote repository.
>
> After this, you can push changes using **git push origin
> \[branch-name\]**

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

```{=html}
<!-- -->
```
1.  Clone the Repository: Use **git clone \[url\]** to get a local copy
    of the repository.

2.  Create a New Branch: Create a branch for your changes using **git
    checkout -b \[branch-name\]**.

3.  Make Changes and Stage Them: Edit files and use **git add
    \[file-name\]** or **git add .** to stage your changes.

4.  Commit Your Changes: Save your changes with **git commit -m
    \"\[commit message\]\".**

5.  Push Your Branch: Use **git push origin \[branch-name\]** to upload
    your branch to the remote repository.

6.  Create a Pull Request (GitHub) or Merge Request (GitLab): This
    allows others to review and comment on your changes before they are
    merged into the main branch.

7.  Review and Merge: Collaborate with team members to discuss, review,
    and finalize the changes for merging. Then use **git merge
    \[branch-name\].**

```{=html}
<!-- -->
```
10. How do you resolve merge conflicts in Git?

> To resolve merge conflicts:

1.  Identify the conflict. Git will notify you of conflicts after
    attempting a merge.

2.  Open the conflicted file/s and look for conflict markers
    (\`\<\<\<\<\<\<\`, \`======\`, \`\>\>\>\>\>\>\`) that indicate
    conflicting changes.

3.  Manually edit the file and decide how to resolve the differences,
    keeping or modifying code as needed.

4.  After editing, use **git add \[file\]**.

5.  Finally, commit the resolution by using **git commit** to finalize
    the merge.

```{=html}
<!-- -->
```
11. What is a pull request, and why is it used in GitHub?

> A pull request (PR) is a request to merge changes from one branch into
> another in a GitHub repository. It is used to facilitate code review
> and discussion among team members before changes are integrated into
> the main codebase. Pull requests help ensure code quality and
> collaboration, allowing for feedback and additional changes.

12. What are some best practices for writing commit messages?

-   Be Concise and Descriptive: Clearly describe what the commit does.

> Example: **git commit -m \"Add validation for user input\"**

-   Use the Imperative Mood: Write commit messages as if you\'re giving
    a command.

> Example: **git commit -m \"Fix login redirect issue\"**

-   Reference Issues or Tasks: Include references to related issue
    numbers for context.

> Example: **git commit -m \"Fix #123 - Adjust padding for header\"**

-   Avoid Vague Messages: Steer clear of generic phrases like \"Updated
    files\" or \"Changes made.\" Be specific about what was changed.

> Example: **git commit -m \"Remove unused CSS classes\"**

-   Limit the Subject Line to 50 Characters: This ensures the summary is
    concise and easy to read in logs.

> Example: **git commit -m \"Refactor authentication flow\"**

-   Test Before Committing: Ensure your code works as intended before
    committing it to avoid issues with broken code in the repository.

> Example: Run **npm test**, **pytest**, or other test commands before
> committing.

**REFERENCES:**

> \[1\] S. Chacon and B. Straub, *Pro Git*, 2nd ed. Apress, 2014.
> \[Online\]. Available: <https://git-scm.com/book>. \[Accessed: Nov.
> 20, 2024\].
>
> \[2\] GitHub, \"GitHub Docs,\" \[Online\]. Available:
> <https://docs.github.com/en/github>. \[Accessed: Nov. 20, 2024\].
>
> \[3\] GitLab, \"GitLab Docs,\" \[Online\]. Available:
> <https://docs.gitlab.com/ee/>. \[Accessed: Nov. 20, 2024\].
>
> \[4\] R. D. Scott, \"A Guide to Git: A Version Control System,\" in
> *Software Development with Git*, 3rd ed. Addison-Wesley, 2020, pp.
> 45-67.
>
> \[5\] D. S. McKinley, \"Resolving Merge Conflicts in Git,\" *Journal
> of Software Engineering and Applications*, vol. 9, no. 3, pp. 119-132,
> Mar. 2021. \[Online\]. Available:
> https://www.scirp.org/journal/paperinformation.aspx?paperid=110795.
> \[Accessed: Nov. 20, 2024\].
>
> \[6\] M. K. Rowe, \"Pull Requests and Code Review in GitHub,\"
> *International Journal of Web Engineering and Technology*, vol. 22,
> no. 5, pp. 560-578, 2018. \[Online\]. Available:
> https://www.inderscience.com/jhome.php?jcode=ijwet. \[Accessed: Nov.
> 20, 2024\].
