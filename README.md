# Infinitech Multi-Cloud Landing Zone — Reference Delivery & Evidence

This repository is a public, synthetic evidence package for evaluating the
Infinitech Multi-Cloud Landing Zone (IMCLZ) service. It shows what enters the
governed delivery path, what customer-facing output is produced, how unsafe
changes are rejected, and what lifecycle evidence was retained across AWS,
Azure, Google Cloud, and Oracle Cloud Infrastructure.

It is deliberately **not** a deployable product distribution. Reusable modules,
request-processing engines, policy source, cloud trust, and operational
automation are part of Infinitech's private product and customer engagement.

## Start here: the 10–15 minute evidence path

1. [Watch the 6:24 technical walkthrough](https://media.infinitechplatforms.com/imclz/v4/infinitech-technical-walkthrough.mp4).
   Its request-through-drift footage remains the canonical product
   demonstration. Its final customer-delivery chapter records the superseded
   public packaging model; this repository and the adaptation guide below are
   the current publication boundary.
2. Read the [architecture](docs/architecture.md) and
   [provider design decisions](docs/design-decisions.md).
3. Compare the four synthetic [requests](examples/requests/) with their
   complete safe [generated roots](examples/generated/).
4. Inspect the passing and intentionally rejected results under
   `examples/policy-results/` and the [acceptance evidence](evidence/acceptance.md).
5. Review [customer adaptation](docs/customer-adaptation.md) to understand why
   production delivery requires an Infinitech engagement, then verify the
   [current evidence release](https://github.com/mikejmckinney/infinitech-multi-cloud-landing-zone-evidence/releases/tag/v0.1.2).

## What the evidence demonstrates

| Capability | Public evidence |
|---|---|
| Request to provider configuration | Four synthetic requests and deterministic generated Terraform roots |
| Prevention before cloud writes | Passing and intentional rejection policy-result snapshots |
| Protected execution | Checksum-bound prepare/approval/execute evidence in the walkthrough |
| Four-provider implementation | Sanitized provider-console proof and acceptance results |
| Evidence and lifecycle | Dashboard, teardown, and drift-routing media with scoped limitations |
| Customer-owned delivery | Architecture and adaptation guidance for a private customer repository |

## Feature evidence

- [Request to configuration](https://media.infinitechplatforms.com/imclz/v1/request-vending.mp4)
- [Policy prevention](https://media.infinitechplatforms.com/imclz/v1/policy-prevention.mp4)
- [Protected execution](https://media.infinitechplatforms.com/imclz/v1/protected-execution.mp4)
- [Four-cloud deployment](https://media.infinitechplatforms.com/imclz/v1/four-cloud-execute.mp4)
- [Evidence dashboard](https://media.infinitechplatforms.com/imclz/v1/evidence-dashboard.mp4)
- [Clean teardown](https://media.infinitechplatforms.com/imclz/v1/verified-teardown.mp4)
- [Drift detection](https://media.infinitechplatforms.com/imclz/v1/drift-detection.mp4)
- [Customer-owned delivery boundary](docs/customer-adaptation.md)

The former customer-delivery feature clip is not linked because it depicts the
superseded operational-style public package. It remains in the private media
record for provenance; it is not evidence of the current public boundary.

## Publication boundary

This package contains interfaces, decisions, complete safe outputs, results,
and evidence. It does not contain:

- reusable Terraform modules or platform/environment implementation roots;
- request generators, validators, or rendering engines;
- the Rego policy implementation or its complete test suite;
- cloud bootstrap, identity, trust, plan, execution, teardown, drift, or
  rollback automation; or
- credentials, provider tokens, Terraform state, saved plans, or customer
  identifiers.

The generated roots reference intentionally withheld modules. They are complete
customer-facing examples, but they cannot create cloud resources by themselves.

## Provenance and limitations

`PROVENANCE.json` identifies the private product revision used to create this
evidence without publishing the private source repository. `SHA256SUMS` covers
every shipped file other than the checksum manifest itself. The static public
workflow verifies evidence integrity only; it does not regenerate or deploy the
product.

Point-in-time findings, resource counts, and workflow outcomes are evidence of
the recorded scenarios—not universal compliance, reliability, cost, or service
level claims. Complete provider-settled cost remains unavailable.

## Discuss an implementation

Every production delivery is adapted to the customer's organizations, identity,
network, regions, controls, operating model, and ownership boundaries. Contact
[hello@infinitechplatforms.com](mailto:hello@infinitechplatforms.com) to request
a cloud-governance readiness discussion.

Use of this repository is governed by the [Infinitech LLC Public Evaluation
Terms](LICENSE).
