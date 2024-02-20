- During development, all branches are created from the `dev`;
- All PRs merge into `dev`;
- The main branch stores the stable version of the project;

## **The Git flow branches that we are interested in are the following branches:**

- `feat/*` - new functionality, docs, build, CI, test development work;
- `fix/*` - fixes of functionality, docs, build, CI, test development work;
- `settings` - project settings, environment settings;
- `hotfix/*` - urgent fixes to production;

## **The naming of branches:**

`feat (or fix, hotfix)/<task number>-<task name>`

- task number - number of task in trello;
- task name - appropriate task title;

Example: `feat/<387>-authorization`.

## **Working with branches:**

- All branches are created from the `dev` branch (this branch is where development is done), the `main` branch stores the stable version;
- A developer uploads his code to a remote repository. And creates a pull request to the `dev` branch;

#### _Create pull request:_

1. Select the `dev` branch as the base branch.
2. Add a developer to the review.
3. Attach a link to the task in Trello to the task description. In some rare cases you can describe what was done if the task is not in Trello (but it is better to ask to create a card for you).
4. If case when there are conflicts:
   Go to code editor -> From the branch you were working in, create a branch with the same name but specify the flag `clean` `feat/87-cards (clean)` -> Go to `dev` branch and pull changes -> Go back to clean branch and merge `dev` branch -> Upload new branch to remote repository -> Delete old pull request -> Create a new one from clean branch.
5. Drag the card to Trello for review.
6. Send the link of the pull request to the reviewer.
7. Wait for approval and do `Squash and merge` with deletion of the original branch.
8. Drag and drop the card into Trello.
