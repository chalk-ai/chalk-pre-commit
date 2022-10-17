# Chalk Pre-Commit

This repository provides configuration which makes it easy to use [chalk's linter](https://github.com/chalk-ai/cli) with [pre-commit](https://pre-commit.com/).

## Usage

First, in the root of your repository, create a `.pre-commit-config.yaml` file containing:

```
repos:
- repo: https://github.com/chalk-ai/chalk-pre-commit
  rev: 24e01cf
  hooks:
  - id: chalk-lint
```

If you already have a .pre-commit-config.yaml file, just add this alongside other pre-commit hook config under the `repos` key.


Then, run: `pre-commit install` to initialize your pre-commit setup. From now on, when you run `git commit`, `chalk lint` will execute.
