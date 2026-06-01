# API_SURFACE

This document describes the public-facing API surface that is available for evidence and review in the GAIA public package.

The API is intentionally limited to observable governance behavior. It is not a disclosure of internal architecture, private orchestration logic, or proprietary swarm implementation.

## Public endpoint groups

### 1. State

#### GET `/global_state`
Returns the current shared GAIA state object.

Purpose:
- Show the live governance state.
- Provide a public view of system-level metrics.
- Support evidence of controlled shared-state management.

#### POST `/global_state`
Updates a single key in the GAIA state, subject to validation.

Purpose:
- Demonstrate bounded and controlled mutation.
- Show that state changes occur through governed paths rather than ad-hoc edits.

### 2. Integrity

#### GET `/system/state_hash`
Returns a hash of the serialized GAIA state for integrity checks.

Purpose:
- Anchor public state snapshots.
- Allow independent verification that a published state has not been silently altered.

### 3. Agents

#### GET `/agents`
Returns a list of agents with public-safe fields such as name, role, and active status.

Purpose:
- Demonstrate the existence of the swarm.
- Show that multiple coordinated agents are present.
- Provide a bounded public inventory of the agent layer.

#### GET `/agents/{agent_name}`
Returns agent detail where disclosure is safe.

Purpose:
- Show agent-level state in a controlled manner.
- Provide traceable agent context without exposing private internals.

#### GET `/agents/{agent_name}/logs`
Returns redacted logs where disclosure is safe.

Purpose:
- Show traceability of agent behavior.
- Support audit review.
- Preserve privacy by omitting sensitive implementation details.

### 4. Messaging and governance actions

#### POST `/messages/send`
Routes a message from one agent to another and may apply bounded state deltas under predefined governance rules.

Purpose:
- Demonstrate controlled inter-agent communication.
- Show that the swarm can coordinate through message-based governance.
- Prove that message handling is auditable and bounded.

## Public API principles

- **Bounded disclosure** — only the behavior necessary to understand the public evidence is exposed.
- **Traceability** — meaningful actions should leave an auditable footprint.
- **Controlled mutation** — state updates must follow governed paths.
- **Silence is valid** — absence of a signal may be the correct outcome.
- **Privacy by design** — internal implementation details are excluded from this surface.

## What is not part of this surface

The following are intentionally excluded:

- Private routing logic.
- Full agent implementations.
- Weights and scoring internals.
- Arbitration and recovery logic.
- Internal metrics and optimization strategies.
- Deployment topology.
- Any implementation detail that would reveal the private core.

## Screenshot mapping

The following screenshots correspond to this API surface:

- `01_global_state.png` → `GET /global_state`
- `02_state_hash.png` → `GET /system/state_hash`
- `03_message_send_request.png` → `POST /messages/send` request body
- `04_message_send_response.png` → `POST /messages/send` response
- `07_agents_list_redacted.png` → `GET /agents`

## Review standard

A reviewer should be able to inspect this surface and confirm:

1. The system has a live shared state.
2. The state can be integrity-anchored.
3. The swarm has multiple agents.
4. Messages can be sent in a bounded way.
5. The public package does not reveal the private core.
