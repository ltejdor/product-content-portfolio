# Fewer "my OTP never arrived" calls: a playbook for banks

**Customer success playbook · For heads of customer service and digital operations**

> Relay is a fictional notification platform, used here as an example. The step-by-step diagnosis for support agents is [A customer didn't receive an OTP](https://github.com/ltejdor/technical-writing-portfolio/blob/main/troubleshooting/otp-not-received.md).

---

## Why these calls matter

An OTP that doesn't arrive isn't a small inconvenience. The customer can't log in or can't pay, often while they're at a till or about to miss a transfer deadline. They call, frustrated, and your agent usually can't see what happened.

Each call costs agent time. Some end with the customer going to a branch or abandoning a payment. And every one is a moment where the customer decides whether your digital banking can be trusted.

This playbook shows how to reduce these calls in three stages: **resolve** them faster, **prevent** most of them, and **anticipate** the rest.

## Stage 1: Resolve faster

**Goal:** an agent knows what happened within the first minute of the call.

With Relay, agents find the customer's OTP with only the customer ID and the approximate time. Each notification shows every channel Relay tried and why it failed, if it did. In most cases, the cause is one of five, and each has a clear answer for the customer.

**What to do:**

1. Give second-line support access to the Relay console.
2. Share the [diagnosis guide](https://github.com/ltejdor/technical-writing-portfolio/blob/main/troubleshooting/otp-not-received.md) with them and add it to your support knowledge base.
3. Ask agents to tag the cause in each ticket. Within a month, you'll know which causes are most common in your bank.

*Uses Relay Core.*

## Stage 2: Prevent most of them

**Goal:** an OTP that can't be delivered by one channel is delivered by another, automatically.

The most common cause of a missing OTP is simple: it was sent by push, and the phone was offline or didn't have the app. Without a backup, the customer gets nothing. With one, they get an SMS a few seconds later and never call.

The second most common cause is timing: the backup exists, but starts so late that the OTP has expired when it arrives.

**What to do:**

1. Make sure every OTP and security alert has a backup channel.
2. Set a short wait before the backup starts, typically under a minute for OTPs.
3. Check that the wait plus the delivery time is well under the OTP's expiry time.

*Uses **Smart Fallback**. If your bank doesn't have it yet, this is where it pays for itself: ask your account manager for a trial on OTPs only.*

## Stage 3: Anticipate the rest

**Goal:** your team knows an OTP failed before the customer calls.

Some OTPs will still fail on every channel: a wrong phone number in the customer's profile, a carrier blocking messages. You can't prevent all of them, but you can be first to know.

**What to do:**

1. Set up an alert for any mandatory notification that isn't delivered by any channel.
2. Route it to a team that can act: for example, show a message in the app, or flag the customer's profile for a phone number check.
3. Review the weekly trend. A sudden rise in one cause, such as carrier rejections, usually points to a problem you can escalate.

*Uses **Delivery Insights**.*

## How to measure progress

Agree on these three numbers with your team before you start, and review them monthly:

| Metric | Where to find it | What good looks like |
|---|---|---|
| OTP-related calls per month | Your contact center tool, using the ticket tag from Stage 1 | Going down month after month |
| OTPs delivered by any channel | Relay delivery history, or Delivery Insights | As close to all of them as possible |
| Average time to resolve an OTP call | Your contact center tool | Under a few minutes |

## Next step

Your account manager can run a free OTP health check: we look at a month of your OTP delivery data with you, identify your most common causes, and show which stage would have the biggest impact for your bank.
