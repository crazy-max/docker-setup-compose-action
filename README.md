[![GitHub release](https://img.shields.io/github/release/docker/setup-compose-action.svg?style=flat-square)](https://github.com/docker/setup-compose-action/releases/latest)
[![GitHub marketplace](https://img.shields.io/badge/marketplace-docker--setup--compose-blue?logo=github&style=flat-square)](https://github.com/marketplace/actions/docker-setup-compose)
[![CI workflow](https://img.shields.io/github/actions/workflow/status/docker/setup-compose-action/ci.yml?branch=master&label=ci&logo=github&style=flat-square)](https://github.com/docker/setup-compose-action/actions?workflow=ci)
[![Test workflow](https://img.shields.io/github/actions/workflow/status/docker/setup-compose-action/test.yml?branch=master&label=test&logo=github&style=flat-square)](https://github.com/docker/setup-compose-action/actions?workflow=test)
[![Codecov](https://img.shields.io/codecov/c/github/docker/setup-compose-action?logo=codecov&style=flat-square)](https://codecov.io/gh/docker/setup-compose-action)

## About

GitHub Action to set up Docker [Compose](https://github.com/docker/compose).

![Screenshot](.github/setup-compose-action.png)

___

* [Usage](#usage)
* [Customizing](#customizing)
  * [inputs](#inputs)
* [Contributing](#contributing)

## Usage

```yaml
name: ci

on:
  push:

jobs:
  compose:
    runs-on: ubuntu-latest
    steps:
      -
        name: Checkout
        uses: actions/checkout@v4
      -
        name: Set up Docker Compose
        uses: docker/setup-compose-action@v1
```

## Customizing

### inputs

The following inputs can be used as `step.with` keys:

| Name           | Type   | Default | Description                                                                     |
|----------------|--------|---------|---------------------------------------------------------------------------------|
| `version`      | String |         | [Compose](https://github.com/docker/compose) version. (eg. `v2.32.4`, `latest`) |
| `cache-binary` | Bool   | `true`  | Cache compose binary to GitHub Actions cache backend                            |

## Contributing

Want to contribute? Awesome! You can find information about contributing to
this project in the [CONTRIBUTING.md](/.github/CONTRIBUTING.md)