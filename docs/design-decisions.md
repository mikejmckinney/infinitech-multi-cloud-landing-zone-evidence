# Provider design decisions

The four clouds share a request and control model, but their APIs and hierarchy
semantics are not treated as identical.

| Concern | AWS | Azure | Google Cloud | OCI |
|---|---|---|---|---|
| Governed scope | Organization account | Subscription | Project | Compartment |
| Parent boundary | Organizational unit | Management group | Folder | Tenancy or compartment |
| Vending stages | Account, then member baseline | Subscription, then subscription baseline | Project and baseline in one provider context | Compartment and baseline in one provider context |
| Central evidence | Organization logging and Security Hub | Log Analytics, Policy, and Defender | Log Router and Security Command Center | Logging and Cloud Guard |
| Region handling | Explicit regional baseline invocation | Subscription controls plus allowed locations | Project services and location policy | Provider region plus allowed-region controls |

## Why prepare and execute are separate

Terraform plans are review artifacts, not merely command previews. IMCLZ retains
the saved plan, policy result, source mapping, and checksum during preparation.
Execution requires the successful prepare run and exact confirmation data, then
uses a distinct write-capable identity. This does not claim two-person
separation of duties; the customer chooses reviewers and approval policy.

## Why provider modules remain separate

Terraform associates resources with provider configurations statically. A
single runtime-selected provider module would load unrelated provider
requirements and cannot safely configure a provider from a scope identifier
that is created in the same apply. Provider-specific roots make authentication,
state, rollback, and responsibility boundaries explicit.

## Why public outputs retain module references

The generated roots are the interface a customer reviewer sees. Publishing them
without the underlying modules demonstrates naming, tags, variables, staged
boundaries, and provider differences without distributing the reusable engine.
