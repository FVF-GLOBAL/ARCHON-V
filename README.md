# ARCHON-V

ARCHON-V is an incrementally developed, hybrid polyglot financial-infrastructure
monorepo. The current implementation is a deterministic Rust domain core; it
does not connect to banks, blockchains, custody systems, signers, or production
infrastructure.

## Status

This repository is at the engineering-baseline and deterministic-core stage.
Nothing in this repository authorizes live financial execution, custody, signer
permissions, or production deployment. Financial outcomes from external
institutions are not treated as atomic with one another.

Repository ownership, the legally correct FVF entity name, copyright holder,
license, and code-owner identities have not been independently verified. See
[the ownership status](docs/ownership-status.md) before relying on any legal or
governance statement.

## Build and test

Requirements: stable Rust (the minimum supported version is stated in
`Cargo.toml`) and Cargo.

```sh
cargo test --locked
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D warnings
```

Bounded verification is available with Rust Kani:

```sh
cargo install --locked kani-verifier
cargo kani setup
cargo kani --package archon-v-core
```

Kani is a bounded model checker, not a proof of all executions. Assumptions and
coverage limits are recorded in [the verification notes](docs/verification.md).
The fuzz target under `fuzz/` requires `cargo-fuzz`; it is not part of the
ordinary workspace build.

See [CONTRIBUTING.md](CONTRIBUTING.md) for local checks and [the architecture
overview](docs/architecture.md) for current scope and boundaries.
