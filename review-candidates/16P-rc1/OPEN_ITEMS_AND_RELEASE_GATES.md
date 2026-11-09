# 16P-rc1 — Unresolved document inputs and publication gates

**Status:** Internal completion register. The candidate documents remain unpublished and unapproved.

This register groups remaining placeholders so they can be resolved deliberately. Do not replace any item with an assumption.

## A. Publisher-supplied factual details

| Input | Current state | Required action |
|---|---|---|
| Establishment country | **Confirmed by owner: Türkiye (9 November 2026)** | Country-level fact is confirmed. Exact registered legal name, business/notification address and any applicable trade-name details still require confirmation from official registration records. |
| Formal non-residential service/request address | Not established | Identify a lawful formal notice/request channel that does not expose a private residential address, if legally permissible. Obtain Turkish counsel review. |
| Formal privacy-request method | Not established | Confirm required submission fields, recipient, delivery method and identity/authority verification route. |
| Representative / not applicable | Not established | Confirm whether a representative is legally required or accurately mark not applicable after review. |
| Canonical TR/EN policy URLs | Candidate paths exist only in this review branch | Assign final public URLs only after approval and deployment. |
| Release document version and effective date | Not approved | Set only after final text approval and exact content hashes are fixed. |

## B. Technical evidence required before final disclosure

| Input | Why it remains open | Evidence needed |
|---|---|---|
| Actual recipient and processor register | Package names do not prove which legal entity receives each category or its role | Exact SDK/service inventory, contracts and provider terms; identify entity, role, purpose and data categories. |
| Transfer countries and mechanisms | Cannot infer data residency from a vendor brand or UMP choice | Provider configuration/contracts and counsel's KVKK Articles 8/9 and, where applicable, GDPR transfer assessment. |
| Provider retention periods | Generic Google retention pages do not establish this app's exact record lifetimes | Provider-specific terms/settings and available account controls. |
| Local technical-record schedule | Size caps/rotation are not time-based retention periods | Define purpose, owner, target period and deletion method for receipts, backups, traces and corrupt copies. |
| Final Release data flow | Development APK evidence is not equivalent to final Release behavior | Inspect final AAB/APK merged manifest, permissions, SDK versions, initialization order, backup rules and network payloads. |
| Production ad/UMP behavior | Currently disabled; future behavior is not yet established | Before activation, verify exact AdMob/UMP configuration, consent lifecycle, ad sources/mediation, identifiers and regional behavior. |

## C. Legal determinations requiring qualified review

| Input | Required determination |
|---|---|
| KVKK legal grounds | Determine a concrete Article 5 basis separately for each purpose; do not default every purpose to consent or legitimate interest. |
| Domestic and international transfers | Determine actual recipient roles, applicable Article 8/9 mechanism and any GDPR safeguard that applies. |
| 16–17-year-old users | Review contractual capacity, consumer protection, privacy and advertising requirements in target jurisdictions. Do not describe all 16+ users as adults. |
| Consumer / liability clauses | Review mandatory warranty, consumer, liability and refund requirements; do not insert blanket waivers. |
| Governing law and disputes | Determine appropriate law, venue and dispute language without limiting mandatory consumer rights. |
| Licence and intellectual property | Confirm the app's actual third-party asset/code licences and scope of end-user licence. |
| Language precedence | Determine how TR/EN differences are resolved without reducing mandatory local rights. |
| Rights-request retention | Define a proportionate period and access controls for request evidence. |
| Support retention exception | Ordinary support email is retained for 12 months after resolution; define and document any specific legal/dispute exception rather than retaining indefinitely. |

## D. Product facts already fixed for this candidate

- Intended audience is 16+; the game is not designed for children.
- No age or date-of-birth collection, age verification, age classification, age-category persistence or age-based ad routing in the current active flow.
- The 16+ statement does not technically block under-16 access.
- Users aged 16–17 may still be minors under local law.
- Production AdMob/UMP initialization and ad requests remain disabled.
- Privacy Policy notice, Terms acceptance and UMP privacy choices are separate.
- No user account or account-deletion feature is represented as existing.
- Ordinary support email correspondence is retained for 12 months after the issue is resolved, subject to a separately documented specific legal/dispute exception.

## E. Publication gates

Do not publish or connect these documents to the app until all applicable items below are complete:

1. Owner confirms factual publisher/contact details.
2. Qualified Turkish counsel reviews KVKK, consumer, minors, transfer and contract provisions.
3. Technical team verifies the exact release artifact, merged manifest, SDK/dependency tree, backup behavior and actual network flows.
4. All placeholders in the eight Markdown source documents are resolved or explicitly marked not applicable with a defensible reason.
5. TR and EN texts are compared for equivalent meaning.
6. HTML mirrors are regenerated from the approved Markdown source and checked for links, language tags, accessibility and deployed routing.
7. Owner approves the exact version and effective date.
8. Canonical public URLs and exact content hashes are recorded in the app's legal-release configuration.
9. Physical-device acceptance flow and end-to-end return to the game are tested.
10. Continue remains disabled until the approved Terms source and exact URL/hash mapping are verified.

## F. Explicitly out of scope for this document-only pass

No Unity code, onboarding behavior, acceptance configuration, APK/AAB, Play Console declaration, production ad configuration, live root policy page or production deployment is changed by this register.

## G. Verified Turkish regulatory guidance incorporated into the review

The following official guidance has been checked and is reflected in the TR/EN KVKK candidates:

- KVKK Article 10 notice must cover controller identity, processing purposes, recipient groups and transfer purposes, collection method/legal grounds, and data-subject rights.
- The Authority's public announcement warns against combining the information notice with explicit consent or requiring a checkbox confirming that the notice was read as a condition of service. Product implementation should keep Privacy/KVKK links informational, Terms acceptance a separate affirmative action, and UMP privacy choices separate.
- The Article 9 international-transfer framework changed effective 1 June 2024. The actual transfer route must be determined from real recipients, roles, countries and contractual arrangements. If a standard contract is used, the Authority states that it must be notified within five business days after signature.
- The 30-day KVKK response wording in the candidate concerns the controller's response to a valid data-subject application under the applicable procedure; it is not a general data-retention period.

Official sources:
- [KVKK — Notice obligation](https://www.kvkk.gov.tr/Icerik/2033/Aydinlatma-Yukumlulugu-)
- [KVKK — Public announcement on fulfilling the notice obligation](https://www.kvkk.gov.tr/Icerik/6765/AYDINLATMA-YUKUMLULUGUNUN-YERINE-GETIRILMESI-HAKKINDA-KAMUOYU-DUYURUSU)
- [KVKK — International transfers / Article 9](https://www.kvkk.gov.tr/Icerik/2053/Yurtdisina-Aktarim)
- [KVKK — Statutory text and Article 5 processing conditions](https://www.aile.gov.tr/kvkk/mevzuat/)

These references explain the legal framework; they do not determine MiniVerse's purpose-specific legal grounds, establish that a transfer mechanism exists, or replace Turkish counsel's review.
