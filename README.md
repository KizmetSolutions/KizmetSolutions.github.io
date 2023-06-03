# Kizmet Solutions websit

This repo hosts the public code that is deployed to Github Pages.

## Source

Private repository builds a static website that is pushed when new content is added. This push is received here as a PR to `main` that needs to be approved in order to be merged and then deploy the changes.

## Main branch

`main` branch is protected so no direct pushes are allowed. The PR mechanism is the only allowed method to update the content. Review of the PR by CODEOWNERS is mandatory, and 1 approval is required.

The static content is expected to be submitted directly to the root folder of the repo.

## Deployment

If `main` receives a push through a PR merge, the `deploy.yml` workflow is triggerd and the public website will be updated.

By default, when pushing content to Github Pages, a `Jekyll` parser would be triggered to build the static website. In our case, the static content is already submitted, so we just need to publish it. To prevent `Jekyll` trying to parse content that it does not understand we have this `.nojekyll` file in the root path of the repository.
