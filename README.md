# Shanghai Jiao Tong University (shanghai-jiao-tong-university)

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

Shanghai Jiao Tong University (SJTU), founded in 1896 in Shanghai, China, is one of China's leading research universities and is ranked #56 in the QS World University Rankings 2025. This repository catalogs SJTU's public developer and API footprint as an [APIs.json](https://apisjson.org) profile, centered on its official developer platform at [developer.sjtu.edu.cn](https://developer.sjtu.edu.cn/).

APIs.json: https://raw.githubusercontent.com/api-evangelist/shanghai-jiao-tong-university/refs/heads/main/apis.yml

Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=shanghai-jiao-tong-university-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, China, GraphQL, Identity, OpenID Connect

## APIs

- **jAccount Single Sign-On (OAuth 2.0 / OIDC)** — SJTU's identity and SSO system providing OAuth 2.0 / OpenID Connect authorization for third-party member sites. Docs: https://developer.sjtu.edu.cn/auth/oidc.html
- **SJTU Data Resources GraphQL API** — GraphQL data platform (POST to https://graphql.sjtu.edu.cn/graphql) for account, faculty, teaching, and paper data; access by approved application. Docs: https://developer.sjtu.edu.cn/graphql/graphql.html
- **Undergraduate Teaching APIs** — Course and teaching data (current academic year). Docs: https://developer.sjtu.edu.cn/graphql/student.html
- **Faculty APIs** — Faculty/staff profile data. Docs: https://developer.sjtu.edu.cn/graphql/faculty.html
- **Academic Paper APIs** — Publication/paper metadata. Docs: https://developer.sjtu.edu.cn/graphql/paper.html
- **Account APIs** — Account-related information. Docs: https://developer.sjtu.edu.cn/graphql/account.html

## Plans / Rate Limits / FinOps

- Plans: [plans/shanghai-jiao-tong-university-plans-pricing.yml](plans/shanghai-jiao-tong-university-plans-pricing.yml)
- Rate Limits: [rate-limits/shanghai-jiao-tong-university-rate-limits.yml](rate-limits/shanghai-jiao-tong-university-rate-limits.yml)
- FinOps: [finops/shanghai-jiao-tong-university-finops.yml](finops/shanghai-jiao-tong-university-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://en.sjtu.edu.cn/
- Developer Portal: https://developer.sjtu.edu.cn/
- Authentication: https://developer.sjtu.edu.cn/auth/oidc.html
- GitHub: https://github.com/sjtug
- LinkedIn: https://www.linkedin.com/school/shanghai-jiao-tong-university/

## Notes

- All listed documentation URLs were verified live (HTTP 200) on 2026-06-03. The jAccount OAuth authorize endpoint resolves (HTTP 400 without valid parameters), and the GraphQL endpoint resolves (HTTP 200) but is gated behind an application/approval process and credentials, so it was not exercised.
- The `api.sjtu.edu.cn` host referenced in OAuth docs did not resolve directly during probing.
- Most developer documentation is in Chinese.
- No single official university-wide GitHub organization exists; `sjtug` (SJTU *nix User Group) is the most established verified community org. Many department/lab orgs (Thinklab-SJTU, SJTU-IPADS, SJTU-HPC, etc.) also exist.
- No fabricated endpoints: only confirmed, publicly documented APIs are cataloged.

## Maintainers

- Kin Lane — kin@apievangelist.com
