# Python GitHub Action

This GitHub Action sets up Python, Poetry and Just, as well as using Just to install project dependencies, in your workflow.

It should be noted that, by default, this Action uses `Python version 3.12` and `Poetry version 1.8.3` but you can pass in your preferred version if you don't want ot use the defaults.

## Examples

### Workflow using default versions

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

### Workflow passing in Python and Poetry versions

```yaml
name: CI

on: pull_request

jobs:
  <job_name>:
    runs-on: ubuntu-latest
    steps:
      - uses: cmb84scd/python-action@v1
        with:
          poetry-version: 'latest'
          python-version: '3.10'
      - run: your code
```
