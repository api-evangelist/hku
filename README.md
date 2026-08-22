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

The University of Hong Kong (HKU) is a public research university in Hong Kong SAR, founded in 1911 and ranked in the top 30 of the QS World University Rankings. This repository catalogs HKU's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile for the API Evangelist network.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/hku/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=hku-api-evangelist&utm_content=repo

## Type

- Type: Index (`x-type: university`, `x-category: Public Research University`)
- Position: Consumer
- Access: 3rd-Party
- ROR: https://ror.org/02zhqgq86

## Tags

Education, Higher Education, University, Hong Kong, Identity Federation, Single Sign-On, Research Data, Open Access, Artificial Intelligence, Research Computing

## Surfaces and who operates them

A university is a federation of buyers. Every surface below carries an operator: `institution`
means HKU runs the thing the contract describes, `tenant` means HKU is an account on someone
else's platform. Tenant contracts are recorded, never stored here as HKU's own.

| Surface | Operator | Probed 2026-08-19 |
|---|---|---|
| **HKU Shibboleth Identity Provider** — `hkafidp.hku.hk`, entityID `https://hkafidp.hku.hk/idp/shibboleth`, scope `hku.hk`, registered by the Hong Kong Access Federation 2016-12-15 and exported to eduGAIN with REFEDS R&S + SIRTFI | institution | 200, signed SAML metadata, 14,831 bytes |
| **HKU AD FS OAuth 2.0 / OpenID Connect issuer** — `adfs.hku.hk`, discovery + JWKS + UserInfo + device code + WS-Fed metadata | institution | 200 discovery, 200 JWKS, 401 UserInfo |
| **HKU ITS API developer portal and gateway** — `developer.hku.hk` + `api.hku.hk` (Azure API Management), GenAI chat/embedding/image APIs opened to students 2026-03-17 | institution | 200 → redirects to `/signin`; gateway 404 envelope |
| **HKU Scholars Hub OAI-PMH** — `hub.hku.hk`, DSpace | institution | 403 Cloudflare challenge — blocked, not absent |
| **HKU DataHub** — `datahub.hku.hk` CNAME → figshare.com | tenant (Figshare) | 202, empty body |
| **HKU Libraries discovery** — `julac-hku.primo.exlibrisgroup.com` | tenant (Ex Libris) | 200 |
| **HKU Microsoft Entra ID tenant** — `login.microsoftonline.com/hku.hk` | tenant (Microsoft) | 200 |

HKU publishes no OpenAPI, no `robots.txt` on `www.hku.hk`, no `llms.txt`, no status page and no API
changelog, and its official GitHub org has no public repositories.

## Artifacts

- OpenAPI (derived from HKU's OIDC discovery document): [openapi/hku-identity-openapi.yml](openapi/hku-identity-openapi.yml)
- Captured discovery document: [well-known/hku-adfs-openid-configuration.json](well-known/hku-adfs-openid-configuration.json)
- JSON Schema: [json-schema/hku-openid-configuration.schema.json](json-schema/hku-openid-configuration.schema.json)
- Examples (real captured responses): [examples/hku-identity-examples.yml](examples/hku-identity-examples.yml)
- Authentication: [authentication/hku-authentication.yml](authentication/hku-authentication.yml)
- Scopes: [scopes/hku-scopes.yml](scopes/hku-scopes.yml)
- Errors: [errors/hku-errors.yml](errors/hku-errors.yml)
- Conformance (education regime): [conformance/hku-conformance.yml](conformance/hku-conformance.yml)
- Identity attribute vocabulary: [vocabulary/hku-identity-attributes.yml](vocabulary/hku-identity-attributes.yml)
- JSON-LD: [json-ld/hku-organization.jsonld](json-ld/hku-organization.jsonld)
- Spectral rules: [rules/hku-identity-rules.yml](rules/hku-identity-rules.yml)
- Lifecycle: [lifecycle/hku-lifecycle.yml](lifecycle/hku-lifecycle.yml)
- Plans / Pricing: [plans/hku-plans-pricing.yml](plans/hku-plans-pricing.yml)
- Rate Limits: [rate-limits/hku-rate-limits.yml](rate-limits/hku-rate-limits.yml)
- FinOps: [finops/hku-finops.yml](finops/hku-finops.yml)
- Domain security: [security/hku-domain-security.yml](security/hku-domain-security.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-19

## Common Properties

- Website: https://www.hku.hk/
- Developer Portal: https://developer.hku.hk/
- Identity Federation: https://hkafidp.hku.hk/idp/shibboleth
- Research Repository: https://hub.hku.hk/
- Library Catalog: https://julac-hku.primo.exlibrisgroup.com/discovery/search?vid=852JULAC_HKU:HKU
- Research Computing: https://hpc.hku.hk/
- AI Policy: https://aied.talic.hku.hk/aipolicy/
- AI Tooling: https://genai.hku.hk/
- Privacy Policy: https://www.hku.hk/about/policies_reports/privacy_policy.html
- GitHub: https://github.com/hku-official
- LinkedIn: https://www.linkedin.com/school/university-of-hong-kong/
- Review: [review.yml](review.yml)

## Notes

**Attribution correction, 2026-08-19.** This profile previously carried eleven API entries derived
from a single Figshare specification — altmetric, articles, authors, collections, institutions,
oauth, other, profiles, projects, symplectic — presented as HKU APIs. They were one vendor
document counted eleven times. The specification has been removed and HKU DataHub is now recorded
for what it is: an HKU tenancy on Figshare's platform, HKU's data under Figshare's contract. The
re-profile replaces them with the surfaces HKU actually operates, which are identity
infrastructure. This lowers the score, and that is the correction working.

Residual vendor-derived files remain on disk pending manual removal and are pointed at by nothing
in `apis.yml`: `collections/` (20 files, every request against `api.figshare.com`) and
`agentic-access/hku-agentic-access.yml` (157 operations derived from the removed Figshare spec).

Access posture was also corrected: the earlier record said "Free · Self-serve signup". HKU's
developer portal redirects every route to institutional sign-in, and API keys are issued only to
HKU staff and students. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
