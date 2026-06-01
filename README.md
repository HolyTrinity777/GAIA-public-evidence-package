# GAIA — Public Evidence Package

GAIA — Global Governance Swarm — is a bounded multi-agent governance coordination system. It provides a single audited surface for shared state, inter-agent messaging, traceable decisions, and controlled state mutation.

This repository is the **public evidence package** for GAIA. It contains observable behavior, redacted traces, screenshots, and verification artifacts. Core orchestration, proprietary agents, internal algorithms, weights, and private metrics remain private and are available only under NDA or separate written agreement.

## What GAIA is for

GAIA is designed to support governance workflows by:

- Coordinating autonomous archetype agents that maintain and mutate system-level metrics.
- Providing a single API surface to query state, audit decisions, send messages, and observe system dynamics over time.
- Enforcing governance primitives such as transparency, traceability, conflict resolution, and controlled state mutation.

**Silence is a valid output.** If agents do not produce a specific class of signal, the correct consensus can be 0%.

## What this public release contains

This package exposes the **observable** layer of the system, not the private implementation.

Included in this release:

- Public documentation describing the system and its boundaries.
- Screenshots of live API behavior.
- Redacted traces and response samples.
- Verification artifacts for state integrity and auditability.
- Public endpoint examples showing the governance surface.

## Publicly declared properties

GAIA is built to demonstrate the following observable properties:

- Shared governance state.
- Controlled state mutation.
- Traceable inter-agent messaging.
- Auditable state integrity.
- Bounded autonomy.
- Redacted public proof of operation.

## Public API surface

The main public governance endpoints are:

- `GET /global_state` — returns the current GAIA global state object.
- `POST /global_state` — updates a single key in GAIA state, subject to validation.
- `GET /system/state_hash` — returns a hash of serialized GAIA state for integrity checks.
- `GET /agents` — lists agents by name, role, and active status.
- `GET /agents/{agent_name}` — returns agent detail, where safe to disclose.
- `GET /agents/{agent_name}/logs` — returns redacted audit logs, where safe to disclose.
- `POST /messages/send` — routes a message between agents and may apply bounded state deltas under governance rules.

## Evidence set

This public release is supported by the following screenshots:

- `01_global_state.png`
- `02_state_hash.png`
- `03_message_send_request.png`
- `04_message_send_response.png`
- `07_agents_list_redacted.png`

These show the live state, integrity anchoring, bounded messaging, and active agent surface without exposing private internals.

## Optional utilities

Any market-like endpoints in this repository are optional utilities or simulation surfaces unless explicitly connected to real execution. They are not the core mission of GAIA and should not be treated as authoritative for governance integrity.

## Private boundary

The following remain private and are intentionally excluded from this public package:
•	Internal architecture.
•	Full agent implementations.
•	Scoring logic and routing rules.
•	Internal metrics and optimization strategies.
•	Orchestration systems.
•	Recovery mechanisms.
•	Arbitration logic.
•	Deployment infrastructure.
•	Proprietary runtime internals.
Access to those components is available only under NDA or separate written agreement.

## Verification

The public package is designed so a reviewer can inspect the evidence directly:

- Confirm state integrity through the state hash artifact.
- Inspect redacted screenshots and traces.
- Review public endpoint examples.
- Validate that the public evidence is internally consistent.

## Status

This is a public evidence package, not a full open-source release. The goal is to make observable behavior verifiable while keeping the private core protected.
