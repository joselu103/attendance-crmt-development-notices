# Attendance CRMT Development Bot Privacy Notice

**Effective date:** 2026-08-31

## Purpose, Status, and Scope

Attendance CRMT (Development) is a development-only Microsoft Teams bot. It is
not a production attendance service.

The currently enabled bot behavior is limited to Microsoft Teams-to-bot
connectivity. A personal-chat, requester-scoped, read-only attendance path is
implemented but disabled. It must remain disabled until the activation
prerequisites described below are configured and verified.

## Information Processed by the Current Connectivity Path

When a user sends a message to the bot, Microsoft Teams and Microsoft Bot Service
may send the message activity and technical metadata needed to route and respond
to that activity. This can include message content, conversation identifiers,
user identifiers supplied by the Microsoft platform, timestamps, and request
metadata.

The application does not intentionally persist message content, employee data, or
attendance data for the currently enabled connectivity behavior. Microsoft, Azure,
and any organization operating Microsoft Teams may process data under their own
applicable agreements, policies, and service configuration.

## Information Processed Only if Read-Only Attendance Is Activated

If the disabled attendance path is activated after all prerequisites are verified,
the bot would process a user's message and bounded date-range request, authenticated
Microsoft identity context, and requester-scoped attendance results returned by
Attendance CRMT. LLM orchestration would use the message to select the permitted
requester-scoped tool and would treat Attendance CRMT responses as data, not
instructions.

This conditional path is read-only and is not currently enabled. This notice does
not make retention, deletion-period, encryption, processing-region, model-provider,
or subprocessor claims for that future path until those facts are approved and
published.

## Identity, Authorization, and Attendance Data Boundary

Attendance CRMT is the authoritative boundary for verified requester identity,
employee mapping, authorization, audit, attendance business rules, and SQL Server
access. The bot does not select an authoritative employee identity or connect
directly to SQL Server.

A Teams activity field, user-provided employee identifier, user statement, or LLM
output is not authority for employee identity or authorization. Attendance CRMT
must validate the identity context, derive the employee mapping, authorize and
audit the requester-scoped tool, apply attendance rules, and access attendance
data.

## Security and Data-Minimization Expectations

Do not send credentials, access tokens, employee identifiers, attendance records,
or other unnecessary sensitive or personal information to this development bot.
The bot must not expose access tokens, secrets, internal identifiers, stack traces,
connection details, or other internal diagnostics in user-visible responses.

## Activation and Publication Prerequisites

Real attendance traffic remains disabled until a deployed non-production HTTPS
Attendance CRMT MCP endpoint, the required Microsoft Entra API registration,
delegated on-behalf-of consent and certificate configuration, and end-to-end
identity, authorization, audit, and safe-error verification are complete.

Production rollout also remains blocked pending the authoritative SQL Server
active-email uniqueness readiness check. Publication of this notice set requires
an approved monitored support/privacy contact and any required organizational
privacy, legal, human-resources, and Teams-administrator reviews.

## Changes and Contact

This notice may change as the development bot gains functionality. Questions about
this development bot or this notice should be directed to the Attendance CRMT
project maintainer until an approved monitored support/privacy contact is
published.
