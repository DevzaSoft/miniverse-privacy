
## Publisher correction — AdMob release target (9 November 2026)

**Supersedes any contrary release-plan statements above:** The publisher explicitly wants Google AdMob advertising **enabled in the released game** and reports having enabled it previously. Earlier review snapshots stating that Production AdMob/UMP is disabled are **not authorization to keep ads off** and must not be treated as the final product decision. The present Unity project, its actual runtime initialization and the final Release build have **not** been inspected in this document-only correction; their current enabled/disabled state remains unverified. The release plan is to restore/retain working AdMob ads, verify actual SDK data flows and implement applicable consent, disclosures and Play Console Data safety declarations. Do not make a unilateral decision to disable advertising. No Unity code, AdMob console configuration, Play Console settings or live legal pages were changed here. Existing contradictory snapshot wording is historical and requires cleanup in the next full editorial pass.
# 16P-rc1 — Unresolved document inputs and publication gates

**Status:** Internal completion register. The candidate documents remain unpublished and unapproved.

This register groups remaining placeholders so they can be resolved deliberately. Do not replace any item with an assumption.

## A. Publisher-supplied factual details

| Input | Current state | Required action |
|---|---|---|
| Establishment country | **Confirmed by owner: Türkiye (9 November 2026)** | Country-level fact is confirmed. |
| Publisher name | **Confirmed: DEVZASOFT is the publisher/display name, not a separate legal entity (9 November 2026)** | Documents now distinguish the publisher brand from the individual/natural-person provider/controller. Do not describe DEVZASOFT as an incorporated company. |
| Controller/provider identity evidence | Drafts currently identify the individual provider as Barışcan DEDEOĞLU | Confirm the exact spelling and legal identity against the owner's official records before publication. |
| Official business/notification address and formal privacy-request channel | Not established | Must be confirmed and legally reviewed; do not invent an address or imply support email automatically meets formal service requirements. |
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
- On 18 February 2026, the Board adopted Principle Decision 2026/347 requiring information notices and explicit-consent texts to be arranged separately. The Authority's 2026 announcement highlights misleading/blanket wording and failure to tailor notices to the controller's own processing. MiniVerse's notices must describe its verified app-specific data flows; generic vendor templates are not sufficient.
- The Article 9 international-transfer framework changed effective 1 June 2024. The actual transfer route must be determined from real recipients, roles, countries and contractual arrangements. If a standard contract is used, the Authority states that it must be notified within five business days after signature.
- The 30-day KVKK response wording in the candidate concerns the controller's response to a valid data-subject application under the applicable procedure; it is not a general data-retention period.

Official sources:
- [KVKK — Notice obligation](https://www.kvkk.gov.tr/Icerik/2033/Aydinlatma-Yukumlulugu-)
- [KVKK — Public announcement on fulfilling the notice obligation](https://www.kvkk.gov.tr/Icerik/6765/AYDINLATMA-YUKUMLULUGUNUN-YERINE-GETIRILMESI-HAKKINDA-KAMUOYU-DUYURUSU)
- [KVKK — International transfers / Article 9](https://www.kvkk.gov.tr/Icerik/2053/Yurtdisina-Aktarim)
- [KVKK — Statutory text and Article 5 processing conditions](https://www.aile.gov.tr/kvkk/mevzuat/)

These references explain the legal framework; they do not determine MiniVerse's purpose-specific legal grounds, establish that a transfer mechanism exists, or replace Turkish counsel's review.

## H. Publisher-provided contact details — 9 November 2026

- Publisher/display name: **DEVZASOFT**.
- Designated support and privacy/data-rights contact email: **devzasoft@gmail.com**.
- The email is included in the candidate documents as the publisher's contact/request channel.
- The email is not described as a physical address and is not represented as automatically satisfying every statutory formal-notice, service or KVKK application requirement.
- DEVZASOFT is not represented as a separate incorporated company or legal entity.
- The controller/provider legal identity and any legally required formal service details remain a publication gate. The publisher brand must not be substituted for the controller's legal identity where law requires disclosure of that identity.
## I. KVKK application channel clarified — 9 November 2026

- The owner-designated privacy contact email is **devzasoft@gmail.com** and is included in the TR/EN documents as the initial contact/request email.
- The official Turkish application methods under Article 13 and Article 5 of the Application Communiqué include written submission, KEP, secure electronic signature, mobile signature, an email address previously notified by the data subject and recorded in the controller's system, or an application developed for that purpose.
- Merely publishing the controller's Gmail contact does not mean every ordinary email from any user is automatically a formally valid KVKK application.
- The Communiqué's required application particulars include the applicant's name/surname, signature for written submissions, Turkish ID number or foreign applicant's nationality/passport/ID number, the applicant's address for notification, any notification email/phone/fax, and the subject of the request. The applicant's notification address is not the publisher's contact email.
- No controller postal address, KEP address or dedicated in-app rights-request workflow has been invented. If one is later established, documents and operational procedures must be updated together.

Official sources:
- [KVKK — Communiqué on application procedures (PDF)](https://www.kvkk.gov.tr/SharedFolderServer/CMSFiles/bf638c8f-7455-49a7-8118-3eb2858a16b5.pdf)
- [KVKK — Public announcement on procedural requirements for complaints](https://www.kvkk.gov.tr/Icerik/6938/Kurumumuza-Yapilan-Sikayetlerin-Usul-Sartlarina-Iliskin-Kamuoyu-Duyurusu)
- [KVKK — Article 10 notice obligation](https://www.kvkk.gov.tr/Icerik/2033/Aydinlatma-Yukumlulugu-)

This clarification is not a legal opinion and does not establish that the published Gmail address alone satisfies every formal statutory application or service requirement.

## J. On-device-first data model and Google Play Data safety release decision — 9 November 2026

**Owner clarification:** DEVZASOFT does not operate a player-account service, collect players' game saves to a developer backend or maintain a server-side database of player progress. Progress, stars, fuel and preferences are stored locally by the app. This is not the same as a verified statement that no data is transmitted by the final Android artifact.

### Data-flow matrix — do not convert assumptions into Play Console declarations

| Data flow | Current evidence/owner description | Owner/developer backend? | Remaining verification |
|---|---|---|---|
| Progress, stars, level completion, fuel, game preferences | Local application files; no developer-server upload identified in reviewed source | No developer backend identified | Verify release network behavior and Android backup/restore configuration |
| Android/Google OS backup and restore | Off-device copies may be created depending on OS/user configuration | Not a DEVZASOFT backend | Inspect backup flags, data-extraction rules and backup transport; avoid asserting that saves never leave the phone |
| Google AdMob advertising SDK | Present in project, but Production ad initialization/ad requests currently disabled | Google service when enabled, not DEVZASOFT's own server | Verify actual Release dependency, SDK initialization, outbound traffic, consent, identifiers, regional behavior, recipients and Play Data safety categories |
| Google UMP privacy SDK | Present in project, Production initialization disabled in reviewed configuration | Third-party component | Verify whether any SDK/native component transmits independently in final artifact; do not equate no ad request with no network activity |
| User-initiated support or rights email | User chooses to send an email to devzasoft@gmail.com | Accessible to publisher through email provider | Describe as voluntary support communication; check applicable retention and disclosure |
| External legal/privacy website | Opens in browser and may contact hosting/network providers | Not game-save upload to DEVZASOFT | Verify site cookies/analytics/network behavior separately |
| Google Play platform telemetry | May be processed by Google as platform operator | Not automatically developer-controlled | Distinguish Play platform processing from SDK transmissions embedded in the app and from any Play Console reports accessible to publisher |

### Release-specific verification steps

1. Freeze the exact APK/AAB build identifier and release dependency list; do not use Development APK results as evidence for Release.
2. Inspect the merged Android manifest for permissions, AD_ID, INTERNET, backup and data-extraction rules.
3. Review SDK initialization and actual outbound traffic on first launch, gameplay, Settings, legal-link opening, offline/online transitions and app restart, without collecting unnecessary user identifiers in the test log.
4. Check whether SDKs or OS services send data even with ad requests disabled; document observed domains, categories and purposes, noting limitations of TLS inspection.
5. Compare findings against current Google Play Data safety definitions, third-party SDK disclosure and Google's current SDK guidance. Record any required declarations for the **actual** released artifact.
6. If ads are enabled later, repeat the entire assessment including UMP consent lifecycle, age-related restrictions and regional policy settings.
7. Publish revised legal text and complete Play Console declarations only after the actual behavior is evidenced and the owner approves.

**Do not preselect** “No data collected” or “No data shared” solely because DEVZASOFT has no backend. Do not assert that Google is solely responsible for every SDK data flow. The actual app configuration, SDK behavior and applicable policy determine the publisher's declarations.

**Publication remains blocked** pending legal controller-identity review, final SDK/data-flow evidence, unresolved legal placeholders and owner approval. No live page, Unity file, advertising setting or Play Console form was changed during this documentation update.
