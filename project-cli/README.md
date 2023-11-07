Project CLI Action
==================

The "project-cli" action is a [composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
that can downloads and installs the [graylog-project CLI](https://github.com/Graylog2/graylog-project-cli).

## Usage

```yaml
name: "Test project CLI"

on:
  workflow_dispatch:

jobs:
  test:
    runs-on: "ubuntu-latest"

    steps:
      - name: "Install Graylog Project CLI"
        uses: "Graylog2/actions/project-cli@main"
```

## Configuration

### Optional Inputs

- `cli-version`: [graylog-project-cli](https://github.com/Graylog2/graylog-project-cli) version. (default: `latest`, example: `0.40.0`)
