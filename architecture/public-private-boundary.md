# Public / Private Repository Boundary

## Purpose

This document defines the publication boundary for the public AI portfolio.

The public repository is a **showroom**, not the production source of truth.

## Public Repository

Appropriate public artifacts include:

- Sanitized bot specifications
- Older or simplified portfolio snapshots
- Evaluation designs with clearly labeled evidence types
- Original instructional materials intended for public review
- Architecture diagrams that do not expose private infrastructure
- General governance patterns
- Redacted examples and case studies

## Private Repository

Keep private:

- Current production instruction sets when public disclosure is unnecessary
- Organization-specific procedures, URLs, identities, or internal schedules
- Personal background not needed for the portfolio
- Credentials, tokens, secrets, recovery information, or account identifiers
- Student or employee records
- Restricted assessment content and answer keys
- Internal logs, incident records, or security-sensitive implementation details
- Draft changes that have not passed publication review

## Publication Decision

Before moving an artifact from private development to the public portfolio, ask:

1. What skill does this artifact need to demonstrate?
2. What minimum detail proves that skill?
3. What details identify people, organizations, systems, or live operations?
4. What could be copied or abused if published?
5. Is third-party material being exposed?
6. Does the artifact reveal more of the current implementation than the portfolio requires?
7. Are test results labeled accurately as simulated, dry-run, or runtime?

Prefer the **minimum sufficient public artifact**.

## History Warning

Deleting a sensitive file from the current branch does not remove it from Git history. If a secret or materially sensitive artifact is committed publicly, treat it as exposed and use an appropriate history-removal and credential-rotation process when necessary.
