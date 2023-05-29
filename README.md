# actions_python_coveralls
A Github action for running pytest with coverage and pushing results to coveralls


<br/>

## How to use
In your .github/workflows directory, create a yaml file (such as main.yaml). Add a job for each desired workflow with the `uses` keyword. Use the `with` keyword to pass any desired variables.

Example:

```

```

<br/>

## Inputs
  - **src:** source directory used for code coverage (defaults to "`.`")
  - **options:** optional flags/parameters used in pytest command
  - **pip_install_command:** pip install command (defaults to "`pip install coveralls pytest pytest-cov`")
  - **py-version:** version of python to use (defaults to "`3.x`")


<br/>

## Requirements
 - coveralls account
 - github repo setup on coveralls
 - `COVERALLS_REPO_TOKEN` secret available in your Github actions secrets and variables

    See Coveralls for more details: https://coveralls.io/

