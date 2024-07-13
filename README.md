# Overview

`d33pster/automated-pytest` is an action that can be used to automatically perform all the operations needed to run `pytest` for your python projects.

## README

* **[Before we begin]** You can also add `d33pster/python-project-structure@v3.5` to your workflow file to maintain the dir-structure in accordance with [`PYPI`](https://pypi.org). Checke it out [here](https://github.com/marketplace/actions/python-project-structure).

* To begin with the action, create `.github/workflows/` in your repository and create a `filename.yml` or `filename.yaml` inside it, where `filename` can be anything of your choice. For this example, lets say `filename=ContinuousIntegration`

* Start writing `ContinuousIntegration.yml`

  ```yaml
  # This workflow will continuously run pytest on each push 

  name: Continuous Integration

  on:
    push:
        branches:
            - '*'
            - '*/*'
            - '**'

  permissions: read-all

  jobs:
    continuous_integration:
        runs-on: ubuntu-latest

        steps:
        - uses: d33pster/automated-pytest@v1.1
  ```

  After creating this file, and pushing the changes to the repository, on each push starting from this one, pytest will run.

## Issues

* Any issues found should be added [here](https://github.com/d33pster/automated-pytest/issues).

## Pull Requests

* Pull requests are welcome and encouraged.