# Security policy

## Scope

The current scope is the source code and development configuration in this
repository. There are no supported production deployments or live financial
integrations.

## Reporting

Do not disclose suspected vulnerabilities publicly before coordinated
assessment. The repository has no verified private security contact yet. Until
one is established, do not include sensitive exploit details, credentials, or
customer data in public issues; contact a verified FVF-GLOBAL security
representative through an independently known channel.

## Security expectations

- Never commit credentials, private keys, or production secrets.
- External financial outcomes must remain explicit and independently
  reconcilable; an ambiguous command must not be blindly retried.
- Do not enable live execution, custody, signing, or production infrastructure
  from this repository without separately authorized controls.
- Dependency changes should be locked, reviewed, and tested.

Security reports and fixes are not evidence of certification or a completed
security audit.
