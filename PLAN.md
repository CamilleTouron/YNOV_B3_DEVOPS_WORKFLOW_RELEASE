# Our plan to achieve this release workflow :

## Setting the work environment :
We use Github because it's free, easy to use, well documented and have a large community. With GitHub Action we manage the versionning of the project and to run the workflow.
We use Docker because we need images and containers to implements the CI/CD. We choose Docker for the same reasons that GitHub : free, easy to use, well documented and have a large community.

## Branch handling :
The stable version remains in the branch main.
The devlopment version in dev. Dev is create from main and is merged on main when considered stable.
To implements a feature we will create a branch from dev and merge it back at the end of the devlopement.
When a merge request is sent, we test the development and the merge is done only if the test's result are positive.
