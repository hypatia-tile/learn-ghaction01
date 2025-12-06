# learn-ghactions

## Check Articles

[Hello World in GitHub Actions](https://dev.to/sre_panchanan/hello-world-in-github-actions-a-beginners-guide-to-your-first-workflow-1mbh)
## Note

Added `.github/workflows/main.yml` file to create a GitHub Action.

```yml
name: CI

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Get Your Code
        uses: actions/checkout@v2

      - name: Say Hello to the World
        run: echo "Hello, World!"
```

## Concerns

- What is `actions/checkout@v2`?

[answer](https://github.com/orgs/community/discussions/25682)

It is an official GitHub Action used to check-out a repository so a workflow can access it.

Action for checking out a repo.
Contribute to `actions/checkout` development by creating an account on GitHub.

By default, this action will check-out to the `SHA` for that workflow’s event
(such as push and pull_request). Otherwise, uses the default branch (usually main or master in a standard repository).

See also :
[behavior of checkout versions](https://qiita.com/uyuni/items/2f2a8ce4fef3712f1b74)

## Workflow dispatch

See also : [GitHub Actions を workflow_dispatch で切り分ける](https://zenn.dev/tetoteto/articles/github_actions_workflow_dispatch_call)

