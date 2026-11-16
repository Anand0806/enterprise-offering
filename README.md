# Enterprise Offering prototype

Clickable end-to-end prototype for the **Enterprise Offering BRD (v1.0, Oct 12, 2026)**. Brands onboard enterprise clients in Reach Central. Enterprises manage employee lines in Enterprise Central. Employees' family members link their own accounts as associates to get discounted plans.

## Open it

Open `prototype/index.html` in any browser. It's one self-contained file with no build step and no server.

The private, shareable version is the Claude artifact: https://claude.ai/artifact/5ubKAdCbAa3qV4SUiKq34H

## What's covered

| View | Screens |
| --- | --- |
| Reach Central home | Welcome hero, action search, Main menu, Marketing (with **Enterprise onboarding**), Operations, Customer support |
| Reach Central · Brand | Enterprise customers, onboarding form, enterprise detail, block or reactivate, Existing customers (with account type and enterprise names), payment verification, enterprise account status report |
| Enterprise Central | Overview, employees (single add, CSV bulk upload, filters, bulk actions), plan changes at next MRC or immediate with differential, VAS, deactivation now or scheduled, associates, MID management, billing and payments, settings, users and roles, audit log |
| Subscriber app | Associate self-linking with a 10-minute OTP, plan comparison, checkout with card on file, delinking |
| Email outbox | Every notification in the BRD, rendered |

Demo data is fictional and stored in the viewer's browser. **Reset demo data** restores it. Payments, bank verification and emails are simulated.

## Assumptions to confirm

1. **Credit limit sign.** The BRD says `credit_limit ≤ 0`. The prototype uses a positive limit and puts the account on Hold when AR minus credit is over it.
2. **Permission modules.** M1 = subscriber and MID management, M2 = billing and payments, M3 = enterprise settings.
3. **Differential amount.** Credit for the unused days of the old plan, then the full charge for the new cycle.
4. **Hold behavior.** New employee accounts are blocked while an enterprise is on Hold.
5. **Bulk upload format.** CSV in the prototype. The BRD says Excel.
6. **Reach-to-brand bill cycle.** Still to be decided with FinOps, so not modeled.
