# MiniVerse Road Puzzle — Global Release Privacy and Data Safety Review

Date: 2026-11-07
Status: REVIEW DRAFT ONLY — not a submitted Play Console declaration.

## Confirmed publisher decisions
- Markets: Worldwide, including Türkiye.
- Business model: Free download, optional rewarded advertisements through Google AdMob; no paid download or in-app purchases planned.
- Publisher: DEVZASOFT; individual data controller: Barışcan DEDEOĞLU.
- Privacy contact: devzasoft@gmail.com.
- No residential or postal address is to be published in these draft files. Applicable legal disclosure requirements remain unresolved.
- Package: com.devzasoft.miniverseroadpuzzle.

## Global data safety principles
Google Play's Data safety form reflects the union of practices across all currently distributed versions and regions. Data transmitted by embedded SDKs counts as collection even if the developer does not directly receive it. On-device-only processing is generally outside the collection definition; Android backup behavior must be verified.

Official references:
- https://support.google.com/googleplay/android-developer/answer/10787469
- https://support.google.com/googleplay/android-developer/answer/13323374
- https://developers.google.com/admob/android/privacy/play-data-disclosure
- https://developers.google.com/admob/android/privacy
- https://developers.google.com/admob/android/privacy/ad-serving-modes

## Candidate data inventory (NOT final form answers)
| Potential category | Source / purpose | Status |
| --- | --- | --- |
| Approximate location inferred from IP | Google Mobile Ads SDK | Confirm actual SDK and classification |
| Device or other identifiers | Ad ID, app set ID, other SDK identifiers | Confirm manifest, consent settings, SDK |
| App interactions | Launches, taps, ad views | Confirm SDK and reporting configuration |
| App performance / diagnostics | SDK and app technical telemetry | Confirm SDK behavior |
| Local game progress / preferences / reward transaction IDs | Game storage | Verify Android Auto Backup, off-device sync and linkability |
| Email/contact details | User-initiated support messages | Verify in-app flow and separate web/email processing |

Do not claim "no data collected" merely because no DEVZASOFT server is used. Do not mark all data as optional merely because rewarded ads are optional; SDK initialization may collect data independently.

## UMP / AdMob worldwide release checklist
- Verify actual Google Mobile Ads and UMP Unity plugin versions and dependencies.
- Verify consent info is refreshed at each app launch, consent form shown when required, and privacy options entry point exposed when required.
- Verify ads are requested only when allowed by current consent status and configured regional rules.
- Configure Google-certified CMP/TCF and relevant privacy messages for EEA, UK, and applicable other regions.
- Test EEA, UK, Switzerland and applicable US-state privacy paths using official debug/test mechanisms; avoid assuming one consent message covers every jurisdiction.
- Owner decision (2026-11-08): general family audience including children, teens and adults. Verify the exact Play Console age bands against the game presentation; do not assume "family audience" alone resolves child-directed / mixed-audience classification or removes child-related obligations.
- Verify rewarded ads are optional, properly rewarded only on confirmed completion, and production ad units remain disabled until live verification.
- Check Play Console Data safety, Ads declaration, privacy policy URL, app content, content rating and target audience against release AAB.

## Open evidence needed
1. Unity release build AAB and merged AndroidManifest.xml.
2. Dependency/version list, enabled SDKs and AdMob account configuration.
3. Network/SDK behavior on physical Android devices in relevant consent test modes.
4. Android backup/restore and local data deletion behavior.
5. Regional privacy messages, ad partners and transfer mechanism details.
6. Actual data retention and deletion procedures for Google SDK data and publisher-managed support communications.
7. Global legal review of applicable data protection, child privacy, and consumer requirements.
8. Public HTTPS legal URLs and a final owner-approved publication decision.

## Deployment
This file is for review branch legal-site-review only. Do not merge or publish it as a final policy or Play Console submission without owner approval and the required technical/legal verification.

## Owner decision update — general family audience (2026-11-08)

The owner has confirmed that the intended audience is a general family audience including children, teens and adults. This supersedes earlier notes that described the product as general audience / not specifically child-directed and supersedes 13+ wording in earlier candidate Terms. The exact Play Console age bands still require a product suitability decision. Do not select every band automatically.

Google Play mixed-audience ad requirements apply when the declared target age groups include children. Before any ads are served to children or users of unknown age, verify the required neutral age-screen behavior, child-directed ad request treatment, and every SDK/mediation adapter version against the current Families Self-Certified Ads SDK list. UMP is a consent/privacy messaging platform, not an age screen.

The product's legal classification in each market remains a separate assessment. For example, the US COPPA analysis considers whether the service is directed to children or has actual knowledge of collecting children's personal information; the FTC's factors include subject matter, visual content, characters, activities/incentives, music, marketing and intended audience. In the EU, GDPR Article 8 digital-consent age rules depend in part on Member State law. These issues cannot be resolved by choosing an “18+” label or adding generic wording to a policy.

References:
- Google Play target audience: https://support.google.com/googleplay/android-developer/answer/9867159
- Google Play Families Policy: https://support.google.com/googleplay/android-developer/answer/9893335
- FTC COPPA FAQ: https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions
- KVKK digital games and personal data symposium: https://www.kvkk.gov.tr/Icerik/8289/Dijital-Oyunlar-ve-Kisisel-Verilerin-Korunmasi-Sempozyumu


## Ad SDK version and child ad request cross-check (2026-11-08)

The earlier 21D technical candidate records Google Mobile Ads Unity Plugin 11.6.0 and Android Google Mobile Ads SDK 25.5.0. Google's currently retrieved Families Self-Certified Ads SDK list identifies Google AdMob Android SDK 19.0.0 or later as self-certified. The recorded Android SDK version is above that listed minimum, but this is not final Release AAB proof. Confirm the resolved Android artifact version and current list status in the actual bundle; check every mediation adapter/custom event independently.

For child or unknown-age ad requests, Google's AdMob guidance says to apply child-directed age treatment and set the maximum ad content rating to G. Confirm the current equivalent Unity API and verify it is applied on every applicable rewarded-ad request. Mixed-audience ad delivery also needs a compliant neutral age-screening path so non-child users can be distinguished from children; UMP consent messaging is not a substitute for age screening.

Sources:
- Families Self-Certified Ads SDK list: https://support.google.com/googleplay/android-developer/answer/12955712
- AdMob Families implementation guidance: https://support.google.com/admob/answer/6223431
- Target audience guidance: https://support.google.com/googleplay/android-developer/answer/9867159


## Owner's equal-priority child / teen / adult decision (2026-11-08)

The owner explicitly confirmed that young children (under 13), teens and adults are all target users with equal priority. This is stronger than a statement that children may happen to use an otherwise adult/general-audience game. The TR/EN Privacy Policy, Terms, KVKK notices and data-access/deletion pages on this branch have been updated accordingly. Do not reuse the older 18+ or 13+ audience statements.

This still does not automatically resolve the legal classification under COPPA. FTC's “mixed audience” category is a subset of child-directed services in which under-13 children are not the primary audience. The owner's equal-priority decision may support that analysis, but the game's toy-city/cartoon visual design, game subject, incentives, store listing, marketing and actual/likely audience must be assessed as a whole. Until qualified US counsel resolves the classification, take the conservative path and do not enable production ad SDK data collection. If under-13 children are the primary audience, do not use age screening to treat other visitors as adults; apply child protections to all visitors as required. If it qualifies as mixed audience, age screening may be used only within the FTC/Google requirements, and under-13 users must not have personal data collected before required COPPA notice/verified parental consent or a valid exception.

For Play Console, evaluate age bands individually. Owner has confirmed children under 13, teens and adults, but has not said whether toddlers/preschoolers aged 5 and under are included. Do not select “5 and under” until suitability is confirmed. Evaluate 6–8, 9–12, 13–15, 16–17 and 18+ separately against game mechanics, reading demands, visuals, audio, marketing and store listing. Exact declaration remains unresolved.

For every child or unknown-age ad request, AdMob guidance requires child-directed age treatment and maximum ad content rating G; use only current Families Self-Certified Ads SDK versions and compliant mediation adapters. No interest-based ads or remarketing for children/unknown-age users. Production ads remain disabled until age routing, any legally permitted neutral age screen, parental notice/consent or applicable exception, and all SDK paths are verified.

Sources:
- Google Play target audience: https://support.google.com/googleplay/android-developer/answer/9867159
- Google Play Families: https://support.google.com/googleplay/android-developer/answer/9893335
- FTC COPPA FAQ: https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions
- FTC COPPA Rule: https://www.ecfr.gov/current/title-16/chapter-I/subchapter-C/part-312
- AdMob Families implementation: https://support.google.com/admob/answer/6223431
- KVKK digital games symposium: https://www.kvkk.gov.tr/Icerik/8289/Dijital-Oyunlar-ve-Kisisel-Verilerin-Korunmasi-Sempozyumu



## Final owner age-band decision — 8 November 2026

The owner has confirmed that children aged 5 and under are NOT part of the target audience. The intended target groups are 6–8, 9–12, 13–15, 16–17 and 18 and over, with children aged 6–12, teens and adults intended with equal priority. This supersedes any earlier uncertainty about preschool/toddler inclusion. In Play Console, select only these five consecutive age bands after confirming the game and store listing are suitable for each. Do not select “5 and under.” This audience decision does not remove Families requirements: the app still intentionally targets children under 13. Production ads remain disabled until the child/unknown-age ad treatment, any required neutral age screen for the mixed audience, SDK/adapter eligibility and applicable legal requirements are implemented and verified.


## Final owner age-band decision — 8 November 2026

The owner has confirmed that children aged 5 and under are NOT part of the target audience. The intended target groups are 6–8, 9–12, 13–15, 16–17 and 18 and over, with children aged 6–12, teens and adults intended with equal priority. This supersedes any earlier uncertainty about preschool/toddler inclusion. In Play Console, select only these five consecutive age bands after confirming the game and store listing are suitable for each. Do not select “5 and under.” This audience decision does not remove Families requirements: the app still intentionally targets children under 13. Production ads remain disabled until the child/unknown-age ad treatment, any required neutral age screen for the mixed audience, SDK/adapter eligibility and applicable legal requirements are implemented and verified.


## Owner's intended ad network plan — Google AdMob only — 8 November 2026

The owner intends to use Google AdMob only and does not plan third-party ad networks or mediation partners. This is a product decision, not proof of the actual dependency tree/account configuration. Before release inspect Unity packages, resolved Gradle dependencies, Android merged manifest, Plugins/Android libraries, AdMob mediation groups/ad sources/custom events and final Release AAB. Confirm no other network SDK/adapter is present or enabled. If found, update data recipients, Families certification, contractual/transfer review and public notices/Data Safety. Even with AdMob only, Google Mobile Ads/UMP child-directed and unknown-age handling, Families rules, Data Safety and KVKK Article 9 review remain required. Production ads stay disabled.


## Families mixed-audience AdMob implementation baseline — 8 November 2026

The owner-declared target groups include children (6–12) and older audiences (13+), so Google Play mixed-audience rules apply. Google Play's current guidance requires a neutral age screen that does not steer users to an older age; free DOB entry is an example. Ads not suitable for children must only be shown to older users. Children and unknown-age users must receive ads only from Families Self-Certified Ads SDK versions; no interest-based advertising or remarketing; child-appropriate creatives and compliant formats. Sources: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en and https://support.google.com/googleplay/android-developer/answer/9893335?hl=en.

Google's current Families list includes Google AdMob Android `com.google.android.gms:play-services-ads` 19.0.0 or later; verify the exact resolved artifact and list at release: https://support.google.com/googleplay/android-developer/answer/12955712?hl=en. Google Unity SDK documents `AgeRestrictedTreatment.Child`, `.Teen`, `.Unspecified` replacing deprecated TFCD/TFUA, and says configure before Mobile Ads initialization: https://developers.google.com/admob/unity/targeting. For child/unknown-age ad requests use child treatment and max content rating G per AdMob's Families guidance: https://support.google.com/admob/answer/6223431?hl=en and https://support.google.com/admob/answer/10477886?hl=en.

Do not initialize/request ads before age resolution. Unknown, invalid, skipped or unavailable age state must follow the child-safe path. UMP is not an age screen. The existence of a neutral age screen and segmented routing has not been verified in the game. Production ads remain disabled pending UI/build tests.


## Settings-only age selector is not a neutral age screen — 8 November 2026

Owner confirms age selection is currently available only in Settings; no first-launch age/date-of-birth screen exists. Google Play's mixed-audience policy requires a neutral age screen so ads unsuitable for children are shown only to older users. It must not steer users to claim an older age; free DOB entry is an example. A settings-only selector is not proof of compliance. Source: https://support.google.com/googleplay/android-developer/answer/9867159?hl=en.

Release blocker: do not use the Settings selector as the ad gate. Before any ad SDK initialization/request, implement a neutral first-launch age screen and safe age routing, or keep production ads disabled for everyone until a compliant design is approved. UMP is not an age screen. Missing/invalid/skipped age state must take child-safe/no-personalised-ad path; if this cannot be assured, do not initialize/request ads. Test clean install, age bands, unknown/invalid, update/persistence, Settings changes, TR/EN, offline and ensure zero ad requests before age resolution.


## Owner decision: no first-launch age screen; keep age selection in Settings — 8 November 2026

The owner declined a first-launch age/date-of-birth screen and chose to retain the existing age selection only in Settings. Respect this choice. Do not call the Settings selector a neutral age screen or use it to route older-audience ads. Since the target includes children and older users, mixed-audience ad compliance remains unresolved. Keep Google Mobile Ads SDK initialization and all production ad requests disabled for every user unless qualified review confirms a compliant alternative under current Families rules. Do not change the declared target audience to exclude children without an explicit product decision. Settings age selection is a preference only, not verified age or parental consent.


## Correction to ad strategy: all-users G/contextual ads do not replace mixed-audience age screening — 8 November 2026

A prior proposal suggested child-appropriate, non-personalised G-rated ads to all users as a possible replacement for a neutral age screen. This is not a confirmed compliance path. Google's current Families policy expressly requires age-screening measures for apps targeting both children and older users, in addition to certified ad SDKs and child-appropriate ads. G max content rating and child-directed treatment are useful request controls but do not by themselves satisfy the age-screen requirement. Sources: https://support.google.com/googleplay/android-developer/answer/9893335?hl=en ; https://support.google.com/admob/answer/6223431?hl=en ; https://support.google.com/admob/answer/10477886?hl=en.

Owner decision remains no first-launch age screen; age selection stays in Settings. Do not implement a first-launch age screen without approval. Keep all production ad requests disabled until a compliant alternative is confirmed or the owner changes the product/target-audience decision. Do not misdeclare the audience.
