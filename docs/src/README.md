# [cargo-deny](https://github.com/EmbarkStudios/cargo-deny)

cargo-deny is a cargo plugin that lets you lint your project's dependency
graph to ensure all your dependencies conform to your expectations and
requirements.

## Quickstart

Installs cargo-deny, initializes your project with a default configuration,
then runs all of the checks against your project.

```bash
cargo install cargo-deny && cargo deny init && cargo deny check
```

## Command Line Interface

cargo-deny is primarily intended to be used as a CLI, see
[Command Line Tool](cli/index.html) for the available commands and their options.

## Checks

cargo-deny supports several classes of checks, see the
[Checks](checks/index.html) for the available checks and their configuration
options.

## API

cargo-deny is primarily meant to be used as a cargo plugin, but a majority of
its functionality is within a library whose docs you view on
[docs.rs](https://docs.rs/cargo-deny)

## GitHub Action

For GitHub projects one can run cargo-deny automatically as part of continous integration using a GitHub Action:

```yaml
name: CI
on: [push, pull_request]
jobs:
  cargo-deny:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - uses: EmbarkStudios/cargo-deny-action@v0
```

For more information, see [`cargo-deny-action`](https://github.com/EmbarkStudios/cargo-deny-action) repository.