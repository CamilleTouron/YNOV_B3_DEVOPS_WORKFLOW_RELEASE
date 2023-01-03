# Our plan to achieve this release workflow :

## Setting the work environment :
We use Github because it's free, easy to use, well documented and have a large community. With GitHub Action we manage the versioning of the project and run the workflow.
We use Docker because we need images and containers to implement the CI/CD. We choose Docker for the same reasons as GitHub : free, easy to use, well documented and have a large community.

## Branch handling :
The stable version remains within the main branch.
The development version in dev branch. dev is created from the main and is merged to main when stable.
To implement a feature we will create a branch from dev and merge it back at the end of the development.
When a merge request is sent, we test the development and the merge is done only if the test's result is positive.
