# 16P-rc1 Editorial and HTML Mirror QA

**Review date:** 9 November 2026  
**Status:** Candidate package consistency checks completed. Not legal approval, not owner publication approval, not live-page verification.

## Scope

Reviewed the eight Markdown candidate sources and their eight HTML review mirrors under `review-candidates/16P-rc1/`.

## Results

| Check | Result |
|---|---:|
| Markdown source files present | 8/8 |
| HTML review mirrors present | 8/8 |
| TR/EN HTML language attributes | 8/8 correct |
| HTML noindex/nofollow markers | 8/8 |
| Explicit review-only banners | 8/8 |
| HTML navigation links to all eight documents | 8/8 |
| Adjacent duplicate Markdown section headings | 0 |
| Stale current-audience claims (0–12, 6+, 13+, mixed/child-only) in candidate body scan | 0 |
| Live/public root pages changed | 0 |
| Production deployment/publish actions | 0 |

## Source structure corrections

- Removed duplicate/obsolete headings in Terms, KVKK, Data Retention and Privacy Policy sources.
- Rebuilt HTML mirrors from the corrected Markdown sources.
- Standardized navigation so every HTML candidate links to all eight TR/EN documents.
- Retained `noindex,nofollow` and a visible review-only banner on every HTML candidate.
- Kept the definitive 16+ intended-audience statement and the caveat that this does not verify age or block under-16 access.
- Kept the 12-month retention statement only for ordinary support email correspondence after resolution; other record classes remain separately unresolved.

## Remaining placeholders

Placeholders are intentionally retained because the required facts or legal determinations are not established by the repository evidence.

| Document pair | Remaining placeholders per language |
|---|---:|
| Privacy Policy TR/EN | 20 |
| Terms TR/EN | 11 |
| KVKK notice TR/EN | 22 |
| Data Retention / Rights Procedure TR/EN | 9 |

Key unresolved categories include establishment/service address or lawful service channel, formal rights-request method, purpose-specific legal grounds, recipient/controller/processor roles, transfer countries and mechanisms, rights-request/provider/local-record retention, licence/IP scope, consumer/liability provisions, governing law/disputes, language precedence, final version and effective date.

## Important limitations

- These are repository-level editorial and structure checks, not legal review.
- HTML mirrors are review-only and are not canonical public URLs.
- No live HTTPS content or deployment branch was changed or verified by this pass.
- No legal basis, recipient, transfer safeguard, retention period beyond the owner's 12-month support-email decision, approval, signature, effective date or canonical URL was invented.
- No Unity configuration, Terms acceptance binding, Continue gate, Production advertising setting, APK/AAB, Play Console declaration or game save was changed.

## Current product facts carried into candidates

- Intended audience: 16+; the game is not designed for children.
- No age/DOB collection, age verification, age classification, age-category persistence or age-based ad routing in the current active flow.
- Intended audience is not age verification; access by under-16 users is not technically blocked.
- Users aged 16–17 may remain minors under applicable law.
- Production AdMob/UMP initialization and ad requests remain disabled.
- Privacy Policy notice, Terms acceptance and UMP privacy choices remain separate.
