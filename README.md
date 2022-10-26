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


## Usage with GitHub Action

This `chalk-pre-commit` plugin assumes that you have `chalk` and `chalkpy` available on your `PATH`.

In GitHub Actions, you can ensure this by first installing your `pip` requirements, and then using either chalk-ai/cli-action or chalk-ai/deploy-action:

```
steps:
- uses: actions/setup-python@v4
  with:
    python-version: '3.10'
    cache: 'pip'

- name: "Install dependencies"
  run: pip install -r requirements.txt

- uses: chalk-ai/cli-action@v1
  with:
    client-id: ...
    client-secret: ...

- uses: pre-commit/action@v3.0.0
```
