# Security Policy

## Supported Versions

This repository supports the latest published public evidence package only.

Older public releases may remain available for review, but only the latest published evidence package should be treated as the current reference.

## Reporting a Vulnerability

If you discover a security issue in the public evidence package, or a disclosure risk that exposes private internals, please report it privately to the copyright holder.

Please include:

- A short description of the issue
- The file or artifact involved
- Why you believe the issue affects confidentiality, integrity, or exposure boundaries
- Any reproduction steps that do not require private access

## What Counts as a Security Issue

A security issue includes, but is not limited to:

- Leakage of private agent names or roles that were intended to remain redacted
- Exposure of weights, scoring logic, or routing algorithms
- Exposure of orchestration, recovery, or arbitration internals
- Public artifacts that can be used to infer private system mechanics
- Broken redaction in screenshots, traces, manifests, or logs
- Incorrect checksums or manifests that undermine evidence integrity

## What Does Not Count as a Security Issue

Not every technical disagreement is a security issue.

Examples of non-security feedback:

- Requests for additional documentation
- Suggestions for better wording
- Questions about the public API surface
- Requests for more public evidence artifacts

Those can be discussed openly unless they reveal private internals.

## Disclosure Principle

The guiding principle is simple:

- Public evidence should remain public-safe.
- Private internals should remain private.
- Redaction should be used wherever disclosure would expose the private core.

## Contact

Contact the copyright holder directly for private security reporting or NDA-bound review.
