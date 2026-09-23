<!-- authorship: rewritten 2026-08-30 by the API Evangelist university pipeline.
     method: searched — read from SJTU's own developer portal.
     source: https://developer.sjtu.edu.cn/graphql/graphql.html -->

# Shanghai Jiao Tong University — Data Resources GraphQL API (SUPERSEDED)

**Status: superseded.** This document describes the *old-version* (老版本) GraphQL interface to
SJTU's Data Resources platform. Every current data-resource page on the university's developer
portal now documents REST `GET` operations under `https://graphql.sjtu.edu.cn/v1` and links back to
the GraphQL pages as the legacy interface. The current contract is captured in
[`openapi/shanghai-jiao-tong-university-data-resources-openapi.yml`](../openapi/shanghai-jiao-tong-university-data-resources-openapi.yml).

This file is kept because the transition is undated and unsignalled — no `Sunset` header, no
changelog, no migration guide — and because the API Evangelist profile of SJTU described only this
GraphQL form from 2026-06-03 until 2026-08-30.

- **Operator:** institution (Shanghai Jiao Tong University Network and Information Center)
- **Legacy endpoint:** `https://graphql.sjtu.edu.cn/graphql` (POST `{"query": "..."}`)
- **Current endpoint:** `https://graphql.sjtu.edu.cn/v1/...` (REST GET)
- **Documentation:** https://developer.sjtu.edu.cn/graphql/graphql.html
- **Access:** OAuth 2.0 client credentials, scope `exchange_data`, gated behind the
  数据资源申请流程 approval workflow. The host is additionally restricted to the campus network —
  an off-campus request is 302'd to `https://restrict.sjtu.edu.cn/`.
- **Introspection:** not run. The host cannot be reached from outside the SJTU network, so no
  schema was harvested and none is asserted here.

## The query language

A query has three parts: the type (which is the interface name), the query conditions, and the
selected fields.

```graphql
{
  tm_class(first: 1, offset: 10, filter: { name: { eq: "123" } }) {
    num
    name
    id
  }
}
```

Three built-in arguments are supported — `first` (page start), `offset` (page size) and `filter`.
Field selection is permission-controlled: a field the application was not granted returns null
rather than erroring, and a caller may simply omit fields it did not apply for. Fields may be
aliased (`username: name`).

## Filter keywords

`filter` is a nested key/value structure of the form `{field: {keyword: value}}`. The same key may
not repeat inside one object — use `in` / `nin` instead.

| Keyword | Meaning |
|---|---|
| `eq` | equals |
| `ne` | not equal |
| `ge` | greater than or equal |
| `gt` | greater than |
| `le` | less than or equal |
| `lt` | less than |
| `like` | SQL `LIKE` |
| `nlike` | SQL `NOT LIKE` |
| `in` | SQL `IN`, comma-separated values inside `[]` |
| `nin` | SQL `NOT IN`, comma-separated values inside `[]` |
| `nil` | SQL `IS NULL` |
| `notnull` | SQL `IS NOT NULL` |

`filter` also supports `and` and `or` logical operators with SQL precedence; `and` is the default
when several conditions are listed side by side. String values inside a filter must have their
double quotes escaped when the query is embedded in a host-language string.

Not every field is filterable — each interface documents its own supported query parameters.

## Data categories

The same five categories the REST contract now serves:

| Category | Chinese | Current REST path |
|---|---|---|
| Account | 账号类 | `/v1/account/info` |
| Faculty and staff | 教职工类 | `/v1/faculty/profile`, `/v1/faculty/degree`, `/v1/faculty/post` |
| Undergraduate teaching | 本科教学类 | `/v1/stu/profile`, `/v1/course/info`, `/v1/course/plan`, `/v1/course/selection` |
| Academic papers | 论文类 | `/v1/paper/info` |
| Assets | 资产类 | `/v1/asset/info` |

The asset category did not exist in the profile taken on 2026-06-03.
