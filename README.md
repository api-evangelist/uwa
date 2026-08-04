# University of Western Australia (uwa)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The University of Western Australia (UWA) is a public research university in Perth, Western Australia, ranked #80 in the QS World University Rankings 2025. This repository catalogs UWA's public developer and API footprint as an APIs.json provider profile for the API Evangelist network.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/uwa/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=uwa-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Australia, Perth

## APIs

- **UWA Developer Portal (Azure API Management)** — Microsoft Azure API Management developer portal for discovering, trying, and subscribing to UWA APIs and products via API keys (gated behind sign-in). Docs: https://api-portal.uwa.edu.au/
- **UWA Profiles and Research Repository (Pure CRIS Web Service)** — Elsevier Pure CRIS Web Service exposing research outputs, people, organisations, projects, and activities; API key required. Docs: https://api.research-repository.uwa.edu.au/ws/api/524/api-docs/documentation/Default.htm

## Plans / Rate Limits / FinOps

- Plans: [plans/uwa-plans-pricing.yml](plans/uwa-plans-pricing.yml)
- Rate Limits: [rate-limits/uwa-rate-limits.yml](rate-limits/uwa-rate-limits.yml)
- FinOps: [finops/uwa-finops.yml](finops/uwa-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.uwa.edu.au/
- GitHub: https://github.com/uwa
- LinkedIn: https://www.linkedin.com/school/the-university-of-western-australia/
- Twitter: https://twitter.com/uwanews
- Developer Portal: https://api-portal.uwa.edu.au/
- Review: [review.yml](review.yml)

## Notes

Findings reflect publicly observable surfaces as of 2026-06-03. The Azure API Management portal (api-portal.uwa.edu.au) is a JavaScript application whose product/API catalog sits behind sign-in, so individual endpoints could not be publicly enumerated. The research repository runs Elsevier Pure CRIS and requires an API key for calls. The official github.com/uwa organization exists but had no public repositories at review time. No public open-data, course/timetable, or OAI-PMH endpoint was confirmed. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
