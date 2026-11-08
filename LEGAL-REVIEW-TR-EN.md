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
3. A neutral age screen is required for mixed-audience ad delivery so children receive the child-appropriate ad treatment. UMP privacy messaging is not a neutral age screen and must not be described as one.
4. The reviewed legal text says the app does not ask for age or collect date of birth. No neutral age-screen implementation has been established by the reviewed materials. Therefore, ad serving to children or users of unknown age is a **release blocker** until a compliant age-screen/ad-routing implementation is verified.
5. The reviewed configuration says Production ad serving is disabled and demo ad units are for development/testing. Keep live ad serving disabled until the exact Google Mobile Ads SDK/plugin version and every mediation adapter are checked against the current Families Self-Certified Ads SDK list and the release build's child-directed/non-personalised request behavior is tested.
6. A child-accessible app must be assessed under applicable child privacy and advertising law in every distribution market. Do not claim parental consent or age assurance merely because UMP is present.

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
