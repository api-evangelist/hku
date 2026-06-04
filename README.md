# University of Hong Kong (hku)

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
