# run-pytest

GitHub action that runs pytest.

# Installing

Create and commit `.github/workflows/run-pytest.yml` in your repo.

```yml
name: Run Pytest

# For example, run it on PRs
on:
  pull_request:

jobs:
  black-suggest:
    runs-on: ubuntu-latest
    steps:
      # Check out the repository
      - uses: actions/checkout@v2

      # Run the action that comments with suggestions
      - uses: cloudtostreet/run-pytest@v1
        with:
          # The directory to run pytest on. Use "." for everything.
          path: "."
```
