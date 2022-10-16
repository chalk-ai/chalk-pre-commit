# Chalk Pre-Commit

This repository provides configuration which makes it easy to use [chalk's linter](https://github.com/chalk-ai/cli) with [pre-commit](https://pre-commit.com/).

## Usage

First, in the root of your repository, create a `.pre-commit-config.yaml` file containing:

```
- repo: https://github.com/chalk-ai/chalk-pre-commit
  rev: 261dbf0
  hooks:
  - id: chalk-lint
```


Then, run: `pre-commit install` to initialize your pre-commit setup. From now on, when you run `git commit`, `chalk lint` will execute.
