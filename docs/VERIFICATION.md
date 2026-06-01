# VERIFICATION

This document explains how a reviewer can verify the GAIA public evidence package without access to private internals.

The goal is not to reproduce the full system. The goal is to confirm that the evidence is internally consistent, that the screenshots correspond to the declared API surface, and that the public artifacts support the stated behavior.

## What can be verified

A reviewer can verify the following:

- The repository contains a public evidence package.
- The screenshots correspond to documented endpoints.
- The state hash is presented as an integrity anchor.
- The agent list shows a live swarm surface.
- Message send behavior is visible and bounded.
- The package does not disclose the private core.

## Verification workflow

### Step 1 — Confirm repository shape

Check that the repository includes the expected public structure:

- `README.md`
- `LICENSE.md`
- `PRIVATE_ACCESS.md`
- `SECURITY.md`
- `docs/`
- `evidence/`
- `verification/`
- `metadata/`

The presence of these directories and files shows that the release is organized as an evidence package rather than a raw implementation dump.

### Step 2 — Inspect the public README

Verify that the README states:

- GAIA is a bounded multi-agent governance coordination system.
- The repository is a public evidence package.
- Core orchestration and private internals remain NDA-only.
- Silence is a valid output.

### Step 3 — Match screenshots to endpoints

Confirm that each screenshot maps to the declared API surface:

- `01_global_state.png` → `GET /global_state`
- `02_state_hash.png` → `GET /system/state_hash`
- `03_message_send_request.png` → `POST /messages/send` request body
- `04_message_send_response.png` → `POST /messages/send` response
- `07_agents_list_redacted.png` → `GET /agents`

### Step 4 — Check redaction discipline

Ensure that screenshots, traces, and examples do not expose:

- Full private agent names if those are considered sensitive.
- Weights or scoring logic.
- Internal orchestration or recovery mechanisms.
- Internal metrics that reveal the private core.

### Step 5 — Inspect state integrity evidence

Review `02_state_hash.png` and any accompanying checksum or manifest files.

The reviewer should be able to confirm:

- A state hash is being published.
- The hash is tied to a timestamped snapshot.
- The evidence package treats integrity as a public review target.

### Step 6 — Review the message flow

Inspect the request and response screenshots for `POST /messages/send`.

The reviewer should confirm:

- The message payload is simple and public-safe.
- The response shows success and a message identifier.
- The message exchange is bounded and traceable.

### Step 7 — Review the agent list

Inspect `07_agents_list_redacted.png`.

The reviewer should confirm:

- Multiple agents exist.
- Their active status is visible.
- Any sensitive names are redacted or replaced with public-safe labels.

## Suggested lightweight verification script

If you include a script in `verification/`, it should do only public-safe checks such as:

- Validate that required files exist.
- Confirm that screenshot filenames match the manifest.
- Confirm that checksum entries match published files.
- Confirm that the README and scope documents reference the same package language.

It should **not** attempt to reconstruct the private system.

## Verification outputs worth including

Useful public verification outputs include:

- `EVIDENCE_MANIFEST.json`
- `CHECKSUMS.txt`
- A short script output showing file presence checks.
- A short script output showing checksum verification success.

## What verification is not

Verification is not:

- Source disclosure.
- Full system replay.
- Reverse engineering.
- Access to private orchestration.
- Access to internal weights, algorithms, or routing logic.

## Review standard

The package is considered publicly verifiable if a reviewer can confirm:

1. The screenshots match the documented endpoints.
2. The artifacts are internally consistent.
3. The private core is not exposed.
4. The package clearly separates evidence from implementation.
5. The public claim is supported by visible behavior.
