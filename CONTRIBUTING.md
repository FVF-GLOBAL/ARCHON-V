# Contributing

## Scope and review

Changes should be small, testable, and consistent with
[the architecture boundaries](docs/architecture.md). A pull request should
explain the behavior changed, failure modes considered, test commands run, and
any remaining verification limitations. Financial execution, key custody,
signer access, production infrastructure, or external provider integrations
require explicit separate authorization and review.

## Local checks

```sh
cargo fmt --all -- --check
cargo test --locked
cargo clippy --workspace --all-targets --all-features -- -D warnings
```

For changes to core state or monetary invariants, also run the Kani harnesses
and relevant fuzz targets where the required tools are available. Record
unavailable checks as blockers; do not weaken a test to obtain a passing result.

## Dependencies and generated files

Keep dependencies minimal, commit `Cargo.lock`, and use `--locked` in CI. Do not
commit credentials, private keys, provider secrets, customer data, or generated
build output. New dependencies need a clear need and maintenance/security
review.

## Legal and ownership material

Legal templates are drafts, not legal advice or executed agreements. Only
authorized counsel and verified entity representatives may approve them.
Ownership and code-review assignments are intentionally left unresolved until
the identity and authority of the relevant entities and maintainers are
verified; see [ownership status](docs/ownership-status.md).
