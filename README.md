# Check the PR head branch name

This action will check the name of the pull request head branch follow the naming convention of the gitflow, and it will fail if it's not follow the below rules:
1. The name of the PR head branch not started with feature/, hotfix/, bugfix/, and release/
2. The hotfix PR not to the main branch.
## How to use:
```
name: "Test Branch Name"
on:
  pull_request:
    types: [opened, edited, reopened, synchronize]
  
jobs:
  test_job:
    runs-on: ubuntu-latest
    name: A job to test branch name
    steps:
      - uses: mhm0ud/github-actions-gitflow@v1
```
