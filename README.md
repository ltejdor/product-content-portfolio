# Product content portfolio · Lucía Tejeda Dorado

I'm a technical writer who works at the intersection of documentation and product marketing. In my current role, leading documentation at a B2B SaaS company for banks, I write the docs, present product webinars to clients, and write product documentation that helps customers get full value from the software and supports upselling.

This repository shows that side of my work.

> **Two readers, one product.** The [technical writing portfolio](https://github.com/ltejdor/technical-writing-portfolio) documents Relay, a fictional notification platform for banks, for developers and support teams. This repository covers **the same features** for the people who decide, buy and measure: heads of digital banking, operations, customer service and compliance.

## The same feature, two jobs

Every piece here has a technical counterpart. Same facts, different reader, different job:

| Business content (this repo) | Reader | Job | Technical counterpart |
|---|---|---|---|
| [One integration for every message your customers can't miss](solution-brief/relay-for-digital-banking.md) | CTOs, heads of digital banking | Show why Relay is worth evaluating, and how small the integration is | [API reference](https://github.com/ltejdor/technical-writing-portfolio/tree/main/api-reference) |
| [Know what happened to every notification, as it happens](feature-page/delivery-visibility.md) | Heads of digital channels, operations | Turn a developer feature into a business benefit, and open the door to an add-on | [Webhooks guide](https://github.com/ltejdor/technical-writing-portfolio/tree/main/webhooks) |
| [What's new in Relay 2026.1](announcement/whats-new-2026-1.md) | Business contacts at client banks | Make a release, including a breaking change, feel like progress | [Release notes](https://github.com/ltejdor/technical-writing-portfolio/blob/main/release-notes/relay-2026.1.md) and [migration guide](https://github.com/ltejdor/technical-writing-portfolio/blob/main/release-notes/migration-2026.1.md) |
| [Mandatory, service or marketing? A practical guide to notification compliance](guide/notification-compliance-guide.md) | Product owners, compliance | Help with a real problem first, build trust, and show where the product fits | [Notification categories](https://github.com/ltejdor/technical-writing-portfolio/blob/main/concepts/notification-categories.md) |
| [Fewer "my OTP never arrived" calls](playbook/otp-support-calls.md) | Heads of customer service | Connect a support problem to a business outcome, and to the add-ons that solve it | [OTP troubleshooting](https://github.com/ltejdor/technical-writing-portfolio/blob/main/troubleshooting/otp-not-received.md) |

## How documentation drives upsell

Relay has a base plan and two add-ons:

| Plan | What it adds |
|---|---|
| **Relay Core** | One API for push, SMS and email, notification categories, consent checks, webhooks and delivery history. |
| **Smart Fallback** | Automatic fallback between channels, per notification type. |
| **Delivery Insights** | Dashboards on delivery, fallback and channel cost, and alerts when a mandatory notification fails. |

Upsell through documentation isn't a sales pitch inside the docs. It's documentation that helps customers use what they have well enough to notice what's missing. Each piece follows the same path:

1. **Start from the reader's problem**, in their words: missing OTPs, unclear reports, compliance risk.
2. **Solve as much as possible with what they already have.** The OTP playbook's first stage only needs Relay Core.
3. **Show the next step where it naturally appears.** When a reader learns that most missing OTPs are push messages with no backup, Smart Fallback isn't an ad: it's the answer.
4. **Link to the technical docs**, so the business reader can hand it to their team and the evaluation keeps moving.
5. **End with one concrete next step**: a demo, a health check, a workshop. Something an account manager can follow up on.

| Signal in the documentation | Add-on it leads to |
|---|---|
| "Every mandatory notification should have a backup channel" | Smart Fallback |
| "How many OTPs needed an SMS last month, and why?" | Delivery Insights |
| "Know a critical notification failed before the customer calls" | Delivery Insights |

## Writing principles

Business content gets the same discipline as technical documentation:

- **Accurate first.** Every statement about how the product works matches the technical docs: statuses, retries, release cadence, what's included in each plan.
- **No invented proof.** No made-up statistics or customer quotes. Where an example helps, it's labelled as illustrative.
- **Plain language.** Benefits explained in the reader's terms, not adjectives. "Changing a channel doesn't need a release" instead of "seamless flexibility".
- **Regulation handled with care.** Regulatory content explains principles and always sends the reader to their compliance team for decisions.

## Contact

- [LinkedIn](https://www.linkedin.com/in/ltejdor)
- [Technical writing portfolio](https://github.com/ltejdor/technical-writing-portfolio)
