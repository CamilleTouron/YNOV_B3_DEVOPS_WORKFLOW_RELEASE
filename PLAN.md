# Our plan to achieve this release workflow :

## Setting the work environment :
We use Github because it's free, easy to use, well documented and have a large community. With GitHub Action we manage the versioning of the project and run the workflow.
We use Docker because we need images and containers to implement the CI/CD. We choose Docker for the same reasons as GitHub : free, easy to use, well documented and have a large community.

## Branch handling :
The stable version remains within the main branch.
The development version in dev branch. dev is created from the main and is merged to main when stable.
To implement a feature we will create a branch from dev and merge it back at the end of the development.
When a merge request is sent, we test the development and the merge is done only if the test's result is positive.
For testing the workflow we use the release branch who will test and then merge with the main branch
## Steps of the workflow's :
GitHub action workflow :
1 - Push on release branch. 
2 - GitHub action run npm to launch API 
3 - GitHub action run npm, and curl to test the app
    IF test ok
    4 - GitHub action push on main branch. 
    5 - GitHub action build image from main branch. 
    6 - GitHub action deploy on Scaleway. 
    IF test Nok
    7 -Alert The one who pushed 

Jenkins workflow :
### 

## Organisation
Marco Scaleway
Kevin Scaleway
Camille Github action
Etienne Github action

