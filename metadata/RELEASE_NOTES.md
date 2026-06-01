# RELEASE_NOTES

## GAIA Public Evidence Package

### Release Status

This release is a public evidence package for GAIA — Global Governance Swarm.

It is intended to document observable behavior, public-safe API surfaces, and redacted evidence artifacts without exposing the private core.

### What this release includes

- `README.md`
- `LICENSE.md`
- `PRIVATE_ACCESS.md`
- `SECURITY.md`
- `docs/SYSTEM_OVERVIEW.md`
- `docs/PUBLIC_SCOPE.md`
- `docs/API_SURFACE.md`
- `docs/VERIFICATION.md`
- `evidence/screenshots/01_global_state.png`
- `evidence/screenshots/02_state_hash.png`
- `evidence/screenshots/03_message_send_request.png`
- `evidence/screenshots/04_message_send_response.png`
- `evidence/screenshots/07_agents_list_redacted.png`

### Public evidence focus

This package focuses on the following publicly observable properties:

- Shared governance state.
- Integrity anchoring through a published state hash.
- Controlled inter-agent messaging.
- Redacted public visibility of the swarm layer.
- Bounded autonomy.
- Traceability without private disclosure.

### What is intentionally excluded

The following are intentionally excluded from this public release:

- Full agent implementations.
- Internal architecture and orchestration logic.
- Weights, scoring logic, and routing algorithms.
- Internal metrics and optimization strategies.
- Recovery mechanisms and arbitration logic.
- Deployment infrastructure and topology.
- Proprietary runtime internals.
- Any unredacted trace or artifact that reveals the private core.

### Notes for reviewers

The screenshots and documents in this package are meant to be reviewed together. The public package should be interpreted as evidence of behavior, not disclosure of the full system.
