# Shiftwell Guardrails
### A shift-swap decision simulator | Product Intern Case Study

Shiftwell Guardrails is an interactive prototype exploring how workforce scheduling software can make shift swaps safer and reduce avoidable manual approvals.

## Prototype

**Live demo:** https://sidminul.github.io/shiftwell-guardrails/

The demo lets you change four inputs and see the resulting illustrative decision:
- **Certificate validity:** expired required credentials block the swap.
- **Role training:** swaps involving an untrained employee are blocked.
- **Projected weekly hours:** more than 48 hours triggers regional approval in this simplified scenario.
- **Approval authority:** the scenario can be routed to a regional approver.

> The demo uses sample inputs and client-side logic. It is not connected to Shiftwell systems and does not process real employee data or approvals. The live link should be used only after GitHub Pages deployment has been verified.

## Product thinking behind the prototype

The case study presents three customer requests:
- **CarePoint Clinics:** prevent scheduling or swaps when mandatory certificates have expired.
- **UrbanMart:** require regional approval when a schedule takes an employee beyond 48 hours per week.
- **FreshBowl:** enable shift-swap requests and approvals through WhatsApp.

The recommendation is to commit first to the two features with supplied engineering estimates and clear consequences:
1. **CarePoint certificate eligibility guard — 1 sprint.**
2. **UrbanMart overtime approval control — 2 sprints.**

The remaining three sprints are capacity for discovery and a possible reusable swap-approval rules engine, conditional on engineering validating the scope and estimate. WhatsApp integration is deferred while the team investigates whether slow manual approvals—not the messaging channel alone—are the main bottleneck.

## What a production version would need

Before release, Shiftwell would need validated customer policies, reliable schedule and credential data, server-side rule evaluation, appropriate approver permissions, auditable decisions, exception handling, and testing of edge cases. A pilot should measure decision time, the percentage of swaps decided within 24 hours, escalation rates, and incorrect approvals.

## AI use and limitations

AI assistance was used to help draft and refine the prototype and supporting documentation. The rules and assumptions must be reviewed by the author. This is a concept demonstration, not a production compliance tool or a guarantee of regulatory compliance.

---

*Shiftwell and the customer names in this assignment are fictional. The 48-hour rule is shown as a simplified case-study assumption; actual customer policy would need to be confirmed.*
