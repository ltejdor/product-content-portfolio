# Know what happened to every notification, as it happens

**Real-time delivery updates and Delivery Insights · Feature page**

**Who this is for:** heads of digital channels and operations managers at banks who are responsible for how customers are notified.

> Relay is a fictional notification platform, used here as an example. The developer guide for this feature is [Receive delivery updates with webhooks](https://github.com/ltejdor/technical-writing-portfolio/tree/main/webhooks).

---

## "Sent" isn't enough

Most notification tools tell you a message was sent. That's where the questions start:

- Did the OTP reach the customer, or are they stuck on the login screen?
- How many of last night's fraud alerts were delivered by push, and how many needed an SMS?
- Why did SMS costs go up this month?

When the answer depends on someone exporting logs and building a spreadsheet, nobody asks until something goes wrong.

## Every status change, the moment it happens

Relay tells your systems what happened to each notification as soon as it happens, on every channel:

| Moment | What your systems know |
|---|---|
| The push didn't arrive in time | Relay is moving to the SMS backup. |
| The SMS was delivered | The customer has the message. |
| Every channel failed | The customer didn't get a message they needed. Act now. |
| A marketing message wasn't sent | The customer hasn't consented. Nothing is broken. |

Your teams can act on this in their own tools: open a ticket automatically, warn the customer in the app, or update a case in your CRM.

**Secure and reliable by design.** Every update is signed, so your systems only accept updates that really come from Relay. If your systems are unavailable, Relay keeps retrying for almost a day, so no update is lost during maintenance windows.

*Included in Relay Core.*

## Delivery Insights: turn updates into decisions

Real-time updates tell you about one notification. **Delivery Insights** shows you the patterns across all of them, without building anything.

### See where your channel budget goes

Track delivery rate, fallback rate and cost per channel for each type of notification. Spot, for example, that a large share of your OTPs fall back to SMS, and find out why.

### Find out why pushes fail

Fallbacks are grouped by reason: customers without the app, phones offline, notifications disabled. Each reason has a different fix, and a different team that owns it:

| Main reason for fallback | Who can fix it | How |
|---|---|---|
| Customer doesn't have the app | Digital marketing | App adoption campaigns for customers who still rely on SMS. |
| Notifications disabled on the phone | Product | Ask for permission at a better moment in the app journey. |
| Phone offline at the time | Nobody needs to | This is what the SMS backup is for. |

### Be the first to know when something critical fails

Get alerted when a mandatory notification, such as an OTP or a fraud alert, isn't delivered by any channel. Your team can contact the customer before they call you.

*Available as an add-on to Relay Core.*

## How a bank might use it

> **Example scenario:** a bank sends most OTPs by SMS, out of habit. With Delivery Insights, it sees that most of its customers have the app installed. It configures push first with an SMS backup after 30 seconds. The SMS backup stays in place for customers who need it, and the bank can see in the dashboard how much of its OTP traffic has moved to push.

This is an illustrative scenario. Your results depend on your customers' app adoption and your SMS costs.

## Next step

- **For your developers:** the [webhooks guide](https://github.com/ltejdor/technical-writing-portfolio/tree/main/webhooks) explains every detail, and the [interactive playground](https://ltejdor.github.io/technical-writing-portfolio/playground/#webhooks) shows it working in a minute.
- **For you:** ask your account manager for a Delivery Insights demo with your own sandbox data.
