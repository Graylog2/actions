Changelog Check Action
======================

The "changelog-check" action is a [composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
that can be used to validate the existence and format of changelog snippets.

## Usage

Add the following workflow to `.github/workflows/changelog.yml` in your repository.

```yaml
name: "Changelog Check"

on:
  pull_request:
    types:
      - "opened"
      - "synchronize"
      - "reopened"
      - "edited"

jobs:
  test:
    name: "Check"
    runs-on: "ubuntu-latest"

    steps:
      - uses: "Graylog2/actions/changelog-check@main"
        with:
          gh-token: "${{ secrets.GITHUB_TOKEN }}"
```

## Configuration

### Inputs

- `gh-token`: A GitHub token that allows access to the REST API for the repository. (e.g., `secrets.GITHUB_TOKEN`)
