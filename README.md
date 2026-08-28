# Archgate Check

Official GitHub Action to run [Archgate](https://archgate.dev) ADR compliance checks on your repository. Automatically installs Archgate and runs `archgate check --output github`, outputting GitHub annotations for any violations.

## Inputs

| Input     | Required | Default  | Description                                    |
|-----------|----------|----------|------------------------------------------------|
| `version` | No       | `latest` | Archgate version to install (e.g. `v0.14.0`). |

## Usage

```yaml
name: Archgate
on:
  pull_request:
  push:
    branches: [main]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: archgate/check-action@v1
```

## Community

Questions or feedback? Join [r/archgatedev](https://www.reddit.com/r/archgatedev).

## License

[Apache 2.0](LICENSE)
