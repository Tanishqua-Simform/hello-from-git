# Creating my First Readme

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