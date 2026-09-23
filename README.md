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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The University of Western Australia (UWA) is a public research university in Perth, Western Australia, and a member of the Group of Eight. This repository catalogs UWA's public developer and API footprint as an APIs.json provider profile for the API Evangelist network.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/uwa/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=uwa-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party
- University (Public Research University)

## Tags

Education, Higher Education, University, Australia, Group of Eight, Perth, Research, Research Data, Research Repository, Identity Federation, OAI-PMH, Library

## Who operates what

Every surface below carries an `x-operator` in `apis.yml`. For a university that distinction matters more than artifact count: **institution** means UWA runs the thing the contract describes; **tenant** means UWA is a customer on a vendor platform, so the data is UWA's and the contract is the vendor's.

### Institution-operated

- **UWA Research Repository OAI-PMH** (`institution`) — open, unauthenticated OAI-PMH 2.0 harvesting at `https://api.research-repository.uwa.edu.au/ws/oai`. All six verbs returned 200 with no credential on 2026-08-30; 167 sets, five metadata prefixes (`oai_dc`, `qdc`, `mods`, `xmetadiss`, `nl_didl`), OpenAIRE CERIF 1.2 schema location. The repository software underneath is Elsevier Pure, but OAI-PMH is an open standard on UWA's own host with a UWA admin contact. Description: [openapi/uwa-oai-pmh-openapi.yml](openapi/uwa-oai-pmh-openapi.yml) — authored by API Evangelist from live probes, not published by UWA.
- **UWA Shibboleth Identity Provider** (`institution`) — signed SAML 2.0 federation metadata at `https://idp.uwa.edu.au/idp/shibboleth`, scoped to `uwa.edu.au`, HTTP-POST and HTTP-Redirect SSO bindings.
- **UWA API Gateway and Developer Portal** (`institution`) — Azure API Management. The gateway at `api.uwa.edu.au` is live (HTTP/2 404 + `application/json` + Azure `request-context`); the portal at `api-portal.uwa.edu.au` serves the stock Azure shell with the catalog behind sign-in and a 404 on `/signup`. Nothing is enumerable.

### Tenant (vendor platform, UWA tenancy)

- **UWA Profiles and Research Repository** (`tenant`) — Elsevier **Pure**, portal at `research-repository.uwa.edu.au`, CRIS web service at `api.research-repository.uwa.edu.au/ws/api/524`. The spec served there declares `info.title: Pure Web Service 524` and `info.contact.name: Elsevier`.
- **UWA Library OneSearch** (`tenant`) — Ex Libris **Primo VE**, tenant `61UWA_INST`.

## Correction, 2026-08-30

This profile was rebuilt under the university pipeline's operator axis. The June 2026 profile carried **29 `apis[]` entries, 28 of which were per-tag splits of one Elsevier Pure Web Service contract**, and those 28 entries additionally declared `baseURL: https://api-portal.uwa.edu.au/` while the specs' own `servers[]` said `api.research-repository.uwa.edu.au`. Removed in this run: the 28 refined per-tag OpenAPIs, the pristine Pure source spec, and every artifact derived from it — 57 Postman/OpenCollection files, 5 JSON Schemas, 5 JSON Structures, 5 examples, a JSON-LD context, a Pure vocabulary, two Spectral rulesets, an authentication summary, an agentic-access classification and a capability map. None of it was UWA's engineering.

Added: an OAI-PMH description and real probed responses, a conformance record, a probed authentication summary, and a deployment vocabulary read off UWA's own endpoint. **This correction lowers UWA's Kin Score, and that is the point** — the score it previously carried was Elsevier's.

## Standards conformance (Kin Score `education` regime)

Confirmed from response bodies, not prose claims — see [conformance/uwa-conformance.yml](conformance/uwa-conformance.yml):

- `oai-pmh` — **yes**, all six verbs 200, unauthenticated
- `shibboleth` — **yes**, Shibboleth IdP metadata with `shibmd:Scope uwa.edu.au`
- `saml` — **yes**, SAML 2.0 `EntityDescriptor` / `IDPSSODescriptor`
- `openaire-cerif-1.2` — partial (schema location + `openaire` set observed, XSD not validated)
- `crossref` — partial (Crossref DOIs in harvested `dc:identifier`; not evidence of membership)
- `orcid`, `datacite`, `scim`, `lti`, `oneroster`, `ed-fi`, `caliper`, `qti` — not found

## Artifacts

- OpenAPI: [openapi/uwa-oai-pmh-openapi.yml](openapi/uwa-oai-pmh-openapi.yml) · pristine copy in [openapi/_original/](openapi/_original/)
- Examples (real probed responses): [examples/](examples/)
- Vocabulary: [vocabulary/uwa-vocabulary.yml](vocabulary/uwa-vocabulary.yml)
- Conformance: [conformance/uwa-conformance.yml](conformance/uwa-conformance.yml)
- Authentication: [authentication/uwa-authentication.yml](authentication/uwa-authentication.yml)
- Domain security: [security/uwa-domain-security.yml](security/uwa-domain-security.yml)
- Plans: [plans/uwa-plans-pricing.yml](plans/uwa-plans-pricing.yml)
- Rate limits: [rate-limits/uwa-rate-limits.yml](rate-limits/uwa-rate-limits.yml)
- FinOps: [finops/uwa-finops.yml](finops/uwa-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.uwa.edu.au/
- News: https://www.uwa.edu.au/news
- Privacy: https://www.uwa.edu.au/privacy
- Disclaimer / copyright: https://www.uwa.edu.au/disclaimer-copyright
- Support: https://www.uwa.edu.au/contact-us
- GitHub: https://github.com/uwa (verified as The University of Western Australia; zero public repositories)
- LinkedIn: https://www.linkedin.com/school/the-university-of-western-australia/
- X: https://x.com/uwanews
- Developer Portal: https://api-portal.uwa.edu.au/
- Identity Federation: https://idp.uwa.edu.au/idp/shibboleth
- Research Repository: https://research-repository.uwa.edu.au/
- Library Catalog: https://onesearch.library.uwa.edu.au/
- Course Catalog: https://www.handbooks.uwa.edu.au/
- AI guidance: https://guides.library.uwa.edu.au/artificial_intelligence
- Review: [review.yml](review.yml)

## Notes

Findings reflect publicly observable surfaces probed on 2026-08-30. No open data portal exists — `data.uwa.edu.au` and `data.research.uwa.edu.au` do not resolve. No public course, timetable, transit or room-booking API was found; `handbooks.uwa.edu.au` and `resourcebooker.uwa.edu.au` are HTML applications. `/.well-known/security.txt` and `llms.txt` return 404, and `idp.uwa.edu.au/.well-known/openid-configuration` returns 404 — UWA's federation surface is SAML, not OIDC. UWA publishes no first-party OpenAPI of any kind. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
