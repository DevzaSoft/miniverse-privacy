# MiniVerse Road Puzzle — 16P-rc1 legal review candidates

**Status:** Review candidates only. Not legal advice, not approved by the owner, not approved by counsel, not published, and not deployed.

**Current owner product decision (9 November 2026):**
- Intended audience: 16 years and older.
- The game is not designed for children.
- No age or date-of-birth collection.
- No age verification, age classification, age-category persistence or age-based ad routing.
- This declaration does not verify the user's age or block access by users under 16.
- Users aged 16–17 are not automatically adults for every legal purpose.
- Production AdMob and UMP initialization/ad requests remain disabled.
- Unified onboarding retains language selection and legal-document access; Continue remains disabled until approved Terms configuration is verified.

## Candidate files

| Document | Turkish | English |
|---|---|---|
| Privacy Policy | `privacy-tr.md` / `privacy-tr.html` | `privacy-en.md` / `privacy-en.html` |
| Terms | `terms-tr.md` / `terms-tr.html` | `terms-en.md` / `terms-en.html` |
| KVKK notice | `kvkk-tr.md` / `kvkk-tr.html` | `kvkk-en.md` / `kvkk-en.html` |
| Retention, deletion and rights procedure | `data-access-deletion-tr.md` / `data-access-deletion-tr.html` | `data-access-deletion-en.md` / `data-access-deletion-en.html` |

## Material alignment work

- Replaced stale 13+, 0–12, 6+ and mixed-audience descriptions with the definitive 16+ intended-audience decision.
- Explicitly distinguish intended audience from age verification; the app does not collect age/DOB and does not block under-16 access.
- Removed claims that legacy age categories are read by the current app. Residual copies in old device backups are not claimed to be remotely erased.
- Clarified that production advertising and UMP initialization/ad requests are disabled in the currently reviewed configuration; SDK package presence is not equated with actual runtime data transmission.
- Kept the distinction between Privacy Policy notice, Terms acceptance and UMP privacy choices.
- Clarified that 16–17-year-olds may remain minors under local law.
- Added the owner's 12-month retention decision for ordinary support email correspondence after the support issue is resolved. Rights-request and provider records remain separate.
- Removed internal Stage21B.3 test notes from user-facing legal candidate bodies.

## Unresolved facts and legal review

Placeholders intentionally remain for:
- Establishment country and lawful formal service/request channel.
- Purpose-specific KVKK legal grounds.
- Actual recipients, controller/processor roles and transfer countries.
- KVKK Article 8/9 and applicable GDPR transfer mechanisms.
- Rights-request, provider and local technical-record retention schedules.
- Final document version, owner-approved effective date and canonical URLs.
- Consumer, liability, intellectual-property, governing-law and dispute provisions.
- Final Release SDK/dependency tree, native manifest and actual network data flows before advertising activation.

Do not replace these placeholders with guesses. Qualified Turkish legal review and owner approval are required before publication.

## Publication boundary

Only this review-candidate folder and internal review notes were updated on branch `legal-site-review`. Root/live HTML pages, the publication branch, GitHub Pages deployment, Unity legal configuration, Continue gating, Production advertising and APKs were not changed.
