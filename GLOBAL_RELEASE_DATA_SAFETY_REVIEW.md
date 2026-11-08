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

