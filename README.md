![](https://github.com/cwaymeyer/react_deployment_template/workflows/CI/badge.svg?branch=develop&event=push)

# React project template

This template bootstraps a React project with CI/CD workflows through GitHub Actions.

Benefits:

- Keep a clean and organized development process.
- Automatate testing and deployment of code to staging and production environments.
- Automatically upload artifacts and coverage reports.

<hr />

## To use

### Set up repository

- Create a new repo on GitHub
- Clone this repository to your machine - `git clone https://github.com/cwaymeyer/react_deployment_template.git`
- Set origin to your repo - `git remote set-url origin <your-repo-url>` (`git remote --v` to verify)

### Set branch structure

Your branch used for production/deployment is the default branch, <b>master</b>. For CI/CD to work correctly, you must create a branch off of master, <b>develop</b>. This will be your staging branch.

All features and updates should be made through a unique branch, and PR's made to <b>develop</b>.

<img src="./branches_flow.jpg" width="500"/>

### Set up Surge

### Customize workflow

The workflow for this project can be found at [`.github/workflows`](https://github.com/cwaymeyer/react_deployment_template/blob/master/.github/workflows/ci.yml).

> <b>Properties to update:</b>
>
> - `STAGING_URL (line 14)`
> - `PRODUCTION_URL (line 15)`

For more information on GitHub Actions, see [the docs](https://docs.github.com/en/actions).

### Set GitHub Secrets

In your GitHub repository, navigate to <b>Settings</b> ➡ <b>Secrets</b> ➡ <b>Actions</b>. Create two secrets with the following values:

> - `SURGE_LOGIN` (your surge id)
> - `SURGE_TOKEN` (your surge password)
