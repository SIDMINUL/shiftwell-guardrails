# Shiftwell Guardrails

**An interactive shift-swap decision simulator** created as a prototype for the Shiftwell Product Intern case study.

## Live demo

After enabling GitHub Pages, the prototype should be available at:

https://sidminul.github.io/shiftwell-guardrails/

## What it demonstrates

Shiftwell serves multi-location businesses with three roles interacting around staffing and shift swaps. This prototype illustrates a product direction focused on safe, compliant scheduling and fewer unnecessary manual approvals.

You can interactively test:
- **Certificate status:** expired required credentials block a proposed swap.
- **Role training:** a staff member who is not trained for the role is blocked.
- **Weekly hours:** projected hours above 48 trigger regional approval in this simplified example.
- **Approval authority:** a scenario can be routed to regional approval.

## Product rationale

The case study presents three customer requests: certificate expiry controls from CarePoint Clinics, overtime approval controls from UrbanMart, and WhatsApp shift-swap approvals from FreshBowl.

The recommended delivery baseline is the two well-estimated, higher-consequence capabilities:
1. CarePoint certificate eligibility guard (estimated 1 sprint).
2. UrbanMart overtime approval control (estimated 2 sprints).

The remaining capacity is reserved for discovery and a possible reusable swap-approval rules engine, conditional on engineering validating scope and effort. A WhatsApp integration is deferred while the team investigates the deeper approval bottleneck.

## How to use the demo

Open the live demo (or open `index.html` locally in a browser). Change the certificate status, weekly hours, training status, and approval policy. The decision panel updates immediately.

## Limitations

This is a static front-end prototype with sample, client-side logic. It is not connected to Shiftwell systems and does not create or send real approvals. The 48-hour threshold and decision rules are illustrative and must be validated against customer policy before a production implementation.

## Production considerations

A production system would require:
- Authoritative employee, schedule, training, and certificate data.
- Server-side rule evaluation with explicitly defined week boundaries and shift-overlap logic.
- Role-based access control and configurable approver routing.
- Audit logs, exception handling, monitoring, and automated edge-case tests.
- A pilot with baseline metrics such as time to decision, percentage approved within 24 hours, escalation rate, and incorrect-approval incidents.

## Run locally

No build tools or dependencies are required. Download or clone this repository and open `index.html`.

## AI assistance

AI assistance was used to help draft and refine the prototype and supporting product documentation. The logic and assumptions should be reviewed by the author. This demo is not a compliance guarantee.

---
*Prepared for a fictional product case study. Shiftwell and its customer names are fictional.*
