# source.ag Python package publisher

For all your Python package publishing needs.

Usage:


```yaml
name: source-cdk-patterns-publish

on:
  pull_request:
    types: [closed]
    branches:
      - main

jobs:
  publish:
    if: github.event.pull_request.merged
    runs-on: ubuntu-latest
    steps:
      - name: Publish
        uses: source-ag/source-actions-gitlab-python-taskdef@v1.2
        with:
          gitlab-token-user: ${{ secrets.GITLAB_TOKEN_USER }}
          gitlab-token: ${{ secrets.GITLAB_TOKEN }}
```
