# Directive: NOTICES-STATE-001

> **Status:** Completed historical directive. Do not re-execute it. Read
> `AGENT_STATE.json` and wait for a newly assigned directive before changing
> this repository.

## Main Objective
Establish `attendance-crmt-development-notices` as a visible coordination participant and prepare the public documentation/notices required for future Attendance Teams bot publication, without claiming that the real attendance integration is enabled.

## Key Context From Other Repositories

- `attendance-crmt` is `ready` and exports MCP Streamable HTTP over HTTPS at `/mcp`, contract 1.2.0, including requester-scoped `list_my_attendance_events`. Its real Teams end-to-end path is blocked by Entra registrations, OBO consent/certificate configuration, a deployed non-production HTTPS endpoint, and a production active-email uniqueness check.
- `attendance-teams-bot` is `ready` and exports a requester-scoped personal-chat read-only attendance flow compatible with CRMT contract 1.2.0. It declares real attendance traffic disabled until the deployed CRMT endpoint and the Entra/OBO prerequisites are configured and verified.
- This repository currently has no `AGENT_STATE.json`; its status, exports, dependencies, and blockers are therefore unknown to the master coordinator.

## Specific Steps

1. Inspect this repository's existing documents and publishing requirements to identify its owned public notices and publication artifacts for the Attendance Teams bot.
2. Create a concise `AGENT_STATE.json` at the repository root that truthfully declares repository status, published document/notices exports, dependencies on the bot/CRMT, and all open blockers. Do not invent completed notices or external approvals.
3. Produce or update the owned public documentation necessary to describe the bot's current read-only scope, responsible system boundaries, user-facing privacy/security expectations, and any publication prerequisites actually required by the chosen distribution channel.
4. Clearly distinguish implemented-but-disabled client/server capability from an enabled production service. Do not publish endpoint URLs, token details, employee data, secrets, or unsupported availability claims.
5. Validate the documentation links/content using the repository's relevant checks, then document any required human, Entra, deployment, marketplace, or legal approvals as explicit blockers rather than treating them as completed.

## Definition Of Done

- A valid root `AGENT_STATE.json` gives the coordinator a truthful status contract for this repository.
- The repository exposes a documented public-notices/publication-artifact inventory and its relationship to the current read-only Teams bot scope.
- Documentation does not imply real Teams attendance traffic is live or bypass the CRMT authorization/audit boundary.
- Relevant repository documentation validation checks pass.
- All remaining external approvals, deployment prerequisites, and missing inputs are named as blockers.

## Required `AGENT_STATE.json` Update

After completion, ensure `AGENT_STATE.json` contains:

- `repo_name`: `attendance-crmt-development-notices`;
- `status`: the actual resulting status;
- `provided_exports.interfaces_or_endpoints`: concrete published notices/documents or other public artifacts, with versions/locations where applicable;
- `dependencies_needed`: precise inputs or approvals still required from `attendance-crmt`, `attendance-teams-bot`, Entra/deployment, or the publishing channel;
- `open_issues_or_blockers`: every unresolved publication or integration blocker, or an empty list only if none remain.

## [COMPLETED] NOTICES-STATE-001

The public development notice inventory, staged privacy/terms scope, and repository
coordination state are locally verified. Real attendance traffic and external
publication readiness remain blocked by the dependencies declared in
`AGENT_STATE.json`.
