# MiniVerse: Road Puzzle — Legal & Google Play Pre-publication Review
**Review date:** 8 November 2026  
**Scope:** Eight TR/EN policy files on `legal-site-review`, known application behavior summarized in the project review, current Google Play policy pages, Google Mobile Ads Unity Plugin disclosure, and official Turkish DPA (KVKK) guidance.  
**Status:** PRE-PUBLICATION REVIEW — NOT LEGAL APPROVAL, NOT READY TO PUBLISH.

## Executive result

The eight documents are coherent as a first factual draft, but the package is **not ready for production publication**. The KVKK Article 10 notice identifies unresolved mandatory disclosure inputs. The public Privacy Policy also depends on the exact Release AAB/merged manifest, final SDK versions, live ad configuration, actual Play Console target-audience declaration, provider contracts, and the deployed HTTPS pages.

Do not merge this review branch into the production/default branch, publish the pages, or treat the documents as legally approved until the blocking items below are resolved.

## 1. Findings by document

| Document | Review result | Required follow-up |
|---|---|---|
| `privacy-tr.html` / `privacy-en.html` | Factually cautious draft. Correctly distinguishes local game saves, optional rewarded ads, UMP choices, third-party SDK data, and lack of in-app accounts. | Reconcile exact Release SDK versions and Data safety declaration; confirm actual providers/recipient entities and destinations; confirm the app's declared target audience; update the “Production ads disabled” statement whenever that changes. |
| `kvkk-tr.html` / `kvkk-en.html` | **Not publishable as a final Article 10 notice yet.** Purpose-specific legal grounds, actual recipients/countries, transfer mechanism, representative details (if any), and request-verification procedure remain unresolved. | Complete every item in Section 3 below using signed contracts, actual configuration and qualified Turkish privacy counsel review. Do not replace missing facts with generic “consent” or “legitimate interest” wording. |
| `terms-tr.html` / `terms-en.html` | Broadly consistent with a single-player puzzle, local saves, no account, no IAP/subscription and optional rewarded ads. | Verify the in-app acceptance screen links to the correct language/version; verify accepted version/hash and UTC timestamp; have Turkish counsel review licence, liability, governing-law and consumer clauses. |
| `data-access-deletion-tr.html` / `data-access-deletion-en.html` | Properly avoids promising a non-existent account-deletion feature or remote deletion of device/provider copies. | Verify Reset Settings behavior against the current build. Keep preference reset, Android “clear app data”, uninstall, UMP choices and a formal data-subject request distinct. |

## 2. Google Play publication requirements

Google Play's User Data policy requires every app to provide a comprehensive privacy policy linked in Play Console and accessible from inside the app. The page must be app-specific, publicly accessible worldwide, HTTPS, non-geofenced, non-PDF and non-editable. It must identify the developer/app and privacy contact, explain data access/collection/use/sharing, security, retention and deletion. The Data safety form must match actual app and SDK behavior.

Sources:
- Google Play User Data policy: https://support.google.com/googleplay/android-developer/answer/10144311
- Prepare your app for review: https://support.google.com/googleplay/android-developer/answer/9859455

**Required release checks**
1. Open every final TR/EN URL in a logged-out browser and verify HTTPS, no login, no geoblocking, correct language, no 404/redirect loop, and mobile layout.
2. Verify the app exposes the privacy policy link in-app and Play Console points to the same canonical policy.
3. Complete the Data safety form against the final Release AAB, including third-party SDK collection/sharing and any backup behavior.
4. Re-check the form and policy whenever SDK versions, ad settings, permissions, adapters, mediation, analytics or data flows change.
5. The game has no user accounts in the reviewed behavior. Google Play's account-deletion flow is therefore not represented as an existing feature. If account creation is introduced later, the in-app and external account-deletion requirements must be implemented before release.

## 3. Blocking KVKK Article 10 inputs

KVKK's official guidance requires the controller and representative identity (if any), processing purposes, recipient groups and transfer purposes, collection method and legal grounds, and Article 11 rights. Purpose and legal ground are separate disclosures; vague generic privacy wording is not a substitute for an activity-specific notice.

Official sources:
- KVKK — Aydınlatma Yükümlülüğü: https://www.kvkk.gov.tr/Icerik/2033/Aydinlatma-Yukumlulugu-
- KVKK — fulfilment of the notice obligation: https://www.kvkk.gov.tr/Icerik/6765/AYDINLATMA-YUKUMLULUGUNUN-YERINE-GETIRILMESI-HAKKINDA-KAMUOYU-DUYURUSU
- KVKK — notice regulation: https://www.kvkk.gov.tr/Icerik/4132/aydinlatma-yukumlulugunun-yerine-getirilmesinde-uyulacak-usul-ve-esaslar-hakkinda-teblig

Resolve and document:

1. **Purpose-specific legal grounds:** local game save/preferences; reward receipt/fraud prevention; UMP privacy choices; Google Mobile Ads processing; support emails; data-subject requests; policy-site server logs. Identify the actual Article 5 condition for each activity and its necessity. Do not presume consent or legitimate interest.
2. **Actual recipient entities and roles:** identify legal entities behind exact Google products/features, email provider, website host/CDN and any other SDK/adapter. Distinguish controller, processor and independent controller roles based on actual contracts and service configuration.
3. **Actual destination countries:** establish where each relevant data flow is received/processed, from provider terms, data-processing terms and account configuration. A domain, debug geography, provider headquarters or generic Google policy is not proof of destination country.
4. **International-transfer mechanism:** if personal data is transferred abroad, identify the actual applicable KVKK Article 9 route and retain supporting agreement/decision/approval and records. Do not state that a standard contract or another safeguard exists until signed and applicable.
5. **Standard-contract notification:** where a KVKK standard contract is used, KVKK states it must be notified to the Authority within five business days after signature. Retain proof of timely notification. Source: https://www.kvkk.gov.tr/Icerik/8043/Standart-Sozlesme-Bildirim-Modulu-Hakkinda-Kamuoyu-Duyurusu
6. **Controller/representative details:** confirm whether a representative is legally applicable; if so, identify them. Confirm public contact details and a practical, secure rights-request verification process.
7. **Retention schedule:** set and document an operational retention rule for support/privacy emails and controller-held records. For local saves, describe the user-controlled lifecycle and any actual automatic cleanup. Do not invent provider retention periods.

Until these facts are confirmed, the current KVKK files should remain explicitly marked as drafts and must not be presented as a completed Article 10 notice.

## 4. Google Mobile Ads / UMP factual checks

Google's current Google Mobile Ads Unity Plugin disclosure says the SDK automatically collects and shares IP address, user product interactions, diagnostic information and device/account identifiers for advertising, analytics and fraud prevention; the page also says data is encrypted in transit using TLS. It describes Android Advertising ID as optional, while App Set ID and other identifiers may still be relevant. The disclosure is version-sensitive and Google says the developer remains responsible for the Play Data safety answers.

Source: https://developers.google.com/ad-manager/mobile-ads-sdk/unity/privacy/play-data-disclosure

**Before release:**
- Inspect the final Release AAB's merged manifest, permissions, SDK/plugin version, mediation adapters and native dependencies.
- Confirm whether AD_ID is present and whether App Set ID or other identifiers are used. Absence of AD_ID alone does not prove no identifiers are processed.
- Confirm exact ad unit IDs and production/test profile. If live ads are enabled, remove or update any statement that says Production ads are disabled.
- Confirm UMP geography, consent messages, privacy-options entry point, and behavior when the user declines, closes the form, is offline, or receives an SDK error.
- Verify that no consent error is treated as consent and that the game does not unnecessarily block core gameplay on personalized-ad consent.
- Capture a final release test report and use it to reconcile the policy and Play Data safety form.

## 5. Target audience and child-directed access

The current documents state that the app's primary commercial/design audience is 18+, while acknowledging that the app has no age check and may be generally accessible. This is not a technical age restriction.

Google Play requires developers to declare actual target age group(s). If children are included in the target audience, additional Families requirements apply, including relevant advertising SDK/ads requirements. Policy wording alone cannot establish the Play Console declaration.

Source: https://support.google.com/googleplay/android-developer/answer/9867159

**Owner decision required:** confirm the actual intended target age group and exact Play Console target-audience declaration. Do not keep “18+” merely as convenient wording if product design, store listing, creative assets or marketing actually target children/teens.

## 6. Terms and in-app acceptance

Before production:
- Confirm the app presents both Turkish and English Terms links as appropriate.
- Confirm the accepted version and document hash correspond to exact published content.
- Confirm UTC acceptance timestamp is stored only after a real acceptance action.
- Confirm the startup gate remains closed if required Terms configuration, language links, document contents or hashes are missing.
- Confirm no UMP action is recorded as Terms acceptance and no Terms acceptance is treated as advertising consent.
- Have Turkish counsel review consumer, licence, liability, termination and governing-law wording.

## 7. Bilingual parity and document QA

The TR/EN versions have matching subject matter and intended obligations. Before publishing, run a content-level comparison after legal edits, not only an HTML syntax check. Keep the same document version and effective date in both languages. Confirm all cross-links and mailto subjects resolve.

## 8. Release gate

**Current status: BLOCKED — do not publish or merge to production yet.**

A release candidate may be approved only after:
- [ ] Product owner confirms target age and Play Console declaration.
- [ ] Final Release AAB/manifest/SDK/ad configuration has been inspected.
- [ ] Google Play Data safety answers match the inspected release build.
- [ ] Actual provider legal entities, roles, destinations and contracts are documented.
- [ ] Purpose-specific KVKK Article 5 grounds and Article 9 transfer route are confirmed.
- [ ] KVKK notice and TR/EN translations are completed and reviewed by qualified Turkish counsel.
- [ ] Terms acceptance/version/hash behavior is verified in the release build.
- [ ] All eight public HTTPS pages are deployed and tested worldwide.
- [ ] In-app links and Play Console URLs point to the correct language pages.

## 9. Review limitations

This is a product/policy consistency and public-source review, not a legal opinion or attorney-client advice. The review did not inspect the final Release AAB, live provider contracts, Play Console declarations, deployed website, actual network payloads, or the developer's complete data-processing records. Findings about those items are intentionally marked as requiring verification rather than assumed facts.

## 10. Owner decision: general family audience (8 November 2026)

The product owner has confirmed that MiniVerse: Road Puzzle is intended for a **general family audience**, including children, teens and adults. The previous “18+ primary audience” wording was inconsistent with this decision and has been removed from the TR/EN Privacy Policy and Terms, and the family-audience context has been added to the KVKK and data-access/deletion documents.

Official Google Play guidance:
- Target audience and content: https://support.google.com/googleplay/android-developer/answer/9867159
- Families Policy: https://support.google.com/googleplay/android-developer/answer/9893335
- Families Self-Certified Ads SDK Program: https://support.google.com/googleplay/android-developer/answer/9900633

**Policy consequences for this app:**
1. In Play Console, declare only the age bands for which the game is genuinely designed and appropriate. “General family audience” does not justify selecting every age band automatically; the owner must confirm suitability of the youngest groups against gameplay, art, store listing, marketing and monetisation.
2. Because the app is a mixed audience, Google Play Families requirements apply if any selected target group includes children. Ads shown to children and users of unknown age must use eligible Families Self-Certified Ads SDK versions and must not use interest-based/personalised advertising or remarketing.
3. A neutral age screen is an accepted age-screening measure for mixed-audience ad delivery. UMP privacy messaging is not a neutral age screen and must not be described as one. For child/unknown-age ad requests, Google's AdMob guidance also requires child-directed age treatment and a maximum ad content rating of G; verify the current Unity API equivalent and apply it consistently to every relevant ad request.

4. The reviewed legal text says the app does not ask for age or collect date of birth. No neutral age-screen implementation has been established by the reviewed materials. Therefore, ad serving to children or users of unknown age is a **release blocker** until a compliant age-screen/ad-routing implementation is verified.
5. The reviewed configuration says Production ad serving is disabled and demo ad units are for development/testing. Keep live ad serving disabled until the exact Google Mobile Ads SDK/plugin version and every mediation adapter are checked against the current Families Self-Certified Ads SDK list and the release build's child-directed/non-personalised request behavior is tested.
6. A child-accessible app must be assessed under applicable child privacy and advertising law in every distribution market. Do not claim parental consent or age assurance merely because UMP is present.


**SDK version cross-check (not final-build verification):** The prior 21D technical candidate records Google Mobile Ads Unity Plugin 11.6.0 and Android Google Mobile Ads SDK 25.5.0. The current Google Play self-certified list retrieved on 8 November 2026 lists Google AdMob Android SDK 19.0.0 or later. The recorded Android SDK version is therefore above the listed minimum, which is encouraging, but the final Release AAB, exact resolved dependency, any mediation/adapters and current list entry still must be checked. Do not treat the Unity wrapper version number as the Android SDK version. Source: https://support.google.com/googleplay/android-developer/answer/12955712

**Remaining owner/product decision:** the broad family-audience decision is recorded, but the exact Google Play age bands remain unconfirmed. Select them only after reviewing the game and store presentation for age appropriateness. If the youngest child groups are not actually intended, do not select them just to increase reach.

## 11. Updated publication gate

The release remains **BLOCKED — do not publish/enable production ads yet**. In addition to Section 8, require:
- [ ] Exact target age bands in Play Console are selected and match the product, store listing and marketing.
- [ ] Neutral age-screen behavior is implemented and verified for a mixed audience before child/unknown-age ad requests.
- [ ] Every advertising SDK and mediation adapter version is verified against Google's current Families Self-Certified Ads SDK list.
- [ ] Child-directed treatment and non-personalised ad behavior are verified for child/unknown-age users; no interest-based ads or remarketing are served to them.
- [ ] Test evidence covers child, adult and unknown-age paths, UMP unavailable/error paths, offline behavior and rewarded-ad completion.
- [ ] The Data safety form and privacy notices match the tested Release AAB and actual enabled services.


## 12. Child privacy and international market review

The owner has confirmed a general family audience including children, teens and adults. This does not by itself settle whether the game is “directed to children” under every jurisdiction's law. That classification can depend on the game's subject matter, visual presentation, characters, music, incentives, store listing, advertising and evidence of intended/actual audience.

- **United States:** FTC COPPA applies to online services directed to children under 13 that collect/use/disclose children's personal information, and to general-audience services with actual knowledge of such collection. FTC guidance treats persistent identifiers and third-party ad-network collection as potentially relevant. Its “mixed audience” category is a subset of child-directed services, not a synonym for every service used by children. A qualified US privacy review is required before distribution/ads to US children. Source: https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions
- **European Economic Area:** GDPR Article 8 digital-consent thresholds for information-society services offered directly to children vary by Member State within the GDPR framework. Do not use a single pan-EU age threshold in the global policy; map the actual launch countries and any guardian-consent flow. Source: https://commission.europa.eu/law/law-topic/data-protection/information-business-and-organisations/legal-grounds-processing-data/are-there-any-specific-safeguards-data-about-children_en
- **Türkiye:** KVKK's digital-games symposium materials highlight the importance of child/teen data protection and age assurance, while noting that Turkish legislation does not currently set a GDPR-style uniform digital-consent age in the same way. This is not a substitute for a case-specific Turkish legal assessment. Source: https://www.kvkk.gov.tr/Icerik/8289/Dijital-Oyunlar-ve-Kisisel-Verilerin-Korunmasi-Sempozyumu
- **Worldwide distribution:** the repository notes a worldwide release intention. A market-by-market matrix is required for child privacy, consumer protection, ad restrictions, data transfers and parental authority. If this cannot be completed before launch, restrict launch markets rather than claiming universal compliance.

## 13. Legacy age-category data correction

The prior 21D technical review notes that a legacy age-category file from an earlier version may be read for safety; new date-of-birth input is not collected. The public TR/EN Privacy Policy, KVKK notice and data-access/deletion pages have been updated to distinguish these facts. A legacy age category is not reliable age verification and is not parental permission. Its actual lifecycle, backup copies and deletion behavior still need confirmation against the final release build.


## 14. Repository / change-control note

The current review branch is substantially ahead of `main`. Draft PR #1 (`legal-site-review` → `main`) reports 22 changed files and 78 commits, including pre-existing review candidates and older technical/legal documents. It is marked Draft and GitHub reports it is not mergeable at this time. Do not merge PR #1 as a whole without a file-by-file review and conflict reconciliation. The public website deployment source/settings were not accessible through the available repository actions; the standard GitHub Pages URL could not be verified. Do not assume the branch is or is not live based only on its name.

## 15. Owner's final audience decision — equal priority (8 November 2026)

The owner has now explicitly confirmed: **young children, teens and adults are all intended target groups with equal priority**. This supersedes the earlier broad “general family audience” description as the operative product decision. The legal documents in this branch have been revised to say that the app intentionally targets young children (under 13), teens and adults equally. The previous 18+ and 13+ statements must not be reused.

### Google Play declaration
Google Play requires selecting each age band for which the app is genuinely designed and appropriate. Its current age-band choices must be checked in Play Console. The owner has confirmed under-13 children are included, but has not specified whether the game is suitable for the “5 and under” group (including toddlers/preschoolers), or only older children within under-13. Do not select “5 and under” without a separate suitability decision. At minimum, evaluate the child bands (5 and under, 6–8, 9–12), teen bands (13–15, 16–17) and adults (18+) individually against actual gameplay, reading requirements, motor demands, visual/audio content, store listing and marketing. Select only those genuinely supported. Source: https://support.google.com/googleplay/android-developer/answer/9867159

### COPPA — important classification distinction
The owner's equal-priority statement establishes that under-13 children are deliberately targeted; it is not a general-audience app merely used by some children. However, it does not alone resolve whether the service is “child-directed” and, if so, whether it qualifies for COPPA's narrower “mixed audience” treatment. FTC considers the totality of factors, including subject matter, visual presentation, characters, child-oriented activities/incentives, music/audio, language, marketing and actual audience evidence. “Mixed audience” is a subset of child-directed services where under-13 children are not the primary audience; it is not interchangeable with “general audience.” Equal priority across children, teens and adults may support an argument that under-13 children are not the primary audience, but the product presentation and actual/likely audience must be reviewed by qualified US counsel. Sources: https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions and https://www.ecfr.gov/current/title-16/chapter-I/subchapter-C/part-312

### Age-screening consequences
- Google Play mixed target groups (children plus older users) require an appropriate neutral age-screening measure before ads intended only for older audiences can be shown; children and users of unknown age must receive compliant Families ad treatment.
- Under COPPA, an age screen is not a universal solution for every child-directed service. FTC guidance permits age-screening in the narrower mixed-audience subcategory where children are not the primary audience, and the operator must not collect personal information from users who identify as under 13 unless COPPA notice/verified parental consent or a valid exception applies.
- If US counsel concludes under-13 children are the primary audience, do not rely on an age screen to treat other visitors as adults; apply COPPA protections to all visitors as required and obtain verifiable parental consent before covered collection unless a specific exception applies.
- Do not collect date of birth or other personal information before any legally appropriate age-screening step. Current app has no age-screen implementation established by the reviewed materials.

### AdMob / Families implementation gate
Production ads remain disabled. For every ad request from a child or unknown-age user, use the Google Mobile Ads SDK child-directed age treatment (tagForChildDirectedTreatment / current Unity API equivalent) and set maximum ad content rating to G. Use only current Families Self-Certified Ads SDK versions and compliant mediation adapters. Do not serve interest-based ads or remarketing to children or unknown-age users. Google's guidance: https://support.google.com/admob/answer/6223431 and https://support.google.com/googleplay/android-developer/answer/9893335

### Remaining audience-specific product question
The owner's “young children” decision does not identify whether toddlers/preschoolers (age 5 and under) are included. This affects the Play Console band, reading/accessibility expectations and suitability review. Keep the age-band declaration unresolved until the owner explicitly confirms this point and the game is assessed.

### Release status
**BLOCKED — no production advertising and no final publication/Play submission approval.** Required evidence: exact Play age-band decision; US COPPA child-directed/mixed-audience legal classification; EU member-state digital-consent matrix; Turkish child-data/KVKK assessment; neutral age-screen design where legally permitted; no-data-before-screen verification; parental notice/consent or documented exception where required; child/unknown/adult ad-routing tests; current SDK/adapter certification; final Release AAB/Data Safety alignment.


## 16. Final owner decision: exclude ages 5 and under (8 November 2026)

The owner has confirmed that children aged 5 and under are not part of the intended audience. The target groups are 6–8, 9–12, 13–15, 16–17 and 18 and over, with children aged 6–12, teens and adults intended with equal priority. This resolves the prior open question about toddlers/preschoolers. Do not select the Play Console “5 and under” band. The app still intentionally targets children aged 6–12, so Google Play Families and applicable child-privacy requirements remain relevant. This decision does not establish that any particular age-suitability, COPPA classification, age-screening, SDK, advertising, KVKK or international-transfer requirement has been satisfied. Production ads and final publication remain blocked pending the evidence and legal review described above.


## 17. Article 10 collection-method audit and Article 5 mapping status — 8 November 2026

The Turkish and English KVKK notice drafts now identify the observed collection channels at a high level: (i) automatic local app records created during gameplay; (ii) automatic data collection/transmission by Google Mobile Ads/UMP components, depending on configuration; (iii) user-initiated support email; and (iv) possible automatic hosting/network security logs when the policy page is visited. The notice explicitly remains a draft and says the final fields/methods must be verified against the final Release AAB, provider agreements and hosting configuration.

### Purpose-by-purpose Article 5 decision register (NOT a legal conclusion)

| Activity / purpose | Data currently described | Article 5 position | Evidence needed before a legal ground can be stated |
|---|---|---|---|
| Local gameplay saves and preferences | Progress, stars, moves, fuel/renewal, settings | UNRESOLVED. First establish whether/how the developer determines and processes identifiable personal data where records remain only on-device. Do not automatically label as contract necessity. | Final build data-flow review; Terms relationship; whether any IDs/telemetry leave device; local backup behavior. |
| Reward receipt and duplicate-reward prevention | Local reward/transaction receipt; ad completion signals | UNRESOLVED. Contract necessity and/or legitimate-interest necessity may be assessed by counsel only after necessity and balancing are documented. | Exact reward flow; receipt fields/lifetime; whether server-side verification or SDK callback only; fraud risk and less intrusive alternatives. |
| UMP privacy choices | User choices and SDK technical records | UNRESOLVED. Separate the user's consent/choice for the underlying ad processing from the legal basis for storing/using the consent record and any provider-side processing. | Exact UMP message types, regions, consent strings/records, SDK roles, account configuration and provider terms. |
| Google Mobile Ads processing | IP address, interactions, diagnostics, device/account identifiers as described in Google's disclosure | UNRESOLVED for the developer's role; Google may act in different roles depending on product/feature. Do not assert one blanket legal ground or assume UMP consent covers all SDK processing. | Exact plugin/native SDK and adapter versions; enabled features; AdMob account/product terms; Google controller/processor role per feature; final AAB and Data safety mapping. |
| Support correspondence | Sender email, message, attachments | UNRESOLVED. Assess separately the basis for answering a user-initiated request, any pre-contractual/contractual context, legal claims and statutory obligations. | Confirm mailbox provider and legal entity; access/forwarding; categories of messages; retention/deletion procedure. |
| KVKK/data-subject requests | Identity/contact details and request contents supplied by applicant | UNRESOLVED pending counsel mapping. Legal-obligation basis may be relevant to statutory response duties, but scope and retention must be limited to what is necessary. | Actual request workflow; identity verification method; access controls; response log fields and retention schedule. |
| Policy-site security logs | Potential IP, timestamp, user-agent/device and request logs | UNRESOLVED. Assess whether the developer receives or controls these logs and the necessity/proportionality of any security processing. | Confirm Pages/hosting/CDN provider, logging features, actual fields, retention, access and provider roles. |

KVKK Article 10 requires a clear legal ground for each relevant processing activity, and the Authority's guidance says the legal ground must identify the applicable condition in Articles 5 or 6; purpose and legal ground are distinct disclosures. Therefore the table above is a work register only and must not be copied into the public notice as a completed legal-basis statement. Official references: https://www.kvkk.gov.tr/Icerik/2033/Aydinlatma-Yukumlulugu- and https://www.kvkk.gov.tr/Icerik/4132/aydinlatma-yukumlulugunun-yerine-getirilmesinde-uyulacak-usul-ve-esaslar-hakkinda-teblig.

### Article 9 transfer decision register

No transfer mechanism is asserted. For each actual overseas recipient, first identify the exporter/importer legal entities, destination country, role, data, purpose and whether the flow is a transfer under KVKK. Then check an applicable adequacy decision or an appropriate safeguard under Article 9; if relying on a standard contract, verify the correct template, signatures and notification to the Authority within five business days. The Authority also publishes reminders about signature authority, Turkish text, dates, supporting documents and the five-business-day notification. Official references: https://www.kvkk.gov.tr/Icerik/2053/Yurtdisina-Aktarim, https://www.kvkk.gov.tr/Icerik/8043/Standart-Sozlesme-Bildirim-Modulu-Hakkinda-Kamuoyu-Duyurusu and https://www.kvkk.gov.tr/Icerik/8170/Yurt-Disina-Kisisel-Veri-Aktariminda-Kullanilacak-Standart-Sozlesmelerde-Dikkat-Edilmesi-Gereken-Hususlara-Iliskin-Kamuoyu-Duyurusu.

**Status:** Article 5 grounds and Article 9 mechanisms remain BLOCKED pending evidence and qualified Turkish counsel review. No public legal notice should imply they are settled.


## 18. Support/privacy mailbox confirmed: consumer Gmail — 8 November 2026

The owner confirmed that `devzasoft@gmail.com` is used directly as a Gmail account for support and privacy correspondence; it is not forwarded to another mail server. The KVKK TR/EN drafts now identify the provider as Google's consumer Gmail service and distinguish the developer's handling of incoming messages from Google's own service role.

**Important contractual distinction:** Google's official policy states that Google does not offer a Data Processing Agreement for consumer Gmail/Drive and does not act as a data processor for the consumer versions. A Google Workspace or Google Cloud service may have a Cloud Data Processing Addendum, but that is not the service the owner has described. Do not identify Google as the developer's processor for the consumer Gmail email flow, and do not claim that a consumer Gmail DPA or Workspace CDPA is in place. Official source: https://support.google.com/policies/answer/9581826

**Transfer and role limitation:** This does not by itself establish the exact Google legal entity, storage/processing countries, applicable international-transfer mechanism, or all independent-controller purposes. Those must be verified from the consumer Gmail account's applicable terms, privacy documentation, actual service configuration and qualified Turkish counsel. No country or KVKK Article 9 safeguard is assumed.

**Operational retention:** the developer should retain support/request emails only while necessary for the request and applicable legal obligations, then delete copies under the developer's control. Google's own system retention/deletion is governed by Google's service terms and policies; no Google retention period is represented as known here. The owner should confirm that account security, recovery options, two-step verification and access are restricted to authorised persons.

**KVKK application channel:** a plain email from any arbitrary address is not automatically a formally valid Article 11/13 application in every case. The official application procedure allows email where the applicant uses an email address previously notified to and registered in the controller's system; other statutory methods include written application, KEP, secure electronic signature and mobile signature. Requests must be handled with proportionate identity/authority verification and statutory content requirements. Official source: https://kvkk.gov.tr/SharedFolderServer/CMSFiles/0517c528-a43d-49f5-b1eb-33dc666cb938.pdf


## 19. Support mailbox security control confirmed — 8 November 2026

The owner confirmed that two-step verification (2-Step Verification) is enabled on the direct consumer Gmail account `devzasoft@gmail.com`, used for support and privacy correspondence. The TR/EN KVKK notices now state this narrow, verified control and recommend restricting mailbox-content access to the authorised developer account. This fact does not prove that recovery channels, app passwords, forwarding rules, connected third-party apps, device sessions, backup codes or all other account-security settings have been reviewed. It is not a claim that all data processing is secure or that a formal information-security programme exists. Before release, review recovery methods, active sessions, connected apps, forwarding/filter rules and access permissions; do not share passwords or verification codes.


## 20. Google Mobile Ads / AdMob role and data-disclosure review — 8 November 2026

Official Google documentation currently says the latest Google Mobile Ads Unity Plugin disclosure (the page identifies version 25.5.0) automatically collects/shares IP address, user product interactions (including app launches, taps and video views), diagnostic information, and device/account identifiers (including Android advertising ID and App Set ID, and in some cases other signed-in account identifiers) for advertising, analytics and fraud prevention. Google says this SDK-collected data is encrypted in transit with TLS. Android advertising ID collection is optional and can be prevented through manifest configuration; that does not prove other identifiers are absent. The developer remains responsible for the Play Data safety answers. Source: https://developers.google.com/ad-manager/mobile-ads-sdk/unity/privacy/play-data-disclosure.

Google's publisher guidance also states that Google acts as a data processor for **some** features in Ad Manager, Ad Exchange and AdMob, processing on publishers' behalf and instructions for those features. This must not be generalized to every AdMob product, feature, data flow or legal relationship. Google's privacy/terms resources separately identify Ads Controller Terms and Ads Processor Terms, and service eligibility varies. Source: https://support.google.com/admob/answer/7666366?hl=en-GB and https://business.safety.google/gdpr/.

**Current conclusion:** the public KVKK draft must not label Google globally as either controller or processor for all AdMob/UMP activity. Before the final notice, identify (a) the exact AdMob products/features actually enabled; (b) whether UMP, mediation, reporting, measurement or other optional features are used; (c) the applicable Google publisher terms and controller/processor terms accepted in the AdMob account; (d) exact Google contracting entity; and (e) actual destination countries and Article 9 transfer route. Product-level role and transfer analysis is required. No signed terms, destination countries, SCCs/standard contracts or transfer mechanism are assumed from generic public documentation.

**Technical disclosure limit:** the public SDK disclosure is a useful baseline, not proof of the user's installed plugin/native dependency. The earlier technical candidate notes GMA Unity Plugin 11.6.0 and Android GMA SDK 25.5.0; these are not confirmed against the final Release AAB. Inspect the exact dependency resolution, manifest, AD_ID permission, mediation adapters and enabled SDK features before updating Data safety and the final public notice.


## 21. AdMob account existence confirmed — 8 November 2026

The owner confirmed that a Google AdMob account exists for DEVZASOFT. This confirms account existence only. It does not establish account verification/approval status, accepted publisher terms, account country, linked app/package, active ad units, enabled products/features, mediation, consent configuration, production ad serving, or the contracting Google entity. Do not infer any of these from account existence.

**Next evidence to collect from the owner/AdMob UI (no passwords, verification codes, payment details or personal identifiers):** (1) account status (approved / under review / action required); (2) publisher account country shown in AdMob; (3) whether MiniVerse: Road Puzzle is added and its Android package name; (4) whether only Google demand is used or mediation/other networks are enabled; (5) whether the account's Policy / Terms section shows publisher terms accepted and which product terms are listed; (6) whether production ad units exist and whether they remain disabled/not integrated in the release build. Capture only non-sensitive status/product labels. The exact applicable publisher/controller/processor terms and destination countries must be verified from the account's accepted agreements and current Google documentation before completing the KVKK notice.

**Publication status remains BLOCKED.** An AdMob account alone does not prove that production ads are enabled or that the data flows/transfer mechanism have been established.


## 22. AdMob publisher terms and account-country verification — 8 November 2026

Official Google AdMob documentation states that the publisher suite (including AdMob) generally treats Google and the publisher as independent controllers for personal data in the publisher products, while Google is a processor for certain specific features. This is feature-dependent; the exact account contract and enabled feature terms must be checked rather than assuming one role for every flow. Sources: https://support.google.com/admob/answer/7666366?hl=en and https://business.safety.google/gdpr/.

Google's AdMob signup guidance says the publisher selects their country/territory during signup and that this selection cannot later be changed. Google also says the account must be verified and payment details completed before it is approved to serve ads. The account's selected country is therefore a necessary evidence item for identifying applicable publisher terms, account status and relevant contractual details, but it does not itself prove where end-user data is stored or processed. Source: https://support.google.com/admob/answer/7356219?hl=en.

Google's AdMob Terms of Service page states that use of the Google Mobile Ads SDK is subject to the terms governing use of AdMob; the page was last updated 23 October 2026. Source: https://developers.google.com/admob/terms.

**Owner confirmation received:** a DEVZASOFT AdMob account exists. **Still unknown:** selected account country, account approval/verification status, exact accepted terms and product-specific terms, app/package association, ad unit status, mediation and enabled features. Ask the owner to provide only the country/territory displayed in AdMob account settings; do not request postal address, tax ID, bank details, publisher ID, login, passwords or verification codes.


## 23. AdMob publisher account country confirmed: Türkiye — 8 November 2026

The owner confirmed that the DEVZASOFT AdMob publisher account country/territory is Türkiye. This is an account-country fact only. It does not establish that all Google processing or storage occurs in Türkiye, does not identify all recipient Google legal entities or destination countries, and does not by itself establish a KVKK Article 9 transfer mechanism. The country selection is relevant to the publisher account's contractual context and payments/tax configuration, but no tax or payment details are collected in this review.

**Next AdMob evidence:** confirm the account's approval/verification status; whether MiniVerse: Road Puzzle is added and the exact Android package name; whether mediation/third-party ad networks are enabled; whether production ad units exist and are integrated; and which publisher/product terms are shown as accepted. The owner should provide only non-sensitive status and product labels, not publisher ID, address, tax ID, bank/payment details, passwords or verification codes.

**Legal conclusion remains open:** assess each enabled Google product/feature's controller/processor role and each actual recipient/transfer route independently. A Türkiye publisher account does not prove Türkiye-only processing. Do not name a transfer country, Google legal entity, adequacy decision, standard contract or other Article 9 safeguard without account terms and technical/provider evidence.


## 24. Official-source cross-check after Türkiye account-country confirmation — 8 November 2026

- Google AdMob signup documentation says the publisher selects the country/territory where they currently live and cannot change that selection later; account verification/payment details are required before approval to serve ads. This supports recording the owner's Türkiye account-country answer, but does not establish data residency. Source: https://support.google.com/admob/answer/7356219?hl=en.
- Google's publisher documentation says Google and the publisher are independent controllers across the publisher suite, while Google is processor for some specific AdMob/Ad Manager/Ad Exchange features. The role is product/feature-dependent; the applicable terms and enabled feature settings must be inspected. Source: https://support.google.com/admob/answer/7666366?hl=en.
- Google says information may be processed on servers outside the country where the user lives. Therefore a Türkiye publisher account cannot be described as Türkiye-only processing or as proof that no cross-border transfer occurs. Source: https://policies.google.com/privacy/frameworks?hl=en.
- KVKK Article 9 was amended effective 1 June 2024. The Authority's current page describes adequacy decisions and appropriate safeguards including standard contracts; a standard contract must be notified to the Authority within five business days after signature. This does not mean a standard contract with Google exists. Sources: https://www.kvkk.gov.tr/Icerik/6649/Personal-Data-Protection-Law and https://www.kvkk.gov.tr/Icerik/2053/Yurtdisina-Aktarim.
- Google's AdMob restricted data processing (RDP) is a limited setting for certain applicable privacy-law contexts and does not turn off mediation or automatically cover data sent to mediation partners. It must not be presented as a universal KVKK solution or a substitute for Article 9 transfer compliance. Source: https://support.google.com/admob/answer/14125907?hl=en.

**Next evidence still needed:** account approval/verification status; MiniVerse app/package association; enabled products/features; mediation partners; accepted publisher terms; actual transfer recipients/countries and transfer mechanism. Account country Türkiye is recorded, but final legal conclusions remain blocked.


## 25. Owner confirms AdMob account approved — distinguish account from app readiness — 8 November 2026

The owner confirmed that the DEVZASOFT AdMob account is approved and described it as ready to serve ads. Record this as the owner's report about the **account**. Do not infer that MiniVerse: Road Puzzle itself has completed its separate app-readiness review, app-ads.txt verification (if required), policy checks, or that live ad units are integrated/serving.

Google's current AdMob Help says each new app must be linked to a supported app store and pass its own app-readiness review before it can fully serve ads. The app-level status is visible in AdMob > Apps > View all apps; “Ready” means the app is ready to serve ads, while “Getting ready”, “Requires review”, or “Needs attention” are not equivalent. Source: https://support.google.com/admob/answer/10564477?hl=en.

Google also says newly created apps may require app-ads.txt verification before approval/readiness, starting January 2025 for new apps where prompted. Source: https://support.google.com/admob/answer/14538460?hl=en.

**Next owner evidence:** inspect only the MiniVerse: Road Puzzle row in AdMob > Apps > View all apps and report its exact status label (Ready / Getting ready / Requires review / Needs attention / Request review). Do not share publisher ID, ad unit IDs, package private keys, payment details, address, tax data, password or verification codes. Also note whether the app's app-ads.txt section says verified, if present. Until this app-level status is confirmed, production ads remain disabled in the project and no claim is made that this specific app is cleared to serve live ads.


## 26. AdMob app-level screenshot evidence — 8 November 2026

The owner supplied an AdMob “All apps” screenshot for the Android app “MiniVerse Road …”. The visible row shows: approval status “İnceleme gerekli” (Requires review); status details “Sınırlı reklam sunumu” with instruction “Limiti kaldırmak için mağaza ekleyin” (Limited ad serving; add a store to remove the limit); store column “Mağaza ekle” (Add store); package/store identity column is “—”; and three active ad units. The screenshot also shows an app-ads.txt setup link at the top. This is direct visual evidence that the app has not yet been linked to a supported store and is not yet approved for full ad serving. It is distinct from the already owner-confirmed approved AdMob publisher account.

Google's official readiness guidance says the app must be publicly published, available to users in a supported store, and linked to that store in AdMob before the review can begin. Private Google Play apps cannot be linked. Once linked, review begins automatically; typical timing is 2–3 days but can take longer. Status “Requires review” means the app has not yet been reviewed and must be linked to a supported store. Sources: https://support.google.com/admob/answer/10564477?hl=en and https://support.google.com/admob/answer/9989980?hl=en.

Google's app-ads.txt guidance says new apps set up in AdMob from January 2025 require app-ads.txt verification when prompted; after publishing the file and AdMob finding it, the owner must return to the app and use Verify app / Check for updates. The app cannot fully serve ads until verification and app readiness approval are complete. Source: https://support.google.com/admob/answer/14538460?hl=en.

**Release gate:** do not attempt to link an unpublished/private Play Console app or invent a store URL. First publish the app publicly to Google Play (or another supported store) and ensure the store listing is available to users. Then use AdMob > Apps > View all apps > Add store to link the exact public listing/package. Next, set up app-ads.txt using the exact seller record AdMob provides, place it at the root of the developer website domain, ensure that domain is discoverable from the Play listing's developer website/contact details as required by Google's setup flow, verify app-ads.txt in AdMob, and request/check app verification. Do not publish an app-ads.txt file with a guessed publisher ID or seller record.

The three active ad units shown in the screenshot do not mean the app is approved or that production ads are currently serving. Keep production ad requests disabled until the app is publicly listed, store-linked, app-ads.txt verified if required, app readiness status is “Ready”, and the separate child-audience/privacy/SDK/legal gates are complete.


## 27. Public terms/privacy/deletion consistency pass — 8 November 2026

The TR/EN Terms of Use no longer claim that an in-app acceptance step is presented, because the current evidence does not establish that such a UI exists. The revised wording describes the terms, asks minors to involve a parent/legal guardian, and preserves mandatory rights. Before publication, compare this wording with the actual first-launch UX and obtain legal review of minor contract capacity/guardian requirements in target jurisdictions.

The TR/EN Privacy Policies now identify direct consumer Gmail for support/privacy correspondence and distinguish it from AdMob/UMP feature-specific Google roles. They state Google's published position that consumer Gmail has no DPA and Google does not act as processor for that consumer service; no Workspace contract is implied. The TR/EN Data Access and Deletion pages now use the same provider description and distinguish developer-controlled mailbox copies from Google's own system retention/deletion.

The old data-deletion-tr.html file remains an unlinked noindex legacy review candidate; the public index links only to the current paired TR/EN data-access-deletion pages. Do not link or publish the legacy file as the canonical page.

Retention remains a substantive open item: local game records have no timed auto-purge identified; Gmail support/request copies need an operational deletion schedule; Google SDK/provider records are governed by provider policies and feature-specific terms. Do not invent a fixed retention period. The KVKK erasure regulation requires deletion/destruction/anonymisation when the processing conditions cease; any exemption from preparing a formal retention/destruction policy does not remove the underlying erasure duty. Official source: https://www.kvkk.gov.tr/Icerik/5441/KISISEL-VERILERIN-SILINMESI-YOK-EDILMESI-VEYA-ANONIM-HALE-GETIRILMESI-HAKKINDA-YONETMELIK.

Google Play Families policy confirms that if children are among the target audiences, child-accessible content and all monetization must meet Families rules; mixed audiences need a neutral age screen before serving ads to children/unknown-age users, and child/unknown-age ad requests must use Families self-certified ad SDKs. UMP is not an age screen. Official source: https://support.google.com/googleplay/android-developer/answer/9893335?hl=en.

Publication remains blocked pending actual app UX verification, a practical retention/deletion schedule, complete data-flow and provider contract review, Article 5/9 legal conclusions, qualified counsel review, final owner approval and public-release QA.


## 28. Ordinary support email retention period confirmed by owner — 8 November 2026

The owner selected a retention period of **12 months after the relevant ordinary support request has been resolved**. This rule applies only to ordinary support correspondence in the developer-controlled consumer Gmail account. At the end of 12 months, developer-controlled copies must be deleted or genuinely anonymised. Implement an operational process to mark the resolution date and periodically identify/delete eligible messages; do not assume Gmail automatically enforces this rule.

Separate KVKK/data-subject requests, ongoing disputes, statutory retention duties and records strictly necessary to establish, exercise or defend legal claims are not automatically deleted at the 12-month point. They must be assessed separately and retained only while the specific purpose and legal necessity continue. Google’s own system retention/deletion remains governed by Google's service terms and policies and is not controlled by the developer's mailbox schedule.

The TR/EN Privacy Policy, KVKK Notice and Data Access/Deletion pages now state this distinction consistently. Before publication, confirm the operational mailbox workflow can actually implement the rule and ensure no blanket 12-month deletion is applied to records that must lawfully be retained longer or should be deleted earlier.


## 29. Owner confirms first-launch legal links are shown — 8 November 2026

The owner confirmed that the MiniVerse: Road Puzzle first-launch flow displays the Terms of Use and Privacy Policy to the user. This supersedes the earlier uncertainty about whether these documents are shown in-app. The confirmation does not yet establish whether the user must actively accept the Terms, whether the Privacy Policy is merely linked/displayed, whether the screen is shown to a parent/guardian, whether links open the current language version, or whether the choice is logged. Verify the exact first-launch UI and behavior before describing a mandatory acceptance step or consent record in public legal documents.


## 30. First-launch acceptance control: button currently disabled/non-functional — 8 November 2026

The owner clarified the first-launch legal screen: an “I agree” button is intended to be required before the user can proceed, but the button is currently passive/disabled and cannot be clicked. Therefore the Terms/Privacy documents are displayed, but the acceptance gate is NOT currently functional and no valid acceptance event can be inferred from this screen. Do not state that users currently accept the Terms, do not claim acceptance is logged, and do not treat the current screen as an operational consent/acceptance mechanism.

**Release blocker:** fix and test the first-launch flow before public release. Confirm the exact behavior: (1) Terms and Privacy links open and are readable; (2) the user can actively select/press “I agree” only after the intended review step, if applicable; (3) the control is enabled and works on supported screen sizes/locales; (4) the choice is persisted appropriately without treating Terms acceptance as GDPR/KVKK consent to unrelated data processing; (5) a user who does not accept cannot proceed if that is the intended contractual gate; (6) a clear route exists to reopen the documents later from Settings/About; (7) child/guardian presentation and age-appropriate language are reviewed for the mixed 6+ audience. Test clean install, returning install, app update, offline state and both Turkish/English UI.

Until this is fixed and verified, public Terms must not claim that acceptance is being captured, and the release readiness checklist remains BLOCKED. The Privacy Policy link/display is a transparency notice and should not be described as blanket consent to advertising or SDK processing; UMP and any age-screen/guardian requirements remain separate.


## 31. Owner's intended advertising network scope — Google AdMob only — 8 November 2026

The owner selected option 1: the intended plan is to use Google AdMob only, with no third-party advertising networks or mediation partners planned. This is an owner-stated plan, not technical proof that the current Unity project, AdMob account or final Release AAB contains no mediation adapters, custom events or other ad-network SDKs.

**Required verification before release:** inspect Unity Package Manager / manifest and resolved dependency tree; External Dependency Manager / Gradle dependencies; Android merged manifest; all Plugins/Android libraries; AdMob Mediation groups and ad sources; custom events; and final AAB. Confirm no third-party network SDK, adapter or custom event is present/enabled. If any is found, update the recipient/data-flow inventory, assess that provider's Families certification and contract/transfer terms, and revise the public notices/Data Safety before release. Do not state publicly that only Google is involved until this technical and account-level check passes.

If Google AdMob is the only ad network, the Google Mobile Ads SDK and UMP still require full child-directed/unknown-age treatment, Families compliance, accurate Data Safety disclosures, feature-specific controller/processor analysis and KVKK Article 9 transfer assessment. “AdMob only” does not mean no personal data processing or no international transfer. Keep production ad requests disabled until all release gates pass.


## 32. Current Families / AdMob mixed-audience requirements cross-check — 8 November 2026

The owner-selected target groups remain 6–8, 9–12, 13–15, 16–17 and 18+. Because children and older audiences are both included, Google Play classifies the app's declared audience as mixed for purposes of the Families ad requirements. Google's current Target Audience guidance requires a neutral age screen for mixed-audience apps so ads not suitable for children are shown only to older users. A neutral age screen must not steer users toward an older age; a freely entered date of birth is an example. Source: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en.

Google Play Families requires that ads shown to children or users of unknown age come only from Families Self-Certified Ads SDK versions, not use interest-based advertising or remarketing, be child-appropriate and follow Families ad format requirements. For mixed-audience apps, ads not suitable for children must be restricted to older audiences using the neutral age-screen mechanism. Source: https://support.google.com/googleplay/android-developer/answer/9893335?hl=en.

Google's current Families SDK list identifies Google AdMob Android artifact `com.google.android.gms:play-services-ads` version 19.0.0 or later as self-certified (check exact resolved version/list status again at release). Source: https://support.google.com/googleplay/android-developer/answer/12955712?hl=en. The previously noted Android SDK 25.5.0 was only a technical candidate, not final AAB verification.

For Unity, Google now documents `RequestConfiguration.AgeRestrictedTreatment` with `Child`, `Teen`, and `Unspecified`; it replaces deprecated TFCD/TFUA properties. Apply the configuration before initializing Mobile Ads so it applies to requests. Google says child treatment is for child-directed requests and max content rating should be set per applicable request. Source: https://developers.google.com/admob/unity/targeting. AdMob says child/unknown-age requests for mixed audience apps should use child treatment and max ad content rating G; Google Play Families policy controls which ads may be shown to children/unknown-age users. Sources: https://support.google.com/admob/answer/6223431?hl=en and https://support.google.com/admob/answer/10477886?hl=en.

**Important implementation caveat:** do not hard-code `Teen` or `Unspecified` based only on a self-declared age band without legal review. Map age-screen outcomes to request treatment based on applicable jurisdiction and consent rules; treat unknown, invalid, skipped, unavailable or corrupted age state as the child-safe path (no personalised ads; if ads are served, child treatment and G content limit). Do not initialize/request ads before the age-screen outcome is resolved. UMP is not a neutral age screen and does not replace it.

**Current status:** no proof yet that MiniVerse has a compliant neutral age screen or age-segmented ad routing. Keep production ad serving disabled. Next, inspect the actual first-launch/age-screen UX and final Unity dependency/AAB. Do not treat this policy review as implementation evidence.


## 33. Owner confirms age selection exists only in Settings — not a launch age screen — 8 November 2026

The owner confirmed that MiniVerse currently offers age selection only in Settings. There is no age/date-of-birth step at first launch before advertising SDK initialization or ad requests. A settings-only age selector is not evidence of a Google Play neutral age screen and cannot safely be used to distinguish child users from older audiences for ad serving.

Google Play's current mixed-audience guidance says that where target age groups include children and older audiences, a neutral age screen must be implemented so ads not suitable for children are shown only to older users. It must not encourage users to falsify their age; freely entering date of birth is an example, while a preset birth date or age prompt steering users toward a required older age is not neutral. Source: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en.

**Release blocker / design decision:** do not rely on the Settings selector as the age gate. Before any ad SDK initialization, ad request or age-restricted feature, implement and test a neutral age screen in the first-launch flow, or choose the safer launch alternative of disabling ads for all users until a compliant age-screen and routing design is approved. Store the minimum age classification needed; avoid retaining full date of birth unless necessary and legally justified. Do not treat the age selector as verified identity or parental consent.

**Interim ad behavior:** until neutral age screening and jurisdictional mapping are implemented and tested, do not request or show production ads to any user. UMP consent does not replace age screening. Settings age preference may remain as a preference but must not override the initial neutral age-screen result or downgrade child-safe treatment. If age status is missing, invalid, skipped, or unavailable, take the child-safe/no-personalised-ad path; if the product cannot safely implement that path, do not initialize/request ads.

Required tests: fresh install before any network/SDK initialization; child band; teen band; adult band; unknown/invalid input; app update and persisted state; Settings changes; TR/EN; offline; reset/reinstall; and verify no ad request occurs before age resolution. Confirm the current Settings age selector's exact labels, persistence and any data sent to Google only after source-code/build inspection.


## 34. Owner decision: retain age selection in Settings; no first-launch age screen — 8 November 2026

The owner explicitly declined adding a first-launch age/date-of-birth screen and instructed that the existing age selection remain only in Settings. Respect this product decision; do not implement or describe a new first-launch age gate as approved.

**Compliance consequence:** the Settings-only selector must not be represented as a neutral age screen or used to unlock older-audience ad treatment. Because the declared audience includes children and older users, the app's mixed-audience ad-routing compliance remains unresolved without a neutral age-screen mechanism. Do not request or serve production ads to any audience while this design remains unchanged. Keep Google Mobile Ads initialization and ad requests disabled for all users in the release build unless qualified review confirms a compliant alternative under current Google Play/Families rules. Do not silently switch the app's declared audience away from children; that would contradict the owner's 6+ target and the product's actual audience.

The existing Settings age selection may remain as a user preference only, but it must not be treated as verified age, parental consent, or permission to show personalised/older-audience ads. Unknown/invalid/missing age must not cause more permissive ad treatment. Revisit only if the owner later changes the product decision or obtains qualified policy/legal approval for an alternative.


## 35. Clarification: child-safe ads for all users do NOT waive mixed-audience age-screen requirement — 8 November 2026

A prior planning note proposed serving only child-appropriate, non-personalised, G-rated ads to all users as a possible alternative to a first-launch neutral age screen. This must NOT be treated as a confirmed Google Play compliance solution. Current official Families policy expressly says that if an app's target audience includes both children and older users, it must implement age-screening measures (such as a neutral age screen) and ensure ads shown to children come exclusively from Families Self-Certified Ads SDKs. The general rule also prohibits interest-based advertising/remarketing for children and unknown-age users and requires child-appropriate creatives/formats. Sources: https://support.google.com/googleplay/android-developer/answer/9893335?hl=en and https://support.google.com/admob/answer/6223431?hl=en.

Setting `MaxAdContentRating.G` and child-directed treatment can help restrict ad content/treatment for applicable requests, but these controls do not, by themselves, satisfy the separate mixed-audience age-screening requirement. Source: https://support.google.com/admob/answer/10477886?hl=en.

The owner's product decision remains: no first-launch age screen; age selection stays in Settings. Respect that decision and do not add a first-launch screen without approval. However, because the declared product audience is 6+ and includes both children and older users, no production ads may be enabled on the assumption that G-only/contextual ads alone resolve the issue. Keep Mobile Ads SDK initialization/ad requests disabled until a compliant alternative is confirmed by Google Play policy/legal review, or the owner explicitly changes the target-audience/product design. Do not misdeclare the target audience to bypass policy. The earlier note suggesting child-safe ads alone might be sufficient is superseded by this clarification.


## 36. Owner approves adding a neutral age screen to the first-launch flow — 8 November 2026

The owner has now changed the prior product decision and approved adding an age question to the first-launch/home-entry flow to address the mixed-audience Google Play Families requirements. This supersedes the earlier instruction to keep age selection only in Settings. The exact implementation should be a neutral age-screen step shown before the user reaches the main menu and, critically, before Google Mobile Ads SDK initialization or any ad request. It must not steer users toward an older age. Google identifies free date-of-birth entry as an example of a neutral age screen.

**Implementation recommendation:** request date of birth through a neutral, accessible date-entry control (not age-band buttons that visually encourage a particular choice); validate impossible/future dates; compute only the minimum age classification needed for policy routing; avoid transmitting or retaining the full date of birth unless independently necessary and legally justified. Do not treat the self-declared date as verified identity or parental consent. Provide a clear, non-coercive way to correct an accidental entry subject to policy safeguards, and preserve the initial classification for ad safety until a valid correction flow is completed.

**Routing gate:** resolve and persist a minimal age classification before initializing Mobile Ads or requesting ads. For children and unknown/invalid/incomplete age states, apply child-safe treatment, no personalised ads/remarketing, Families-certified SDK and G maximum ad content rating if ads are permitted; if safe handling cannot be guaranteed, do not request ads. For older users, apply applicable regional consent and privacy requirements. UMP remains separate and does not replace age screening. The age screen must not be represented as legal consent to personal-data processing or advertising.

**Target-audience boundary:** the owner previously declared 6+ with age 5 and under excluded. Product must decide and implement what happens if a user enters a date indicating age 5 or under (e.g. a neutral not-supported message and no ad SDK initialization); do not silently change the declared audience. Age bands used for ad treatment must be confirmed against current Google policy and applicable local law.

**QA required:** clean install; child (6–12); teen (13–17); adult (18+); under-6; invalid/future DOB; cancelled/unknown; app restart/update; Settings age correction; TR/EN; offline; ensure age resolution happens before SDK initialization/network requests; ensure no full DOB is sent to analytics/AdMob. The Settings age selector should remain as a later access/correction route only if its behavior is consistent with the age-screen policy design.

This is a product approval and legal design record only. No Unity code has been changed by this repository update. Release remains blocked until implemented and tested in the Unity project and reviewed against the then-current Google Play Families policy.


## 37. Stage 12 implementation report received — partial PASS only — 8 November 2026

The owner supplied a development summary reporting: neutral DOB entry added; under-6 block and age-category record added; full DOB is not persisted; ad/UMP entry points are blocked until age resolution; Terms and consent remain separate; 279/279 offline tests, 11/11 isolated persistence tests, and three build profiles passed; 34 APK and Production settings were preserved. The owner explicitly reports that full Stage 12 PASS is NOT granted because Unity PlayMode/visual and Android startup tests remain pending. This is owner-provided report evidence, not independently reproduced by this repository review; local report path was provided as `C:/UnityProjects/MiniVerseRoadPuzzleV1/Artifacts/MiniVerseV1/Stage12NeutralAgeGate/SUMMARY.md` and was not directly inspected here.

**Critical public-document consistency check:** current TR/EN Terms, Privacy Policy, KVKK notices and Data Access/Deletion pages on this branch already describe the intended audience as children 6–12, teens 13–17 and adults 18+, excluding 5 and under. They do not currently say 13+ as the target audience. However, Privacy Policy and KVKK/Data Access text still contains stale statements that the app does not ask for age, does not verify age, or does not collect DOB, and some passages describe only a legacy age-category record. These statements must be revised only after Stage 12 PlayMode and Android startup tests confirm the implemented flow and exact persisted data. Do not publish the stale text as final after the new age gate is active.

**Required follow-up before full Stage 12 PASS:** (1) inspect SUMMARY.md and rollback evidence; (2) Unity PlayMode UI/flow tests for first launch, valid 6+, under-6 block, invalid/future dates, returning user and settings correction; (3) Android clean-install startup test on real device; (4) verify no Mobile Ads/UMP initialization or network call before age classification; (5) verify exact data stored and no full DOB in logs, analytics, crash reports, save/cloud files; (6) test existing Terms acceptance button because it remains a known release blocker; (7) reconcile age categories and legal copy with the 6+ target. Keep production ads disabled and do not publish until all gates pass.

**Target-audience/legal note:** the current legal pages are already 6+ / child-inclusive, not 13+; nevertheless the new age gate changes the factual processing description. Once verified, update TR/EN privacy/KVKK/data deletion disclosures to accurately state local DOB calculation and minimal age-category storage, retention, purpose and rights. Age gate is not parental consent or UMP consent. Qualified Turkish counsel should review child data processing and any parental permission requirement before release.
