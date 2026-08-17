# Customer adaptation

IMCLZ is delivered as an adapted implementation, not a universal template that
can be enabled safely without discovery. A production engagement resolves at
least the following decisions in the customer's own environment.

| Area | Customer-specific decisions |
|---|---|
| Cloud hierarchy | Existing organizations, management groups, folders, tenancies, delegated administrators, and allowed child scopes |
| Identity and trust | Identity provider, GitHub organization, OIDC subjects, plan and execution roles, emergency access, and rotation ownership |
| Network and IPAM | Hub/spoke or transit topology, address allocation, DNS, egress, inspection, private endpoints, and inter-cloud connectivity |
| Regions and residency | Approved regions, sovereignty constraints, service availability, paired regions, and exception handling |
| Logging and security | Existing SIEM, log destinations, retention, encryption keys, Security Hub, Defender, SCC, Cloud Guard, and incident routing |
| Policy and compliance | Required controls, evidence standards, exceptions, approval roles, and regulatory mappings |
| Terraform and state | Backend ownership, encryption, locking, state separation, recovery, imports, and existing-resource adoption |
| Source control and CI | Repository ownership, branch rules, environment reviewers, runner policy, secret scanning, and alert routes |
| Naming and cost | Naming conventions, required business tags, billing hierarchy, budgets, chargeback, and orphan-resource handling |
| Operating model | Platform ownership, service requests, maintenance windows, support, upgrades, rollback authority, and handoff acceptance |

## Delivery boundary

A real customer receives a pinned release in a new customer-owned private
repository. Infinitech configures the agreed provider paths and controls with
customer-authorized access. The customer retains its repository, configuration,
state, logs, resources, and extensions according to the executed agreement.

This public repository demonstrates delivery discipline and evidence. It does
not include the reusable implementation or confer rights to deploy it.
