# Shiftwell Guardrails
### Shift-swap decision simulator | Product Intern Case Study

**[Open the live prototype →](https://sidminul.github.io/shiftwell-guardrails/)**

Shiftwell Guardrails is an interactive concept prototype exploring how workforce scheduling software can make shift swaps safer while reducing avoidable manual approvals.

## Try the prototype

Change the inputs in the demo to see how the illustrative decision changes:

- **Certificate validity:** an expired required certificate blocks the swap.
- **Role training:** an employee who is not trained for the role is blocked.
- **Projected weekly hours:** exceeding 48 hours triggers regional approval in this simplified scenario.
- **Approval authority:** review how the request is routed for approval.

The prototype uses sample inputs and client-side logic. It is not connected to Shiftwell systems, does not process real employee data, and does not create real approvals.

## Product recommendation

The case study covers three customer requests:

- **CarePoint Clinics:** prevent shifts or swaps when mandatory credentials have expired.
- **UrbanMart:** require regional approval when a schedule takes an employee above 48 hours per week.
- **FreshBowl:** support shift-swap requests and approvals through WhatsApp.

The recommended first commitments are the two scoped features with supplied engineering estimates and clear customer consequences:

| Proposed work | Estimated effort |
|---|---:|
| CarePoint certificate eligibility guard | 1 sprint |
| UrbanMart overtime approval control | 2 sprints |

The remaining three sprints are capacity for discovery and a possible reusable swap-approval rules engine, only if engineering validates its scope and estimate. WhatsApp integration is deferred while the team investigates whether slow manual approvals—not the messaging channel alone—are the main bottleneck.

## What a production version would need

Before release, Shiftwell would need validated customer policies, reliable schedule and credential data, server-side rule evaluation, appropriate approver permissions, auditable decisions, exception handling, and edge-case testing.

A pilot should measure:
- Time from swap request to decision
- Percentage of requests decided within 24 hours
- Escalation rates and approval workload
- Incorrect approvals and blocked attempts

## AI use and limitations

AI assistance was used to help draft and refine the prototype and supporting documentation. The author should review the assumptions and final claims. This is a concept demonstration, not a production compliance tool or a guarantee of regulatory compliance.

---

*Shiftwell and the customer names in this assignment are fictional. The 48-hour threshold is a simplified case-study assumption; actual customer policy, including week boundaries and exceptions, would need to be confirmed.*
