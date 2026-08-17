# Acceptance evidence

## Evidence-production scenarios

The evidence builder executes these scenarios against the private product
revision recorded in `PROVENANCE.json`:

1. Validate one synthetic request for each of AWS, Azure, Google Cloud, and OCI.
2. Render the same inputs twice and require byte-identical generated roots.
3. Check Terraform formatting for every published root.
4. Evaluate a passing plan fixture with zero policy violations.
5. Evaluate an intentionally unsafe plan fixture and require one or more
   actionable violations.
6. Reject prohibited implementation paths and executable capabilities across
   the complete exported tree.
7. Scan the complete exported tree for secrets.
8. Generate and immediately verify the canonical checksum manifest.

Machine-readable results are in `validation.json`,
`publication-boundary.json`, and `examples/policy-results/`.

## Retained product demonstration

The canonical walkthrough records the following point-in-time evidence:

| Scenario | Recorded result | Limitation |
|---|---|---|
| Intentional prevention | Unsafe plan rejected before cloud writes; corrected plan passed the same policy package | Demonstrates the retained scenario, not every possible unsafe change |
| Protected execution | Saved-plan checksum and authorized execute boundary were correlated | Does not claim mandatory two-person separation of duties |
| Provider proof | Sanitized console evidence connected governed resources across four providers | Identifiers are masked and evidence is time-bound |
| Tag evidence | 26 selected resources showed 26/26 required business tags in the retained execute evidence | Not a universal compliance percentage |
| Lifecycle | Five four-cloud workload cycles completed and disposable state returned to empty | Not an SLA or reliability percentage |
| Drift | Nightly refresh-only planning produced evidence-routed follow-up | Remediation remains reviewed, not automatic |
| Cost | Complete provider-settled cost is unavailable | No zero-cost or savings claim is made |

The public artifact is evidence of implemented behavior and delivery discipline.
It is not a certification, authorization, audit opinion, customer reference, or
guarantee of regulatory outcome.
