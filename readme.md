# Basics of Git (Creating my First Readme :))

Hi, I am Tanishqua Bansal, trainee engineer at Simform solutions. This repository is where I am practicing hands-on git course. I will include the detailed information of my progress and topics that i have covered so far.

##### Dt. 16 Jan, 2025.

I have started with the udemy course - 

## Rocking Git & GitHub - A Real World Guide by Rajdeep Saha

This course has delved deep inside the realms of Git and GitHub

### 1. Fundamentals of Git

- Git - Version Control System
    - Centralized and Distributed
- Git Workflow
- Environment Setup and GitHub account created.
- Branch
    - Create Branch and switch to it
    ```commmand - git branch <branch-name>; git switch <new-branch>```
    - Pull vs. Fetch+Merge
    - Git Graph Extension (or command: git log --graph)
- Merge
    - Recursive merge or 3-way merge
    - Fast-forward merge

### 2. Real World Git using GitHub

- Pull Request
- First-contributions
    - Fork -> Clone -> Edit -> Pull request
    - Forked the firstcontributions repository and added my name to the contributors list.
    - Keeping remote respository updated using upstream branch
        ```command - git remote add upstream <url-of-upstream>; git pull upstream ```
        Alternatively, do ```Sync Fork``` on the GitHub GUI.
- Solved Merge Conflicts @mergeConflict file.
- Making Markdown Readme.md
- GitHub Issues
    - Issue is registered. Fork the repository, clone, solve and push.
    - Create Pull Request linked to the issue (Use GitHub Documentation.)
    - PR is merged and issue is solved.
- Webhook
    - Jenkins may perform API calls every minute to fetch updated repo from GitHub.
    - This will bombard GitHub server and get only stagnant data back.
    - To overcome this, use webhook.
    - GitHub makes POST call to jenkins(etc.) when repo changed.
- Branching Strategy
    - Trunk Based - Only small features are added periodically to main branch. 
        - Usecase: DevOps, as they require quick feature update. Mature Team.
    - Git Flow - Released based workflow. Rather than small changes, it makes big releases once/month or so.
        - Usecase: New team. New to Git.
        - Requires: Release manager.

## LMS Git Course

Read the theory from the LMS portal.

- Git - Basic Concepts
    - Branching is lightweight compared to CVCS because instead of copying whole code, it simply makes pointer to the new Branch.
    - Git Terminology - Blob, Tree, Commit, Branch, Tag, Clone, Pull, Push, HEAD.
- Environment Setup ```command - git config --global <changes>```
- Life Cycle and General Workflow - [Git and Github Crash Course](https://www.youtube.com/watch?v=SWYqp7iY_Tc&t=639s&ab_channel=TraversyMedia)

##### Dt. 17 Jan, 2025.

## Rocking Git & GitHub - A Real World Guide by Rajdeep Saha

On day 2 of git course, I completed the remaining sections of Udemy Course.

### 3. Git Continued

- Git Revert - creates new commit that undoes any specific previous commit/s.
    - It does not changes the history rather preserves it.
    - ```command - git revert <commit-id>```
- Git Reset - removes the commits from staging area and local repository, but keeps them in working directory.
    - So, if the reset was done accidentally, we can add the files again and commit.
    - ```command - git reset <commit-id>```
    - Remove from working directory as well ? Run ```command - git reset <commit-id> --hard```
- Git Rebase - creates cleaner history compared to merge.
    - Merge makes new commit after merging whereas rebase will simply make copy of commits in feature branch to the main branch.
    - It then deletes the commit id's from the feature branch forever.
    - [In Feature branch]```command - git rebase main``` This will shift the feature branch to the latest commit of main branch.
    - [In Main branch]``` command - git rebase <feature-branch>``` This will add the the commits of feature branch on top of main branch.
- Squash Merge - It helps squash multiple commit into single commit.
    - ```command - git rebase -i HEAD~<number-of-commits-to-merge>``` then use squash keyword from Vim [^1]
    - In Vim, write new commit message. Now the commits are squashed. 
    - Merge or Rebase the feature branch to main branch.
- Reorder Commit - using interative (-i) rebase we can reorder the commits.
    - In interactive Vim, change the order of commits and save.
- Cherry Pick - it only merges specific commit from feature branch to main branch.
    - Just like rebase, it also creates new commit for cherry-picked commit.
    - ```command- git cherry-pick <commit-id/s>```
- Git Stash - it saves the unstaged work of current working directory before switching branch.
    - ```command- git stash save -m "comment-as-per-need"``` saves the unstaged changes with a 'index state' and branches can be switched now.
    - ```command- git stash list``` lists all the index states in stash.
    - ```command- git stash apply <number-of-index-state>``` restores the changes of that stash in working directory.
    - ```command- git clear``` deletes the stash.

### 4. Git and GitHub Interview Prep

- Get Recruiters attention
    - Make Readme.md, include 1. Usecase, 2. What i learned, 3. How to run?
    - Don't just fork and clone, personalize it.
    - Update profile with picture and personal details.
- 5 impressive projects
    - Consume [APIs](https://github.com/public-apis/public-apis)
    - Frontend website - online store
    - Create API - for backend jobs
    - Own resume website

- Imp questions
    - List all files changed in a particular commit ?
        - ```command- git show <commit-id>``` shows the differences of files changed
        - ```command- git alias -tree``` shows only the name of file changed
    - How to know which branches are merged ?
        - ```command- git branch --merged``` tells which branches are merged to current branch.
        - for not merged branches, replace ```--merged``` with ```--no-merged```
    - What is git remote add and git clone ?
        - Git remote add - adds the remote repository url to local. 
        - Git clone - makes a local copy of remote repo as well as brings the commit history.
    - List all files changed in all commits ?
        - ```command- git log --stacked```
    - How to keep forked repo updated ?
        - ```command - git remote add upstream <url-upstream-repo>``` Adds remote upstream url. 
        - ```command - git pull upstream``` Fetches and merges the changes from upstream repo.
        - ```command - git push origin main``` Pushes the changes of upstream (from local repo to remote origin).

Voila, with that WE (You[Viewer] and I[Tanishqua]) have successfully finished this Udemy Course!

## LMS Git Course

Let's jump in to our Git - Practical Exam. Wish me luck!

Okay, so I have successfully completed the exam, here is the link to the [repo.](https://github.com/Tanishqua-Simform/Git-Practical-Exam/)

## Finishing Touch

- Went through [Official Documentation](https://git-scm.com/docs) and [GitHub Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/)
- Visualized git commands using [tools.](https://git-school.github.io/visualizing-git/)

##### With this we come to an end for our Git Course (Learning duration - 2 days).

[^1]: In Vim editor, press 'i' to insert, ':wq' to save the file.