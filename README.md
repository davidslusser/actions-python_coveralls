# actions_python_coveralls
A Github action for running pytest with coverage and pushing results to coveralls


<br/>

## How to use
In your .github/workflows directory, create a yaml file (such as main.yaml). Add a job for each desired workflow with the `uses` keyword. Use the `with` keyword to pass any desired variables.

Example:

```
on: [push]

jobs:
  coveralls:
    runs-on: ubuntu-latest
    name: "coveralls"
    steps:
      - uses: davidslusser/actions_python_coveralls@test
        with:
          src: "src"
          options: "--cov=src"
          pip_install_command: "pip install -e .[dev]"
          coveralls_repo_token: ${{ secrets.COVERALLS_REPO_TOKEN }}
```

<br/>

## Inputs
  - **src:** source directory used for code coverage (defaults to "`.`")
  - **options:** optional flags/parameters used in pytest command (defaults to --cov)
  - **pip_install_command:** pip install command (defaults to "`pip install coveralls pytest pytest-cov`")
 

<br/>

## Requirements
 - coveralls account
 - github repo setup on coveralls
 - `COVERALLS_REPO_TOKEN` secret available in your Github actions secrets and variables

    See Coveralls for more details: https://coveralls.io/

