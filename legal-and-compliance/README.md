# Legal, Tax & Compliance for Global Indie Founders

> **A first-principles legal, tax, and compliance guide for independent software developers operating global digital products.**

---

## 1. Global Business Incorporation Options

When launching a commercial SaaS or paid digital product, registering a formal business entity insulates founders from personal financial liability and enables global banking access.

```text
┌───────────────────────────────────────────────────────────────────────────┐
│                      INCORPORATION DECISION MATRIX                        │
└───────────────────────────────────────────────────────────────────────────┘
   Indie Bootstrapper (Solo / Micro-SaaS) ──► US Delaware LLC (Single-member, Pass-through tax)
   VC-Track / Multi-Founder Equity        ──► US Delaware C-Corp (Stock issuance, VC friendly)
```

| Entity Type | Tax Treatment | Complexity | Best For |
| :--- | :--- | :--- | :--- |
| **US Delaware LLC** | Pass-through taxation (Profits flow directly to personal tax return) | Low maintenance & reporting | Solo indie hackers, bootstrapped SaaS |
| **US Delaware C-Corp** | Corporate tax rate + personal dividend tax | High reporting & stock management | Multi-founder startups, VC fundraising |

### Turnkey Formation Platforms
- **[Stripe Atlas](https://stripe.com/atlas)**: Automated US Delaware LLC or C-Corp formation with a US bank account (Mercury / SVB) and Stripe integration.
- **[Firstbase](https://firstbase.io)**: Global incorporation platform for non-US residents.

---

## 2. Handling Global Digital Sales Tax, VAT & GST

Selling digital products globally subjects your business to local Value Added Tax (VAT) and Goods and Services Tax (GST) in over 100 countries—even without a physical presence.

```text
┌───────────────────────────────────────────────────────────────────────────┐
│                    PAYMENT PROCESSOR VS MERCHANT OF RECORD                │
└───────────────────────────────────────────────────────────────────────────┘
   Traditional Gateway (Stripe) ──► You are responsible for global tax filing in 100+ countries.
   Merchant of Record (Paddle)  ──► MoR acts as reseller & remits all global taxes automatically.
```

- **Merchant of Record (MoR)** (*Paddle, Lemon Squeezy*): The MoR sells your software as the legal reseller, handling global tax compliance, VAT remittance, and local currency billing automatically.
- **Payment Processor** (*Stripe*): Lower fees per transaction (2.9% + $0.30), but requires using Stripe Tax or tax services (TaxJar, Anual) to calculate and file local sales taxes manually.

---

## 3. Core Legal Agreements & Policies

Every commercial website or application must display three foundational legal documents:

1. **Terms of Service (ToS)**: Defines user obligations, acceptable use policies, payment terms, refund rules, and liability limitations.
2. **Privacy Policy**: Explicitly details what user data you collect (cookies, IP addresses, emails), how it is processed, and third-party services used (e.g., Stripe, Plausible, Vercel).
3. **Cookie Policy & Banner**: Required in jurisdictions enforcing GDPR or ePrivacy directives.

---

## 4. Global Data Protection Compliance (GDPR & CCPA)

- **General Data Protection Regulation (GDPR - EU)**: Mandates explicit user consent before tracking, the right to data deletion ("Right to be Forgotten"), and user data portability.
- **California Consumer Privacy Act (CCPA - US)**: Requires clear "Do Not Sell My Personal Information" options and transparent data collection disclosures.

---

## 5. Summary

Addressing legal, tax, and compliance requirements early prevents expensive legal hurdles as your product scales. Utilizing a Merchant of Record and standard legal templates allows indie founders to sell globally with complete peace of mind.
