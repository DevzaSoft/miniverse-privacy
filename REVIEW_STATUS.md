# MiniVerse Privacy Website — Review Branch Report

Date: 2026-11-07
Repository: https://github.com/DevzaSoft/miniverse-privacy
Branch: legal-site-review

## Changes prepared
- Rebuilt `index.html` as a bilingual document hub with links to each review document.
- Added `terms-tr.html` and `terms-en.html` as Terms of Use review candidates.
- Added `kvkk-tr.html` as a Turkish KVKK disclosure review candidate.
- Added `data-deletion-tr.html` as a data-request information page candidate.
- Updated `privacy-tr.html` and `privacy-en.html` with the owner-confirmed individual developer identity and the owner's stated general-audience intent.
- Updated `styles.css` with responsive document cards and consistent DEVZASOFT branding.

## Owner-confirmed details
- Data controller / individual developer: Barışcan DEDEOĞLU (owner-approved for publication in review drafts).
- Brand: DEVZASOFT
- Contact: devzasoft@gmail.com
- App: MiniVerse Road Puzzle
- Package: com.devzasoft.miniverseroadpuzzle

## Important limitations
These files are review candidates only. They are not legal advice, lawyer-approved documents, or publication approval.

The following must be verified before final publication:
1. Postal/service address is intentionally not published at the owner's request; verify whether the proposed contact and application procedure meets applicable requirements.
2. Correct KVKK legal basis for each processing purpose and category.
3. Actual recipients, processors, international transfer destinations and valid transfer mechanism(s).
4. Retention and deletion periods for local game data, Google Mobile Ads/UMP data, logs and hosting.
5. Current Android manifest, SDK versions, actual network/data behavior and Android backup/restore behavior.
6. Google Play Data safety and target-audience declarations against the actual release build.
7. Target countries, applicable consumer law, governing law and dispute provisions.
8. Final legal review by a qualified Turkish privacy/consumer-law professional.
9. Effective dates and version numbers after all above are settled.

Owner decision updated on 8 November 2026: the app is intended for a general family audience including children, teens and adults. This supersedes the earlier general-audience / not-child-directed wording and the 13+ wording in older 21D candidates. Exact Play Console age bands still require a product suitability decision. The classification under each country's child-directed / mixed-audience laws must be assessed from actual product presentation, marketing, audience and data flows; it is not resolved merely by this owner statement.

## Deployment status
- Changes were committed only to `legal-site-review`.
- The `main` branch was not modified.
- GitHub Pages deployment was not triggered or verified.
- The public URL https://devzasoft.github.io/miniverse-privacy/ could not be verified in this session.
- No existing public content was replaced.

## Next step
Owner review of the candidate texts, then qualified legal review and completion of the unresolved factual items. Only after explicit owner approval should changes be merged to `main` and GitHub Pages deployment verified.

## Owner audience decision update — 8 November 2026

The owner confirmed that young children (under 13), teens and adults are all intentionally targeted with equal priority. This supersedes “general family audience” as the operative detailed audience decision and supersedes all earlier 18+ / 13+ draft wording. Public-facing review candidates on this branch have been updated to reflect this decision. Exact Play Console age bands remain open because “young children” does not yet establish whether age 5 and under (toddlers/preschoolers) are included.

COPPA classification is not automatically settled by the phrase “equal priority.” FTC distinguishes child-directed services, mixed-audience child-directed services (where under-13s are not the primary audience), and general-audience services. Review product visuals, toy-city/cartoon presentation, activities, incentives, audio, store listing, marketing and actual/likely audience. Obtain qualified US legal review before enabling data collection/ads to under-13 users. Production ad serving remains disabled.



## Final owner age-band decision — 8 November 2026

The owner has explicitly excluded children aged 5 and under from the intended audience. The target groups are 6–8, 9–12, 13–15, 16–17 and 18 and over, with children aged 6–12, teens and adults intended with equal priority. This resolves the earlier open question about toddlers/preschoolers. The app remains child-inclusive because ages 6–12 are intentionally targeted; Families and child-privacy requirements therefore remain applicable. This decision does not authorize production ads, merge to main, or final publication.


## KVKK Article 10 / Article 5 / Article 9 follow-up — 8 November 2026

- Added a visible draft / not approved for publication banner to `kvkk-tr.html` and `kvkk-en.html`.
- Clarified the observed collection channels in both notices: local in-app records, automatic third-party SDK collection/transmission, user-initiated support email, and possible automatic hosting/network logs on policy-page visits. Final fields and providers still require technical/contract verification.
- Added a purpose-by-purpose Article 5 decision register and Article 9 transfer evidence checklist to `LEGAL-REVIEW-TR-EN.md`. These are explicitly work registers, not legal conclusions. No legal ground, recipient country, standard contract or transfer safeguard has been invented or declared complete.
- Official KVKK guidance confirms that Article 10 notices must identify the controller/representative, purposes, recipient groups and transfer purposes, collection method, legal ground, and data-subject rights; the legal ground must identify the applicable Article 5/6 condition. Sources are linked in the legal review document.
- Current state remains BLOCKED for final publication, merge to `main`, production ads and Play submission approval pending actual provider/contract/configuration evidence and qualified Turkish counsel review.


## Support/privacy mailbox confirmation — 8 November 2026

The owner confirmed direct consumer Gmail use of `devzasoft@gmail.com` for support and privacy correspondence, with no forwarding. The TR/EN KVKK drafts now identify consumer Gmail and do not misclassify Google as the developer's processor for this email flow. Google's official policy says consumer Gmail has no DPA and Google does not act as processor for the consumer service: https://support.google.com/policies/answer/9581826. Exact Google legal entity, processing countries, independent-controller purposes and any Article 9 transfer mechanism remain to be verified; no destination country or safeguard has been invented. The review also records the KVKK application-method distinction: email is a prescribed method when sent from an email address previously notified to and registered in the controller's system; other statutory methods remain available. See the official application procedure: https://kvkk.gov.tr/SharedFolderServer/CMSFiles/0517c528-a43d-49f5-b1eb-33dc666cb938.pdf.


## Support mailbox security confirmation — 8 November 2026

The owner confirmed two-step verification is enabled on `devzasoft@gmail.com`. The KVKK TR/EN drafts now state this specific control, without claiming that all account-security settings or the complete security programme have been audited. Remaining mailbox review: recovery methods, active sessions, connected apps, forwarding/filter rules and access permissions.


## AdMob country and official-source check — 8 November 2026

The owner confirmed the AdMob publisher account country is Türkiye. Official Google signup guidance says this selection cannot later be changed, but it does not imply data is stored/processed only in Türkiye. Google's publisher-suite roles are feature-specific: Google and publisher are independent controllers for the publisher products generally, while Google acts as processor for some specific features. Google's privacy documentation states that data may be processed on servers outside the user's country. KVKK Article 9 transfer rules (effective 1 June 2024) require an applicable legal transfer route; standard contracts require Authority notification within five business days of signature. No contract, destination country or transfer safeguard is assumed to exist. Official references: https://support.google.com/admob/answer/7356219?hl=en ; https://support.google.com/admob/answer/7666366?hl=en ; https://policies.google.com/privacy/frameworks?hl=en ; https://www.kvkk.gov.tr/Icerik/6649/Personal-Data-Protection-Law ; https://www.kvkk.gov.tr/Icerik/2053/Yurtdisina-Aktarim.

AdMob restricted data processing is not a universal KVKK solution and does not disable mediation or automatically cover data sent to mediation partners: https://support.google.com/admob/answer/14125907?hl=en. Next evidence: account approval/verification status, app/package association, enabled products/features, mediation partners and accepted publisher terms. Publication remains blocked.


## AdMob account approval recorded — app readiness still separate — 8 November 2026

The owner reports that the DEVZASOFT AdMob account is approved and ready. This does not prove that MiniVerse: Road Puzzle has separately passed AdMob app readiness review or app-ads.txt verification. Google's current guidance says each new app must be linked to a supported app store and reviewed; check the exact app row in AdMob > Apps > View all apps. “Ready” is the app-level state that indicates readiness to serve ads. Sources: https://support.google.com/admob/answer/10564477?hl=en and https://support.google.com/admob/answer/14538460?hl=en. The owner must provide only the app-level status label and app-ads.txt verification status, if shown. Project production ads remain disabled until child-audience, SDK, consent, legal-transfer and technical checks are completed.


## AdMob app readiness screenshot recorded — 8 November 2026

Owner screenshot shows Android app status “İnceleme gerekli” (Requires review), “Sınırlı reklam sunumu” (Limited ad serving), store action “Mağaza ekle” (Add store), no store/package identity linked (—), and three active ad units. This is app-level status, not account status. Google requires a publicly available app in a supported store, linked in AdMob, before readiness review. Private Play apps cannot be linked. After linking, review generally takes 2–3 days but may take longer. New AdMob apps set up since January 2025 require app-ads.txt verification when prompted; after the file is found, owner must trigger Verify app / Check for updates. Official references: https://support.google.com/admob/answer/10564477?hl=en ; https://support.google.com/admob/answer/9989980?hl=en ; https://support.google.com/admob/answer/14538460?hl=en.

Do not fabricate a store listing or app-ads.txt seller record. Wait for public Google Play availability, link the exact package/listing, set up app-ads.txt from the exact AdMob seller details, verify it, then confirm app status becomes Ready. Three active ad units do not prove approval. Production ads remain disabled pending app readiness and separate child-privacy/legal checks.


## Release sequencing clarification — owner is intentionally pre-publication — 8 November 2026

The owner clarified that MiniVerse: Road Puzzle has not yet been published because the final preparation stages are still in progress and the owner is waiting for those stages to be completed before the first Google Play release. This is intentional and is not a current defect or an overdue owner action. The AdMob screenshot's missing store link / “Add store” / “Requires review” / limited ad serving state is therefore expected before public release.

**Correct sequence:** (1) finish legal notices and verify actual technical/data flows; (2) complete the game release candidate, store listing, privacy-policy URL, Data safety declaration, target audience and Families compliance; (3) prepare app-ads.txt using the exact seller record from AdMob and publish it on the developer website if required; (4) owner approves the final release and publishes the app publicly to Google Play; (5) only after the public listing is available, link the exact Play listing/package in AdMob; (6) complete app-ads.txt verification and AdMob app-readiness review; (7) enable production ads only after app status is “Ready” and child-audience, consent, SDK, transfer and legal checks have passed.

Do not ask the owner to publish early just to clear AdMob's app-review status. Do not treat the current pre-publication AdMob state as a failure. The publisher account itself is owner-confirmed approved; the app-level review necessarily waits until the public store listing exists. Production ads remain disabled until all gates are complete.


## Public-document consistency pass — 8 November 2026

- Removed unsupported claim of a mandatory in-app Terms acceptance screen from TR/EN Terms; now describe terms without asserting an unverified UI.
- Added parent/guardian review wording for minors while preserving mandatory rights.
- Identified direct consumer Gmail provider in TR/EN Privacy Policy and Data Access/Deletion pages; distinguished Gmail from AdMob/UMP feature-specific roles and avoided describing consumer Gmail as the developer's processor.
- Kept legacy data-deletion-tr.html unlinked and noindex; canonical public index links paired TR/EN data-access-deletion pages.
- Retention schedule, actual first-launch UX, Article 5/9 legal grounds/transfers and qualified legal review remain unresolved. Production ads and publication remain blocked.


## Owner retention decision — 8 November 2026

Ordinary support emails are to be retained for 12 months after the relevant support request is resolved, then developer-controlled copies must be deleted or genuinely anonymised. This period does not automatically apply to separate KVKK/data-subject requests, ongoing disputes, statutory retention duties or records strictly necessary for legal claims; these are assessed separately and retained only while necessary. The TR/EN Privacy Policy, KVKK Notice and Data Access/Deletion pages were updated consistently. Operational implementation in Gmail (resolution date marking and periodic deletion review) remains to be confirmed; Gmail does not automatically implement this custom retention rule.


## First-launch legal acceptance gate issue — 8 November 2026

Owner confirmed the first-launch screen displays Terms of Use and Privacy Policy and is intended to require an “I agree” action before proceeding. However, the “I agree” button is currently passive/disabled and cannot be clicked. Therefore the acceptance gate is currently non-functional; do not claim that acceptance is captured or that users have accepted the Terms. This is a release blocker requiring a Unity UI fix and verification across clean install, update, returning install, offline state, screen sizes and TR/EN. Keep Terms acceptance separate from UMP advertising/privacy consent and do not claim that Privacy Policy display itself is consent.


## Owner advertising-network choice — 8 November 2026

The owner chose Google AdMob only; no third-party ad networks or mediation partners are planned. Record this as the intended plan only. Actual Unity dependencies, Gradle tree, Android merged manifest, Plugins/Android libraries, AdMob mediation groups/ad sources/custom events and final Release AAB must still be checked to prove no other network SDK/adapter is included or enabled. If any is present, update data-flow/recipient disclosures, Families SDK eligibility, contracts/transfers and Data Safety. AdMob-only does not remove child-directed/unknown-age safeguards, UMP requirements, or KVKK Article 9 review. Production ads remain disabled until all gates pass.


## Ad safety workstream — current Google Families requirements — 8 November 2026

Because the owner-selected target audience includes both children aged 6–12 and older groups, Google Play mixed-audience requirements apply. A neutral age screen is required to ensure ads not suitable for children are shown only to older users; it must not encourage users to claim an older age. For children and unknown-age users, only Families Self-Certified Ads SDK versions may serve ads, with no interest-based ads or remarketing, child-appropriate creatives and compliant ad formats. Google AdMob Android SDK `play-services-ads` 19.0.0+ is currently listed as self-certified; exact final dependency must be verified. Unity SDK age treatment uses `AgeRestrictedTreatment.Child/Teen/Unspecified`, replacing deprecated TFCD/TFUA. Child/unknown-age requests should use child treatment and G maximum ad content rating. UMP is not an age screen. Official sources: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en ; https://support.google.com/googleplay/android-developer/answer/9893335?hl=en ; https://support.google.com/googleplay/android-developer/answer/12955712?hl=en ; https://developers.google.com/admob/unity/targeting ; https://support.google.com/admob/answer/6223431?hl=en.

Age-screen presence and ad routing in the current Unity build have not yet been confirmed. No production ads until verified. Next step: inspect whether the app currently asks for age/date of birth before any ad SDK initialization or request.


## Age-selection flow confirmed — Settings only — 8 November 2026

Owner confirms MiniVerse age selection currently exists only in Settings. There is no first-launch age/date-of-birth screen before ads. This is not a verified neutral age screen for Google Play mixed-audience ad routing. Release blocker: do not enable production ads or rely on the Settings value to serve older-audience ads. Implement and test a neutral first-launch age screen before any ad SDK initialization/request, or keep ads disabled for all users. UMP is not age screening. Unknown/invalid/skipped age must remain on child-safe/no-personalised-ad path; if safe handling is not implemented, do not initialize/request ads. Google guidance: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en.


## Product decision recorded — no first-launch age screen — 8 November 2026

Owner explicitly chose to keep age selection only in Settings and declined adding a first-launch age/date-of-birth screen. This is a product preference, not evidence of mixed-audience ad-policy compliance. The Settings selector cannot be represented as a neutral age screen or used to serve older-audience ads. With a 6+ mixed audience, keep Mobile Ads SDK initialization and production ad requests disabled for all users unless a qualified, policy-compliant alternative is confirmed. Do not silently change the target audience declaration. Revisit only with the owner's approval.


## Ad strategy policy correction — 8 November 2026

Correction: serving G-rated, non-personalised/contextual ads to every user does not by itself remove Google Play's neutral age-screen requirement for mixed-audience apps. Official Families policy expressly requires age-screening measures where the declared audience includes both children and older users, plus certified ad SDKs and child-appropriate ads. Owner still declines first-launch age screen and wants age selection in Settings. Respect that choice; do not implement without approval, but keep production ads disabled until a compliant alternative is verified or product/target-audience decision is explicitly changed. Never misdeclare the audience. The prior suggestion that child-safe ads alone may solve the requirement is superseded. Sources: https://support.google.com/googleplay/android-developer/answer/9893335?hl=en ; https://support.google.com/admob/answer/6223431?hl=en ; https://support.google.com/admob/answer/10477886?hl=en.


## Product decision updated — neutral age screen approved — 8 November 2026

Owner now approves adding a neutral age question to the first-launch flow. This supersedes prior Settings-only decision. Place before main menu and before AdMob SDK initialization/ad requests. Prefer neutral date-of-birth entry; do not steer toward older ages. Retain only minimal age classification where possible; full DOB must not be sent to AdMob/analytics without necessity and legal basis. Under-6 handling must be defined because declared target is 6+ (5 and under excluded). UMP is separate; age entry is not consent. Child/unknown users require child-safe ad treatment, Families-certified SDK and G content cap if served; if safe routing fails, do not request ads. Unity code has not yet been changed; release remains blocked pending implementation and QA.


## Stage 12 status received from owner — partial PASS, not full PASS — 8 November 2026

Owner reports implementation of neutral DOB entry, under-6 block and minimal age-category persistence; full DOB is not saved; ad/UMP entry points are blocked until age resolution; Terms and consent remain separate. Automated checks: 279/279 offline, 11/11 isolated persistence, three build profiles passed; 34 APK and Production settings preserved. Full PASS withheld pending Unity PlayMode/visual and Android startup testing. The reported local summary is `C:/UnityProjects/MiniVerseRoadPuzzleV1/Artifacts/MiniVerseV1/Stage12NeutralAgeGate/SUMMARY.md`; not independently inspected.

Current TR/EN legal docs already state 6–12, 13–17 and 18+ target groups, excluding 5 and under (not 13+ only). However, Privacy Policy/KVKK/Data Access pages still say the app does not ask for age or collect DOB; these factual statements must be revised after runtime verification. Next: inspect summary and rollback, finish PlayMode/UI/Android startup tests, prove no ad/UMP init or network before age resolution, check data minimization across logs/analytics/crash/cloud, and fix/test known disabled Terms acceptance button. Production ads and publication remain blocked.


## Stage 12 status update — Unity QA passed; Android/native/privacy gates remain blocked — 8 November 2026

Owner-reported Unity QA: 29/29 PASS, zero Console errors, seven real screenshots reviewed. Age 6, under-6 block, invalid/future DOB, persistence reload and Settings category passed. Terms Continue remains disabled/passive as expected and is a separate release blocker. 34 APK files preserved; Stage 13 not started.

Stage 12 remains partial PASS because Android clean-install, native SDK startup order and comprehensive DOB leakage checks remain BLOCKED. Owner supplied local report path `C:/UnityProjects/MiniVerseRoadPuzzleV1/Artifacts/MiniVerseV1/Stage12NeutralAgeGate/Validation/LATEST_RESULTS.md` (not independently inspected). Next gates: physical Android clean install, confirm no AdMob/UMP init or network before age resolution, comprehensive DOB scan in logs/logcat/analytics/crash/local/cloud/network, and repair/test Terms acceptance. Production ads remain disabled; do not publish or start Stage 13.


## Android build/signing failure — Stage 12 remains partial PASS — 8 November 2026

Owner reports one Android build failed during signing with `UnityException: Can not sign the application`; no APK was created and install/Android tests remain BLOCKED. Device identified: 24090RA29C, Android 15/API 35. 34/34 protected APKs preserved, no data deleted, no retry started. Stage 13 not started.

Next local action is inspection only: Unity Publishing Settings keystore path/readability, selected alias, and current-session keystore/key password fields. Do not share credentials or commit secrets. No retry until explicit owner approval plus fresh preflight and rollback checkpoint. After successful signing, verify APK signature/package identity before install. AdMob/UMP startup order and comprehensive DOB leakage checks remain unverified. Production ads remain disabled and app unpublished.


## Owner explicitly approves one Android APK retry after preflight — 8 November 2026

The owner explicitly approved one further Android APK build attempt, conditional on completing a fresh preflight first. This is approval for one controlled retry only; it does not authorise repeated retries, keystore regeneration/replacement, deletion of the 34 protected APKs, publication, production ad activation or Stage 13. Before building, verify the current project/branch and rollback checkpoint, preserve and count all 34 protected APKs, confirm keystore file exists/readable, selected alias exists, signing identity/package ID/build profile are unchanged, credentials are entered locally in Unity's secure fields (never logged or shared), and output path is new/non-overwriting. If any preflight check fails, STOP and report BLOCKED without building. If all pass, perform exactly one build attempt. On success, verify APK exists, package ID/version, signing certificate fingerprint matches the existing intended release identity, and artifact hash; only then install on Xiaomi 24090RA29C / Android 15 API 35. If signing fails again, stop immediately; do not retry automatically. Stage 12 remains partial PASS until Android runtime, native SDK ordering and DOB leakage tests pass. Production ads stay disabled; do not publish or start Stage 13.


## Android retry successful — update install only — 8 November 2026

Owner reports the single authorised build succeeded and signature matched the prior verified certificate. Package `com.devzasoft.miniverseroadpuzzle`, version `0.1.0` / code `1`; SHA-256 `EC2CB2F6EA4E5760E5A71DF18CE8FA518F83BE4AC45A54C8EDAA2C995FC65DE0`. In-place update installed without data loss. 34/34 protected APKs unchanged; production ads disabled. Clean-install and Android runtime tests remain BLOCKED. Do not uninstall or clear data on the user's primary phone; use a disposable test device/emulator or isolated test identity. Verify the reported APK and hash, inspect ControlledBuildRetry/SUMMARY.md, then test fresh install, age-gate flow, native AdMob/UMP initialization ordering and DOB leakage. No more builds without separate approval. Stage 12 partial PASS; Stage 13 not started; app not published.


## Stage 12.1 status — unified onboarding automated tests passed; owner approval pending — 8 November 2026

Owner reports single onboarding panel with language, unselected age list, legal links and separate Terms checkbox; DOB fields removed. Unity QA 51/51 PASS, Console 0 errors, offline 294/294 PASS, persistence 16/16 PASS, C# builds 4/4 PASS. 34/34 protected APKs unchanged. No APK/Resolve; production ads disabled.

BLOCKED: approved Terms version, canonical URL and content hash are missing; Continue remains disabled. Real pointer/touch and post-acceptance end-to-end tests not complete. Next verify authoritative Terms and Privacy URLs/version/hash, run touch and full acceptance flow tests, confirm explicit acceptance record and returning-user navigation. Do not infer/fabricate legal URLs or hashes. Age picker requires separate Google Play Families policy review. No build, ads, publish or Stage 13 until evidence is complete and owner approves.


## Stage 12.1 latest validation — pointer simulation passed; full approval withheld — 8 November 2026

Owner reports Unity EventSystem pointer QA 53/53 PASS and zero Console errors. Turkish/English language selection, age selection, document open/return and disabled Terms/Continue checks passed in simulation. Not physical touchscreen evidence. 34 APKs preserved; no build/Resolve; Stage 13 not started.

FAIL: TR/EN Privacy Policy/KVKK still describes no age selection/verification and no DOB collection; now stale because onboarding asks for a self-declared age and stores age category. Update after verifying actual data fields and persistence. Acceptance record lacks verified document content hash and language evidence. Record exact Terms version, canonical URL/hash, displayed language, effective date and timestamp only after explicit user acceptance; do not treat Privacy Policy viewing as consent.

BLOCKED: authoritative Terms version/canonical URL/hash and verified deployed Privacy URLs/content; physical Android touch; successful acceptance-to-main-menu E2E. Continue must remain disabled while authoritative Terms source is unavailable. Self-selected age list is not automatically confirmed as a Google Play neutral age screen; policy review remains necessary before advertising. Production ads disabled. No build, Resolve, publication or Stage 13. Full Stage 12.1 PASS is not approved.


## Stage 12.1 latest report — legal text and acceptance evidence updated; approval withheld — 8 November 2026

Owner reports TR/EN Privacy/KVKK/data access/deletion documents corrected and acceptance record linked to Terms version, URL, two hashes, language, effective date and explicit user action. Automated results: 335/335 offline, 24/24 persistence, 3/3 C# builds; 34/34 APKs preserved. No build/Resolve/publication; Stage 13 not started.

Gaps: secure age correction UI missing despite being described in legal disclosures; implement or correct disclosures. Device time is not independent verification; record its source honestly. BLOCKED: approved Terms configuration absent, Continue disabled, current Unity QA, physical touch and acceptance-to-menu E2E pending, and age-list Google Play policy status unresolved. Production ads disabled. Full Stage 12.1 PASS not granted.
