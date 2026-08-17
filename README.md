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

1. [Watch the 6:30 technical walkthrough](https://github.com/user-attachments/assets/e8e092a7-8a9e-4e68-ba37-0691ec61da14).
2. Read the [architecture](docs/architecture.md) and
   [provider design decisions](docs/design-decisions.md).
3. Compare the four synthetic [requests](examples/requests/) with their
   complete safe [generated roots](examples/generated/).
4. Inspect the passing and intentionally rejected results under
   `examples/policy-results/` and the [acceptance evidence](evidence/acceptance.md).
5. Review [customer adaptation](docs/customer-adaptation.md) to understand why
   production delivery requires an Infinitech engagement.

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

- [Request to configuration](https://github.com/user-attachments/assets/06b260f9-733c-4664-bf6c-46cf70a718b3)
- [Policy prevention](https://github.com/user-attachments/assets/4c1d1e0f-4157-4811-8589-d96236d72394)
- [Protected execution](https://github.com/user-attachments/assets/d30f8560-8bbb-40bc-a472-1d48a4cb82eb)
- [Four-cloud deployment](https://github.com/user-attachments/assets/fc7c8482-1c91-4b71-b4e6-b18a7a274177)
- [Evidence dashboard](https://github.com/user-attachments/assets/4ca94d0a-0f1b-4e8a-9de9-58714651bd1e)
- [Clean teardown](https://github.com/user-attachments/assets/79d9adc2-5407-4c25-b3f4-60e60f555163)
- [Drift detection](https://github.com/user-attachments/assets/fdce9de2-d984-48c6-9f3b-e5355f7f9750)
- [Customer-owned delivery](https://github.com/user-attachments/assets/d39abe34-356c-428e-91b0-d5b5293cec47)

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
