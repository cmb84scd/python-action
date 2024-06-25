# Python GitHub Action

This GitHub Action sets up Python, Poetry and Just, as well as using Just to install project dependencies, in your workflow.

It should be noted that this Action uses `Python version 3.12` and `Poetry version 1.8.3`.

## Example workflow

```yaml
name: CI

on: pull_request

jobs:
  <job_name>:
    runs-on: ubuntu-latest
    steps:
      - uses: cmb84scd/python-action@v1
      - run: your code
```
