# Engagement scope

Copy to `security/SCOPE.md` in the project being tested and fill in. Agents refuse to run without it.

## Owner sign-off
- Product:
- Owner of the product and environments (name, role):
- Authorized by (name, date):
- Operator running the agents:
- Valid from / until:

## In scope
| Target | Type (repo, web, API, infra) | Environment | active (yes/no) |
|---|---|---|---|
| ./ (this repository) | repo | n/a | n/a |
| https://staging.example.com | web + API | staging | yes |
| https://example.com | web | production | no (passive only) |

## Out of scope
- Third-party services (payment, auth provider, email, CDN, analytics)
- Anything not listed above

## Test accounts
| Role | Login | Where the password lives (not the password itself) |
|---|---|---|
| user A | | env var SEC_USER_A_PASS |
| user B (same role, other tenant) | | env var SEC_USER_B_PASS |
| admin | | env var SEC_ADMIN_PASS |

Two accounts of the same role are needed for access control checks (IDOR, tenant isolation).

## Limits
- Rate limit: 5 requests per second
- Login attempts per account: 5
- Allowed hours:
- Data that must never be modified:

## Focus and known issues
- Priority areas (auth, payments, uploads, admin, multi-tenancy, ...):
- Already known or accepted risks (do not re-report):

## Stop and contact
- Who to notify if something breaks or real data is exposed:
