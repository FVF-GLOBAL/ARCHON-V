# Repository instructions

- Read `README.md`, `docs/architecture.md`, and `docs/ownership-status.md`
  before changing architecture, legal, or ownership claims.
- Keep monetary values exact. Do not use floating-point types for amounts.
- Keep external financial systems in independent failure domains. Never infer
  atomicity between a bank rail and a blockchain.
- Model accepted, submitted, confirmed, reconciled, legally final, rejected,
  and unknown as distinct outcomes. Do not automatically retry an ambiguous
  command.
- Do not add live provider integrations, custody, signer permissions, or
  production infrastructure without explicit separate authorization.
- Preserve deterministic behavior and typed error paths. Run the smallest
  relevant test, then the documented checks available in the environment.
- Do not claim legal ownership, approvals, certifications, provider integration,
  test results, or formal proofs that have not been verified.
- Keep legal templates clearly marked as unexecuted drafts requiring counsel
  review. Do not add an unverified copyright or license grant.
