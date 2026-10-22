# What's new in Relay 2026.1: clearer results, fewer false alarms

**Customer announcement · March 2026**

**Who this is for:** business and operations contacts at banks that use Relay. It's sent by email and published in the customer portal, alongside the technical release notes for their IT teams.

> Relay is a fictional notification platform, used here as an example. The technical version of this announcement is the [Relay 2026.1 release notes](https://github.com/ltejdor/technical-writing-portfolio/blob/main/release-notes/relay-2026.1.md).

---

Relay 2026.1 is about trust in your numbers. When a report says a notification failed, it should mean that a customer missed something. When something critical fails, you should know before the customer calls.

## In one minute

- **Your delivery rate becomes more accurate.** Messages Relay doesn't send on purpose, such as marketing to customers who haven't consented, no longer count as failures.
- **You see the backup working.** Relay now reports the moment it moves from push to SMS, so you can measure how often your backup is needed.
- **Support finds any OTP in seconds,** with only the customer and the time.
- **Every notification has a clear category:** mandatory, service or marketing. The right rules apply automatically.
- **Your webhooks are better protected** against a type of attack where a real message is captured and sent again later.

## What this means for you

### "Blocked" is not "failed"

Until now, a marketing notification Relay didn't send because the customer hadn't consented appeared as a failed delivery. Relay was doing exactly what it should, but your reports said otherwise.

From 2026.1, these notifications have their own status: **blocked**. Your delivery rate now reflects real delivery problems only, and your teams stop chasing false alarms.

> **Your IT team may need to act before upgrading.** Reports or alerts that count failed notifications need a small change. We've sent them a [migration guide](https://github.com/ltejdor/technical-writing-portfolio/blob/main/release-notes/migration-2026.1.md) with every step.

### See how often your backup saves the day

Relay now tells you each time a push doesn't arrive and the SMS backup starts. For the first time, you can answer questions like "how many OTPs needed an SMS last month, and why?"

**Want to see it as a dashboard?** Delivery Insights groups every fallback by reason and channel cost, so you can decide where to act. [See how it works](../feature-page/delivery-visibility.md).

### Answer "my OTP never arrived" in seconds

Support teams can now find a customer's notifications with only the customer ID and an approximate time. No more asking IT to search the logs. We've written a [playbook for support teams](../playbook/otp-support-calls.md) on how to use it.

### Categories that apply the rules for you

Every notification type now belongs to a category. We've assigned one to each of your existing types. Please review them with your compliance team: our [practical guide](../guide/notification-compliance-guide.md) explains how to choose.

## Coming up

- **Webinar, 19 March: "What's new in Relay 2026.1."** A 30-minute walkthrough with live demos, and time for your questions. Your account manager will send the invitation.
- **Questions about your upgrade?** Your account manager can plan it with you.
