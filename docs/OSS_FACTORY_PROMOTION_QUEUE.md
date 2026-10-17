<!-- oss-factory:v1
{"id":"20261017-civic-crisiscleanup-4-web-queue","kind":"state","project":"crisiscleanup-4-web","from":"chatgpt","to":["factory"],"status":"working","dedupe_key":"promotion-queue:CrisisCleanup/crisiscleanup-4-web","civ":{"city_id":"oss:crisiscleanup-4-web"}}
-->

# Canonical upstream promotion queue — CrisisCleanup/crisiscleanup-4-web

Tracked via registry PR https://github.com/kvnloo/oss-factory/pull/191 (provisional until merged). Fork Issues are disabled; this fork-local document is the **one canonical queue**. Original implementation PRs, issue threads, and author credit stay where they originated.

- Origin: https://github.com/CrisisCleanup/crisiscleanup-4-web
- Coordination fork: https://github.com/kvnloo/crisiscleanup-4-web
- Last evidence audit: 2026-10-17
- State: **ORIGIN_LIVE / CHECK** (not origin-action authorization)

## Existing upstream review / source work

- Origin PR: https://github.com/CrisisCleanup/crisiscleanup-4-web/pull/1387 (draft; no review comments).
- Requirement: https://github.com/CrisisCleanup/crisiscleanup-4-web/issues/1164 — failed queue removal must not show success.
- Source: `civic/phone-queue-error-toast-1164` @ `f3264b5ad9acd7b1f9728389e468618a69fffbef`.
- Change: catch rejected `completeCallsForPhoneNumber`; use existing `getErrorMessage` error toast; success only on resolved promise.
- CI: https://github.com/CrisisCleanup/crisiscleanup-4-web/actions/runs/36838683698 — `action_required`, **zero jobs**; not a passing test. Requested optional workflow approval once on the existing PR: https://github.com/CrisisCleanup/crisiscleanup-4-web/pull/1387#issuecomment-6243118760.
- Gate: targeted hook test for rejection/success, normal TypeScript tests/build, maintainers' CI approval; no parallel PR.
- Next: verify test harness and CI activation, update same PR rather than create duplicates.

## Release gates

- Record original author/reporter/maintainer provenance and exact source head SHA.
- Follow project contribution policy, current upstream reviews, conflicts, and CI checks.
- Require native targeted tests; separate static reasoning from exercised runtime evidence.
- Do not publish an overlapping origin PR or claim a fork draft is landed.
- Only a bounded human authorization under factory/HITL.md permits additional origin actions; upstream merges are for maintainers.

## Results

- **Ready for new origin publication:** none independently verified.
- **Origin writes from this coordination update:** none.
- **Next update:** when CI/reviews/test results or upstream ownership changes materially.
