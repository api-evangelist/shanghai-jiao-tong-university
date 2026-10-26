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

Shanghai Jiao Tong University (上海交通大学, SJTU), founded in 1896 in Shanghai, China, is a C9 League
public research university. This repository catalogs SJTU's public developer and API footprint as an
[APIs.json](https://apisjson.org) profile, centered on the university's own developer platform at
[developer.sjtu.edu.cn](https://developer.sjtu.edu.cn/).

SJTU is unusual in this cohort. Almost every machine-readable surface attributed to a university is a
vendor's contract running under the institution's name — Figshare, Elsevier Pure, Ex Libris,
Dataverse. **Nothing in this repository is.** Every host is under `sjtu.edu.cn`, and every contract is
the university's own engineering, run by its Network and Information Center (网络信息中心).

APIs.json: https://raw.githubusercontent.com/api-evangelist/shanghai-jiao-tong-university/refs/heads/main/apis.yml

Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=shanghai-jiao-tong-university-api-evangelist&utm_content=repo

## Type

- Index
- University — Public Research University
- Producing
- 1st-Party

## Tags

University, Higher Education, Education, Research, China, C9 League, Identity Federation, Course
Catalog, Research Computing, Campus Life, OAuth, OpenID Connect, SAML, Shibboleth, Payments

## APIs

Every surface below carries `x-operator: institution` — SJTU operates the thing the contract
describes, not just the data behind it.

- **SJTU Open API** (`https://api.sjtu.edu.cn`) — the university's own REST platform. 59 documented
  operations across 13 families: Profile, Task, Enterprise, File, Notification, Mail, Finance,
  Education, Card, Unicode (思源码), Barcode, Calendar, Signature. OAuth 2.0 throughout, one common
  `errno`/`entities[]` envelope, and field-level scope control — the same Profile call returns a
  different object shape to a `basic` token than to a `privacy` one.
  Docs: https://developer.sjtu.edu.cn/api/overview.html
- **SJTU Data Resources API** (`https://graphql.sjtu.edu.cn/v1`) — institutional data exchange over
  account, faculty, undergraduate-teaching, academic-paper and asset records. **Now REST, not
  GraphQL**: the host name is a fossil of an earlier implementation the portal now labels 老版本
  (old version). Docs: https://developer.sjtu.edu.cn/graphql/overview.html
- **jAccount Authorization Server** (`https://jaccount.sjtu.edu.cn/oauth2`) — SJTU's own OAuth 2.0 /
  OpenID Connect provider, publishing discovery at
  `/oauth2/.well-known/openid-configuration` and a 39-scope bitmask registry.
  Docs: https://developer.sjtu.edu.cn/auth/oidc.html
- **SJTU Identity Provider** (`https://jaccount.sjtu.edu.cn/idp`) — Shibboleth SAML 2.0 IdP with
  openly published metadata, federating SJTU into CARSI and through it eduGAIN.
- **Jiao Wo Ban (交我办) Process Platform** — the campus super-app and the low-code workflow platform
  behind it, with a full first-party developer programme. Also the registration surface for every
  other SJTU API. Docs: https://developer.sjtu.edu.cn/form/guide/introduce.html

## Artifacts

| Artifact | Path |
|---|---|
| OpenAPI — Open API (derived) | [openapi/shanghai-jiao-tong-university-open-api-openapi.yml](openapi/shanghai-jiao-tong-university-open-api-openapi.yml) |
| OpenAPI — Data Resources (derived) | [openapi/shanghai-jiao-tong-university-data-resources-openapi.yml](openapi/shanghai-jiao-tong-university-data-resources-openapi.yml) |
| Authentication | [authentication/shanghai-jiao-tong-university-authentication.yml](authentication/shanghai-jiao-tong-university-authentication.yml) |
| OAuth scopes (39 + `openid`) | [scopes/shanghai-jiao-tong-university-scopes.yml](scopes/shanghai-jiao-tong-university-scopes.yml) |
| Error catalog (25 codes) | [errors/shanghai-jiao-tong-university-errors.yml](errors/shanghai-jiao-tong-university-errors.yml) |
| Conformance (education regime) | [conformance/shanghai-jiao-tong-university-conformance.yml](conformance/shanghai-jiao-tong-university-conformance.yml) |
| JSON Schema | [json-schema/](json-schema/) |
| Examples | [examples/shanghai-jiao-tong-university-examples.yml](examples/shanghai-jiao-tong-university-examples.yml) |
| Design rules (SJTU's own) | [rules/shanghai-jiao-tong-university-design-rules.yml](rules/shanghai-jiao-tong-university-design-rules.yml) |
| Lifecycle + the GraphQL→REST migration | [lifecycle/shanghai-jiao-tong-university-lifecycle.yml](lifecycle/shanghai-jiao-tong-university-lifecycle.yml) |
| Vocabulary (identity/document code tables) | [vocabulary/shanghai-jiao-tong-university-vocabulary.yml](vocabulary/shanghai-jiao-tong-university-vocabulary.yml) |
| Well-known probe table + fetched documents | [well-known/](well-known/) |
| Legacy GraphQL interface (superseded) | [graphql/shanghai-jiao-tong-university-graphql.md](graphql/shanghai-jiao-tong-university-graphql.md) |
| Plans / Rate Limits / FinOps | [plans/](plans/) · [rate-limits/](rate-limits/) · [finops/](finops/) |

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://en.sjtu.edu.cn/
- Developer Portal: https://developer.sjtu.edu.cn/
- API Reference: https://developer.sjtu.edu.cn/api/list.html
- Authentication: https://developer.sjtu.edu.cn/auth/oauth.html
- Identity Federation: https://jaccount.sjtu.edu.cn/idp/shibboleth
- Research Computing (交我算): https://docs.hpc.sjtu.edu.cn/
- Library: https://www.lib.sjtu.edu.cn/
- Research Repository: https://scholar.sjtu.edu.cn/
- AI Policy: https://www.sjtu.edu.cn/tg/20250304/207682.html
- Sign-up (application registration): https://my.sjtu.edu.cn/
- LinkedIn: https://www.linkedin.com/school/shanghai-jiao-tong-university/

## What changed on 2026-08-30

This profile was rebuilt under the API Evangelist university pipeline. The 2026-06-03 profile was
correct about ownership and wrong about scope:

- **The entire Open API platform was missing.** 59 operations, 13 families, a 39-scope OAuth
  registry, a 25-entry error table and a published set of design rules — none of it was recorded.
  The June notes said `api.sjtu.edu.cn` "did not resolve during probing"; it does. The host answers
  only under `/v1` and `/v2` and closes the connection at the root, so a root probe reads as dead.
- **The Data Resources API had migrated from GraphQL to REST** with no `Sunset` header, no changelog
  and no dated signal, and this repo still described the superseded GraphQL endpoint. It had also
  gained a fifth data category (资产类, assets).
- **One gated platform had been split into five `apis[]` entries** by data category — the same
  footprint inflation that vendor tag-splitting produces. Collapsed to one surface.
- **Two machine-readable documents were found that had never been catalogued**: OpenID Connect
  discovery at the issuer-relative path (which is why a root probe missed it), and Shibboleth SAML
  IdP metadata.
- **`github.com/sjtug` was re-labelled `x-operator: tenant`** — SJTUG is the SJTU *nix User Group, a
  student organisation with its own domain, not the university's engineering org.

## Notes

- Every URL in `apis.yml` was re-probed on 2026-08-30. Results, including the failures, are in
  `x-coverage.evidence` and in `well-known/shanghai-jiao-tong-university-well-known.yml`.
- SJTU publishes **no** OpenAPI, changelog, status page, deprecation policy, `security.txt`,
  `llms.txt`, agent card or `api-catalog` on any host. Both OpenAPI documents here are DERIVED by
  API Evangelist from SJTU's own HTML documentation and are marked as such in `info.x-provenance`.
- `graphql.sjtu.edu.cn` is restricted to the campus network by design — an off-campus request is
  302'd to `restrict.sjtu.edu.cn` and told to use the SJTU VPN. That is a finding about SJTU.
  `scholar.sjtu.edu.cn` completes TLS and then returns nothing to a caller outside China; that is a
  finding about our vantage, and it is recorded as unverified rather than dead.
- On scholarly infrastructure the gap is real: the Paper API carries `doi` and `wos` as opaque
  strings but conforms to neither Crossref, DataCite nor ORCID, and no OAI-PMH endpoint could be
  reached anywhere on `sjtu.edu.cn`.
- Most developer documentation exists only in Chinese.
- Department and lab GitHub organisations exist (Thinklab-SJTU, SJTU-IPADS, SJTU-HPC and others);
  none is an official university engineering org, and no source is published for any platform above.
- No fabricated endpoints: only confirmed, publicly documented APIs are cataloged.

## Maintainers

- Kin Lane — kin@apievangelist.com
