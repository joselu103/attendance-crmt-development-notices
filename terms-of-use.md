# Attendance CRMT Development Bot Terms of Use

**Effective date:** 2026-08-31

## Development-Only Service and Current Status

Attendance CRMT (Development) is a development-only Microsoft Teams bot. It is
provided to validate Microsoft Teams, Azure Bot Service, and bot-hosting
connectivity. It is not approved for production attendance management.

The currently enabled behavior is connectivity-only. A personal-chat,
requester-scoped, read-only attendance path is implemented but disabled. It must
remain disabled until every activation prerequisite in these terms and the public
notices inventory is configured and verified.

## Permitted Read-Only Scope

If the disabled path is activated, an authenticated user may request only their
own attendance in a bounded date range in a personal chat. The path is read-only.
It does not create, update, approve, or otherwise manage attendance records.

It does not permit requests for another employee's data, group, meeting, or
channel use, or attendance-related business or employment decisions. Attendance
output is informational and must not be treated as an employment record,
authorization, or business decision.

## Identity and Authority

Attendance CRMT remains the authoritative boundary for verified requester identity,
employee mapping, authorization, audit, attendance business rules, and SQL Server
access. The bot does not connect directly to SQL Server or recreate those rules.

A supplied employee identifier, Teams activity field, user statement, or LLM
output is not authority for employee identity or authorization. Attendance CRMT
must derive the employee mapping, authorize the requester-scoped tool, and record
the audit outcome.

## Acceptable Use and Prohibited Inputs

Use the bot only with an authorized development account and only for permitted
development testing. Do not submit credentials, access tokens, employee data,
attendance information, or other unnecessary sensitive or personal information.

Do not impersonate another person, attempt to bypass Attendance CRMT authorization,
or attempt to provide an authoritative employee identity through chat content or
tool input.

## Availability and Non-Production Status

The bot may be changed, restarted, disabled, or removed without notice. It is
provided as-is for development testing and may return incomplete, fixed, or
non-authoritative responses.

Implementation readiness is not production activation, end-to-end verification,
or AppSource/Commercial Marketplace approval. No production availability is
promised.

## Activation Prerequisites

Real attendance traffic remains disabled until a deployed non-production HTTPS
Attendance CRMT MCP endpoint, the required Microsoft Entra API registration,
delegated on-behalf-of consent and certificate configuration, and end-to-end
identity, authorization, audit, and safe-error verification are complete.

Production rollout also remains blocked pending the authoritative SQL Server
active-email uniqueness readiness check. Publication readiness remains blocked
until the organization confirms the internal custom-app distribution channel,
approves a monitored support/privacy contact, and completes any required privacy,
legal, human-resources, and Teams-administrator reviews.

## Changes and Contact

These terms may change as the development bot gains functionality. Questions about
this development bot or these terms should be directed to the Attendance CRMT
project maintainer until an approved monitored support/privacy contact is
published.
