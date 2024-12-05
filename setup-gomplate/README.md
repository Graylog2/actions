Gomplate Action
===============

The "setup-gomplate" action is a [composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
that can downloads and installs the [gomplate](https://github.com/hairyhenderson/gomplate) templating tool.

## Usage

```yaml
name: "Setup gomplate"

on:
  workflow_dispatch:

jobs:
  test:
    runs-on: "ubuntu-latest"

    steps:
      - name: "Install gomplate CLI"
        uses: "Graylog2/actions/setup-gomplate@main"
```

## Configuration

### Optional Inputs

- `version`: The gomplate version to install. (default: `latest`, example: `4.2.0`)
