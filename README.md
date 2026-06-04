# University of Western Australia (uwa)

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
