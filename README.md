# Shanghai Jiao Tong University (shanghai-jiao-tong-university)

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
