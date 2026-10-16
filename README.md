# Shiftwell Guardrails
### Shift-swap decision simulator | Product Intern Case Study

**[Open the live prototype →](https://sidminul.github.io/shiftwell-guardrails/)**

Shiftwell Guardrails is an interactive concept prototype showing how workforce scheduling software can automatically approve eligible swaps while blocking unsafe requests and escalating exceptions.

## Try the prototype

Select a customer scenario and test the decision logic:

- **FreshBowl — automatic swaps:** eligible swaps can be automatically approved in the demo when the configured checks pass. Conflicts or policy exceptions require review.
- **CarePoint Clinics — credential guard:** a swap is blocked when a required certificate has expired.
- **UrbanMart — overtime control:** a schedule taking an employee above 48 hours per week requires regional approval.
- **Shared eligibility checks:** training and availability are checked across scenarios.

The prototype uses sample inputs and client-side logic. It is not connected to Shiftwell systems, does not process real employee data, and does not create real approvals. Its rules are illustrative and require customer and engineering validation before production use.

## Product recommendation

The case study covers three customer needs:

| Customer | Proposed capability | Estimated effort from case brief |
|---|---|---:|
| CarePoint Clinics | Block swaps when mandatory certificates have expired | 1 sprint |
| UrbanMart | Route schedules exceeding 48 weekly hours to regional approval | 2 sprints |
| FreshBowl | Automatically approve eligible swaps and send exceptions for review | Not estimated in the brief |

The proposed initial commitments are CarePoint's certificate eligibility guard and UrbanMart's overtime approval control. The remaining three sprints are capacity for discovery and a possible reusable swap-approval rules engine, conditional on engineering validating scope and effort. FreshBowl's automatic-swap workflow should be explored as a reusable rules capability; the prototype does not imply that this work has already been committed or estimated.

## What a production version would need

Before release, Shiftwell would need validated customer policies, reliable schedule and credential data, server-side rule evaluation, appropriate approver permissions, auditable decisions, exception handling, and edge-case testing. Automatic approval should occur only when all mandatory checks pass.

A pilot should measure:
- Time from swap request to decision
- Percentage of requests decided within 24 hours
- Eligible swaps automatically approved
- Exceptions escalated for review
- Incorrect approvals, blocked attempts, and manager workload

## AI use and limitations

AI assistance was used to help draft and refine the prototype and supporting documentation. The author should review the assumptions and final claims. This is a concept demonstration, not a production compliance tool or a guarantee of regulatory compliance.

---

*Shiftwell and the customer names in this assignment are fictional. The 48-hour threshold is a simplified case-study assumption; actual customer policies, week boundaries, exceptions, and automatic-approval criteria would need to be confirmed.*
