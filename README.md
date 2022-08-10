![](https://github.com/cwaymeyer/react_deployment_template/actions/workflows/dev.yml/badge.svg?branch=develop&event=push)
![](https://github.com/cwaymeyer/react_deployment_template/actions/workflows/prod.yml/badge.svg?branch=master&event=push)

# React project template

#### ⚠ README CURRENTLY OUT OF DATE

This template bootstraps a React project with CI/CD workflows through GitHub Actions.

Benefits:

- Keep a clean and organized development process.
- Automatate testing and deployment of code to staging and production environments.
- Automatically upload artifacts and coverage reports.

<hr />

## 💻 To use 💻

### 1. Select 'Use this template'

[Creating a repo from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template)

### 2. Set branch structure

Your branch used for production/deployment is the default branch, <b>master</b>. For CI/CD to work correctly, you must create a branch off of master, <b>develop</b>. This will be your staging branch.

All features and updates should be made through a unique branch, and PR's made to <b>develop</b>.

<img src="./branches_flow.jpg" width="600"/>

The above process is <b>necessary</b> for the workflow to work as intented. Beyond develop and master, you can use any branch name you like.

### 3. Set up Surge

- Install surge (`npm install -g surge`)
- Run `surge` to create a domain. <i>You will want to do this twice and set two different domains - one for staging and one for production</i>. Must have a Surge account.

[Reference video](https://www.youtube.com/watch?v=-EjdMvYPSVU&t=55s)

### 4. Link repository to Codecov

For code coverage reporting, you must register your repository with Codecov. Instructions found [here](https://docs.codecov.com/docs).

### 5. Customize workflows

The workflows for this project can be found at [`.github/workflows`](https://github.com/cwaymeyer/react_deployment_template/blob/master/.github/workflows).

> <b>Properties to update in `push.yml`:</b>
>
> - `STAGING_URL (line 14)`
> - `PRODUCTION_URL (line 15)`

Update lines 14-15 with the staging and production URLs you set in step 3.

<hr />

<b>This workflow will run on a PR or push to the develop or master branch</b>.

For more information on GitHub Actions, see [the docs](https://docs.github.com/en/actions).

<hr />

### 6. Set GitHub Secrets

In your GitHub repository, navigate to <b>Settings</b> ➡ <b>Secrets</b> ➡ <b>Actions</b>. Create two secrets with the following keys and values:

> - `SURGE_LOGIN` - your Surge ID
> - `SURGE_TOKEN` - your Surge password

### You are now ready to begin adding your own code and deploying!
