# Attendance CRMT Development Notices

Public development notices for the Attendance Teams bot integration.

## Current Publication Status

The currently enabled bot behavior is connectivity-only and is not a production
attendance service. A requester-scoped, personal-chat, read-only attendance path
compatible with Attendance CRMT MCP contract 1.2.0 is implemented but disabled.
Real attendance traffic must remain disabled until every activation prerequisite
below is configured and verified.

## Published Artifacts

- [Privacy notice](privacy-policy.md)
- [Terms of use](terms-of-use.md)

Canonical manifest URLs:

- Privacy: `https://github.com/joselu103/attendance-crmt-development-notices/blob/main/privacy-policy.md`
- Terms: `https://github.com/joselu103/attendance-crmt-development-notices/blob/main/terms-of-use.md`
- Website/support entry point: `https://github.com/joselu103/attendance-crmt-development-notices`

## System Responsibilities

The Teams bot owns Teams interaction, LLM orchestration, authenticated MCP client
behavior, and safe rendering. Attendance CRMT remains the authoritative boundary
for verified requester identity, employee mapping, authorization, audit,
attendance business rules, and SQL Server access. The bot never selects an
authoritative employee ID or connects directly to SQL Server.

## Activation Prerequisites

- Deployed non-production HTTPS Attendance CRMT `/mcp` endpoint, contract 1.2.0.
- Attendance CRMT Entra API registration and `attendance.access` scope.
- Approved delegated OBO consent and production certificate configuration.
- End-to-end identity, authorization, audit, and safe-error verification.
- Production active-email uniqueness readiness check before production rollout.
- Confirmed internal custom-app distribution, monitored contact, and required
  organizational legal/privacy/HR/Teams-admin approvals.

## Distribution Boundary

These artifacts are prepared for an organization-internal Microsoft Teams custom
app. They do not claim AppSource/Commercial Marketplace approval or production
availability.

## Contact

Questions should be directed to the Attendance CRMT project maintainer until an
approved monitored support/privacy contact is published.
