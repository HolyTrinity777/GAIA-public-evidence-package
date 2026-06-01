# PUBLIC_SCOPE

This repository contains the **public evidence package** for GAIA — Global Governance Swarm.

The purpose of this document is to define what is publicly disclosed, what is redacted, and what remains private.

## Publicly included

The following materials are part of the public release:

- Public README and system documentation.
- Screenshots of live API behavior.
- Redacted traces and response samples.
- Verification artifacts and checksum outputs.
- Public endpoint examples.
- Evidence manifests and release notes.

## Publicly declared behavior

The public package is intended to show the following observable properties:

- Shared governance state.
- Controlled state mutation through validated paths.
- Traceable inter-agent messaging.
- Auditable state integrity.
- Bounded autonomy of swarm agents.
- Redacted proof of operation.

## Public API surface

The following endpoint classes are considered public for evidence purposes:

- `GET /global_state`
- `POST /global_state`
- `GET /system/state_hash`
- `GET /agents`
- `GET /agents/{agent_name}` where disclosure is safe
- `GET /agents/{agent_name}/logs` where disclosure is safe and redacted
- `POST /messages/send`

## Public evidence artifacts

The canonical public evidence set includes:

- `01_global_state.png`
- `02_state_hash.png`
- `03_message_send_request.png`
- `04_message_send_response.png`
- `07_agents_list_redacted.png`

These artifacts are intended to demonstrate the observable behavior of the system without revealing private implementation.

## Excluded from public release

The following remain private and are not included in the public package:

- Internal architecture.
- Full agent implementations.
- Weights and model-specific internals.
- Scoring logic and algorithms.
- Internal metrics and optimization strategies.
- Orchestration systems and recovery mechanisms.
- Arbitration logic.
- Deployment infrastructure.
- Proprietary runtime internals.

## NDA boundary

Access to excluded materials is available only under NDA or separate written agreement. The public package is intentionally limited to evidence of behavior, not disclosure of the private core.

## Privacy rule

If a file, screenshot, trace, or example risks exposing the private core, it should be redacted or omitted.
