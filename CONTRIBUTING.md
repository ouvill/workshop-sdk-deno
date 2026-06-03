# SPDX-License-Identifier: GPL-3.0-only
# Copyright 2026 Canonical Ltd.

# Contributing to the Deno SDK for Workshop

Thank you for your interest in contributing!

## How to contribute

- **Issues**: Report bugs, suggest enhancements, or ask questions via the
  [issue tracker](https://github.com/canonical/workshop-sdks/issues).
- **Pull requests**: Fork the repository, make your changes, and open a pull
  request. Please ensure your changes pass existing tests and follow the
  project's code conventions.
- **Code of conduct**: All participants must follow the
  [Ubuntu Code of Conduct](https://ubuntu.com/community/ethos/code-of-conduct).

## Development

### Project layout

- `sdkcraft.yaml` — SDK definition file.
- `hooks/` — Lifecycle hooks (setup-base, setup-project, check-health).
- `tests/` — Spread-based integration tests.
- `VERSION` — Published Deno version for this SDK.

### Testing

Tests use the [Spread framework](https://snapcraft.io/docs/spread-tests).

```bash
# Run all tests
spread tests/
```

### License

By contributing, you agree that your contributions will be licensed under the
GPL-3.0-only license.
