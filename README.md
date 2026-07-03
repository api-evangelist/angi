# Angi (angi)

Angi (formerly Angie's List, founded 1995) is a digital home services marketplace connecting homeowners with home service professionals for repair, maintenance, and improvement projects. Angie's List merged with IAC's HomeAdvisor in 2017 under parent ANGI Homeservices Inc.; in March 2021 the consumer brand and parent company were both renamed Angi, with HomeAdvisor continuing as the pro-facing "Angi Leads" lead-generation business. IAC fully spun off its stake in April 2025, making Angi Inc. (NASDAQ: ANGI) an independent public company. Angi does not operate a self-serve public developer portal or publish an API reference. It does offer a gated, partner-only lead-delivery mechanism: Angi Ads/Angi Leads pushes new homeowner leads as JSON to a webhook URL a pro's CRM provides (authenticated with an X-API-KEY header), and an OAuth-style "Sign in with Angi" account-linking flow used by a short list of approved CRM/field-service partners (ServiceTitan, Jobber) to receive lead and booking data. Both require a direct arrangement with an Angi Ads Client Success Manager rather than self-serve API keys.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/angi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/angi/refs/heads/main/apis.yml)

## Rebrand History

- **1995:** Angie's List founded as a members-only home service provider review service.
- **2017:** IAC's HomeAdvisor merges with Angie's List under a new parent, ANGI Homeservices Inc.
- **March 2021:** Angie's List renamed Angi; ANGI Homeservices Inc. renamed Angi Inc. HomeAdvisor continues internally as the pro-facing "Angi Leads" lead-generation business.
- **April 2025:** IAC completes the spin-off of its stake in Angi; Angi Inc. (NASDAQ: ANGI) becomes a fully independent public company.

No historical Angie's List public developer API was found to have ever existed as a self-serve, documented product - GitHub's [angieslist](https://github.com/angieslist) organization contains only internal tooling forks (an Airbnb JavaScript style guide fork, a PetaPoco ORM fork, a gulp-shell fork), not API clients or SDKs, and has been inactive since 2022.

## Tags

- Home Services
- Marketplace
- Leads
- Angie's List
- HomeAdvisor
- IAC
- Webhook
- No Public API

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Angi Leads Delivery (Webhook) API

Not a self-serve public API - there is no published base URL, API reference, or API key signup. Once a pro or CRM partner is approved by an Angi Ads Client Success Manager, Angi Ads/Angi Leads pushes each new homeowner lead as a JSON POST to a webhook URL the partner's CRM supplies, authenticated with an X-API-KEY header. Angi documents the lead field list in its help center and also supports connecting via Zapier for CRMs without a native integration. Verified integrations exist for ServiceTitan, Jobber, SmartMoving, ActiveProspect, and Smith.ai.

- **Human URL:** [https://intercom.help/angi/en/articles/10288125-setting-up-api-integration-with-angi](https://intercom.help/angi/en/articles/10288125-setting-up-api-integration-with-angi)
- **Base URL:** `https://www.angi.com` (no dedicated API base URL is publicly published - this is the company's own domain of record)

#### Tags

- Leads
- Webhooks
- Lead Generation
- Partner Integration

#### Properties

- [Documentation](https://intercom.help/angi/en/collections/12900573-api-integrations)
- [API Reference](https://intercom.help/angi/en/articles/10288125-setting-up-api-integration-with-angi)

### Angi Pro Account Linking (Sign in with Angi)

An OAuth-style "Sign in with Angi" account-linking flow used by a short, approved list of CRM and field-service management partners (ServiceTitan, Jobber) to connect a pro's Angi account and receive account, profile, and lead/booking data into the partner platform's native booking screen. No public client-registration process, scope list, or token-endpoint documentation is published; access is arranged directly between Angi and the partner.

- **Human URL:** [https://help.servicetitan.com/docs/angi-leads-integration](https://help.servicetitan.com/docs/angi-leads-integration)
- **Base URL:** `https://www.angi.com` (no dedicated API base URL is publicly published)

#### Tags

- OAuth
- Account Linking
- CRM Integration
- Partner

#### Properties

- [Documentation](https://help.servicetitan.com/docs/angi-leads-integration)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/angi)
- [Website](https://www.angi.com)
- [Documentation](https://intercom.help/angi/en/collections/12900573-api-integrations)
- [Plans](plans/angi-plans-pricing.yml)

## Pricing

Angi does not sell API access as a metered developer product, and it does not publish an official rate card for its Angi Ads / Angi Leads pro advertising program. Third-party contractor reviews and industry guides (2026) put pay-per-lead pricing at roughly **$15-$120+ per lead** on top of a **$200-$600+/month membership fee**, with a standard lead commonly shared among 3-8 (sometimes more) competing pros. Angi Ads is a separate pay-per-click placement product with an annual membership fee. Contracts are typically 12 months with auto-renewal and an early-cancellation fee of roughly 30-35% of the remaining contract value. See [plans/angi-plans-pricing.yml](plans/angi-plans-pricing.yml) for details and sources - none of these figures come from an official Angi price list.

## Review

Does Angi expose a documented public WebSocket API? **No.** Angi does not operate a self-serve public developer portal or API reference of any kind - no REST, GraphQL, WebSocket, or SSE. See [review.yml](review.yml) for the full findings, sourced from Angi's help center, partner integration guides (ServiceTitan, SmartMoving, ActiveProspect), and corporate history.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
