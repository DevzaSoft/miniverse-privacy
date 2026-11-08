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
