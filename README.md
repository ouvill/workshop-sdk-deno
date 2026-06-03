# Deno SDK for Workshop

This SDK provides the Deno runtime for secure JavaScript and TypeScript
development within a workshop. The Deno module cache and user configuration
are persisted across workshop updates.

---

## Reference workshop

A minimal workshop:

```yaml
# workshop.yaml
name: deno-dev
base: ubuntu@24.04
sdks:
  - name: ouvill-deno
    channel: latest/stable

actions:
  hello-deno: |
    deno run https://docs.deno.com/examples/hello-world.ts
```

This installs Deno and makes the `deno` command available on the PATH.

---

## Using the SDK

### Prerequisites and project layout

1. No prerequisite SDKs are required.
2. No specific project layout is needed.
3. On launch, Deno is added to PATH and the environment is configured. The
   Deno module cache (`/home/workshop/.cache/deno`) and the Deno install
   directory (`/home/workshop/.deno`) are persisted across workshop updates.

### Run Deno scripts

```bash
workshop shell
deno run https://docs.deno.com/examples/hello-world.ts
```

### Verify from the command line

```bash
workshop shell
deno --version
```

---

## Plugs (resources this SDK consumes)

### `deno-cache`

- Interface: `mount`
- Workshop target: `/home/workshop/.cache/deno`
- Purpose: Persists the Deno module cache (`DENO_DIR`) across workshop updates,
  so cached dependencies are not re-downloaded on refresh.

### `deno-data`

- Interface: `mount`
- Workshop target: `/home/workshop/.deno`
- Purpose: Persists Deno user data (`DENO_INSTALL`), including globally
  installed scripts and configuration, across workshop updates.

## Slots (resources this SDK provides)

This SDK doesn't define any slots.

---

## Documentation and guidance

- [Deno official documentation](https://docs.deno.com/)
- [Workshop documentation](https://ubuntu.com/workshop/docs/)

---

## Community and support

- [Deno community](https://deno.com/community):
  [Discord](https://discord.gg/deno)
- Workshop forum:
  [Discourse](https://discourse.ubuntu.com/)
- Please review our
  [Code of Conduct](https://ubuntu.com/community/ethos/code-of-conduct) before
  participating.

---

## Contributions

All contributions, including code, documentation updates, and issue reports,
are welcome!

- See `CONTRIBUTING.md` for guidelines.
- Open issues or pull requests on the official repository.

---

## License and copyright

Copyright 2026 Canonical Ltd.

This SDK is licensed under the GPL-3.0-only license.

Deno is licensed under the
[MIT License](https://github.com/denoland/deno/blob/main/LICENSE.md).
