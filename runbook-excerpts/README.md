# Operational reasoning excerpts

These excerpts demonstrate the operating model without publishing executable
runbooks or automation.

## Failed preparation or policy rejection

- Treat the result as a blocked proposal; do not bypass or weaken the rule.
- Correlate the violation with its Terraform address and mapped source location.
- Correct the request or implementation, create a new plan, and evaluate it
  through the same policy package.
- Preserve the failed result as prevention evidence when the scenario was an
  intentional control exercise.

## Control changes

- Add or change a control together with passing and failing scenarios.
- Require complete policy test coverage before promotion.
- Re-evaluate representative plans for all affected providers.
- Record exceptions explicitly with an owner, scope, reason, and expiry; do not
  turn temporary exceptions into silent defaults.

## Identity rotation

- Rotate plan and execution identities independently.
- Validate the new trust subject before retiring the previous identity.
- Preserve a time-bounded overlap only when rollback requires it.
- Confirm that no standing provider keys or customer credentials remain after
  handoff.

## Rollback and recovery

- Stop at the provider boundary that failed; do not assume a cross-cloud
  transaction.
- Compare the saved plan, execution evidence, and actual state before choosing
  rollback, forward repair, or import.
- Run provider-local cleanup and verify state rather than inferring success from
  a workflow conclusion alone.
- Escalate any non-empty disposable state or unexpected persistent-resource
  change for reviewed recovery.

The complete customer runbook and automation are delivered only in a scoped,
customer-owned private repository.
