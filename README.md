# Chalk Pre-Commit

This repository provides configuration which makes it easy to use [chalk's linter](https://github.com/chalk-ai/cli) with [pre-commit](https://pre-commit.com/).

## Usage

In the root of your repository, create a `.pre-commit-config.yaml` file contianing:

```
- repo: https://github.com/chalk-ai/chalk-pre-commit
  rev: 261dbf0
  hooks:
  - id: chalk-lint
```
