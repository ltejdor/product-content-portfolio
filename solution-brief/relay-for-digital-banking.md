# One integration for every message your customers can't miss

**Relay for digital banking teams · Solution brief**

**Who this is for:** CTOs, heads of digital banking and IT architects evaluating how their bank sends notifications.

> Relay is a fictional notification platform, used here as an example. Its developer documentation is in the [technical writing portfolio](https://github.com/ltejdor/technical-writing-portfolio/tree/main/api-reference).

---

## The problem: every channel is a separate project

In most banks, notifications grew one system at a time. The login system sends OTPs by SMS. The card platform sends payment alerts through its own push provider. Marketing has a separate tool for campaigns.

The result is familiar:

- **Every change is an IT project.** Moving OTPs from SMS to push means touching the login system, testing it and waiting for the next release window.
- **Nobody sees the full picture.** When a customer says an OTP never arrived, support has to check three systems, if they can check at all.
- **Costs are hard to control.** SMS is often sent by default, even to customers who have the app and would get a push for a fraction of the cost.

## How Relay solves it

Your systems tell Relay **what** to notify and **to whom**. Relay decides **how**, based on rules your bank controls.

| Instead of... | With Relay... |
|---|---|
| Each system connecting to each channel | Every system connects once, to one API. |
| Channel logic hard-coded in each system | Channels, order and fallbacks are configuration. Changing them doesn't need a release. |
| A separate record in each system | One delivery history per customer, across every channel. |
| Consent checks spread across tools | Relay checks marketing consent before sending, every time. |

**What this means for your roadmap:** once a system is connected, your business teams can change how customers are notified, for example moving OTPs from SMS to push with SMS as a backup, without asking IT for a new project.

## What integration takes

Relay is designed so that the integration is the smallest part of the project.

- **One API call to send.** Your developers send the customer, the type of notification and the values for the template. That's it.
- **No duplicate messages, by design.** Every request carries a unique key, so a retry after a network error never sends a customer two OTPs.
- **A sandbox from day one.** Your teams test every notification end to end without reaching real customers.
- **Real-time results.** Relay tells your systems what happened to each notification through webhooks, so you don't have to keep asking.

Your developers can read the [API reference](https://github.com/ltejdor/technical-writing-portfolio/tree/main/api-reference) and try it against a mock server before the first meeting.

## Built for regulated banking

- **Strong customer authentication.** OTPs can be configured to always have a backup channel and never wait for quiet hours.
- **Consent by default.** Every notification belongs to a category: mandatory, service or marketing. Relay applies the right rules to each one automatically. Read [our guide to notification compliance](../guide/notification-compliance-guide.md).
- **Traceability.** Every attempt on every channel is recorded with its time and result, ready for audits and customer complaints.
- **Predictable change.** Relay releases once a year, with a migration guide and a long transition period for anything that changes your integration.

## Plans

| | Relay Core | + Smart Fallback | + Delivery Insights |
|---|---|---|---|
| One API for push, SMS and email | ✓ | ✓ | ✓ |
| Notification categories and consent checks | ✓ | ✓ | ✓ |
| Webhooks and delivery history | ✓ | ✓ | ✓ |
| Automatic fallback between channels, per notification type | | ✓ | ✓ |
| Dashboards: delivery rate, fallback rate and cost per channel | | | ✓ |
| Alerts when a mandatory notification isn't delivered | | | ✓ |

Most banks start with Relay Core and Smart Fallback for OTPs and security alerts, then add Delivery Insights once they want to optimise channel costs.

## Next step

Book a 45-minute technical session with your account manager. Bring your architect: we'll map your current notification flows and show what the first integration would look like.
