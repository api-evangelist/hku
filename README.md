# University of Hong Kong (hku)

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

The University of Hong Kong (HKU) is a public research university in Hong Kong SAR, ranked #27 in the QS World University Rankings 2025. This repository catalogs HKU's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile for the API Evangelist network.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/hku/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=hku-api-evangelist&utm_content=repo

## Type

- Type: Index
- Position: Consumer
- Access: 3rd-Party

## Tags

Education, Higher Education, University, Research Data, Open Access, Hong Kong

## APIs

- **HKU ITS API Developer Portal** — Azure API Management developer portal; discover/try APIs and sign up for keys (gated). Docs: https://developer.hku.hk/
- **HKU DataHub (Figshare)** — Research-data repository on Figshare; public content via the Figshare REST API. Docs: https://docs.figshare.com/
- **HKU Scholars Hub OAI-PMH** — DSpace institutional repository with an OAI-PMH metadata-harvesting interface. Docs: https://hub.hku.hk/

## Plans, Rate Limits, and FinOps

- Plans / Pricing: [plans/hku-plans-pricing.yml](plans/hku-plans-pricing.yml)
- Rate Limits: [rate-limits/hku-rate-limits.yml](rate-limits/hku-rate-limits.yml)
- FinOps: [finops/hku-finops.yml](finops/hku-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.hku.hk/
- Developer Portal: https://developer.hku.hk/
- GitHub: https://github.com/hku-official
- LinkedIn: https://www.linkedin.com/school/university-of-hong-kong/
- Review: [review.yml](review.yml)

## Notes

Verification caveats (probed 2026-06-03): `developer.hku.hk` (HTTP 200) is gated behind institutional sign-in, so individual APIs are not publicly enumerable. `datahub.hku.hk` / `hku.figshare.com` (HTTP 202) are Figshare-hosted; the public Figshare REST API (`api.figshare.com`, 200) serves their content. `hub.hku.hk` (HKU Scholars Hub, DSpace, OAI-PMH at `/oai/request`) returned HTTP 403 to automated probes — consistent with bot/WAF blocking, documented as live but not independently confirmed live. `github.com/hku-official` is the official org but has no public repositories. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
