# Mandatory, service or marketing? A practical guide to notification compliance for banks

**Guide · For product owners, compliance and digital teams**

> Relay is a fictional notification platform, used here as an example. This guide describes general principles of EU regulation. It isn't legal advice: rules vary by country and change over time, so confirm every decision with your compliance team. The technical version of this topic is [Mandatory, service and marketing notifications](https://github.com/ltejdor/technical-writing-portfolio/blob/main/concepts/notification-categories.md).

---

## Why this matters

Banks send customers dozens of different notifications. Each one sits somewhere between two risks:

- **Not sending something the customer needed.** A fraud alert that never arrives, or a legally required notice that wasn't sent.
- **Sending something the customer didn't agree to.** A promotion to a customer who never gave marketing consent.

The first erodes trust and can breach regulation. The second can too, and it's the kind of mistake customers remember. Most banks manage both risks with spreadsheets, team knowledge and good intentions. This guide offers a simpler model: decide the **category** of each notification once, and let the rules follow from it.

## Three categories, three sets of rules

### Mandatory: the customer must receive it

**Examples:** one-time passwords, fraud and security alerts, notices the bank is legally required to send.

OTPs are part of strong customer authentication, required under the EU's second Payment Services Directive (PSD2) for most online payments and logins. Regulations such as PSD2 and the Digital Operational Resilience Act (DORA) also require banks to inform customers without undue delay when a major incident affects their financial interests.

**What it implies:** no opt-out, no quiet hours, and a backup channel if the first one fails.

### Service: helps the customer manage their products

**Examples:** card payment alerts, low balance warnings, direct debit reminders.

These are part of the service the customer contracted, so they don't need marketing consent. But customers expect control: someone who pays by card ten times a day may not want ten alerts.

**What it implies:** respect the customer's preferences, and consider quiet hours for anything that can wait.

### Marketing: promotes a product or offer

**Examples:** a new savings product, a pre-approved loan, a cashback campaign.

Under EU rules on electronic communications (the ePrivacy Directive, as each country implements it) and the GDPR, marketing by push, SMS or email generally requires the customer's prior consent, which they can withdraw at any time.

**What it implies:** check consent before every send, and always apply quiet hours.

## A four-question test

When your bank creates a new notification, ask these questions in order. The first "yes" gives you the category.

1. Does the customer need it to authenticate, or to protect their money or data? → **Mandatory**
2. Does a regulation require the bank to send it? → **Mandatory**
3. Does it promote a product, offer or service the customer doesn't have yet, even partly? → **Marketing**
4. Otherwise → **Service**

## The most common mistake: mixed messages

> "Your card payment of €45.00 at Café Central was approved. Get 2% cashback with our Premium card!"

It looks like a payment alert. Because of the last sentence, it's marketing: it needs consent. Customers who haven't consented shouldn't receive it, which means they also lose the payment alert.

**The fix:** send two notifications. The payment alert as a service notification, and the offer as a marketing notification, only to customers who have consented.

## Checklist for your notification catalogue

Use this with your compliance and product teams, once a year or whenever you add a notification type.

- [ ] Every notification type has a category, and someone owns that decision.
- [ ] Every mandatory notification has a backup channel.
- [ ] Every notification required by law has the regulation referenced next to it.
- [ ] No service notification contains promotional content.
- [ ] Marketing notifications are checked against consent at the moment of sending, not when the campaign was planned.
- [ ] You can show, for any customer, which notifications were sent, when, on which channel and with what result.

## How Relay helps

In Relay, the category is part of each notification type's configuration. Once you set it, Relay applies the rules automatically: it checks consent for every marketing notification, never delays a mandatory one, and records every attempt for audits.

| Checklist item | In Relay |
|---|---|
| Category for every notification | Required on every notification type. Included in Relay Core. |
| Backup channel for mandatory notifications | Automatic fallback per notification type, with **Smart Fallback**. |
| Consent checked at sending | Automatic for every marketing notification. Included in Relay Core. |
| Full history for any customer | Every attempt on every channel. Included in Relay Core. |
| Know when a mandatory notification fails | Alerts with **Delivery Insights**. |

## Next step

Review your notification catalogue with this checklist. If you'd like a second pair of eyes, your account manager can run a catalogue review workshop with your product and compliance teams.
