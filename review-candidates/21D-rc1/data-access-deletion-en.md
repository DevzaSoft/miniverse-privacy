> SUPERSEDED AUDIENCE NOTE (8 November 2026): This 21D-rc1 candidate predates the owner's later confirmation that MiniVerse Road Puzzle is intended for a general family audience including children, teens and adults. Do not use its prior 13+ or earlier audience wording as the current product decision. See `LEGAL-REVIEW-TR-EN.md` Section 10. The candidate remains a draft and is not publication-approved.

> REVIEW CANDIDATE ONLY — Not published; neither owner publication approval nor professional legal approval is recorded. Review version: **21D-rc1**, reviewed **2026-11-07**. Proposed effective-date rule: the separately owner-approved publication date, or a later date explicitly chosen by the owner, after all open issues are resolved; not effective today. Exact date: [OWNER_APPROVED_EFFECTIVE_DATE].

Controller/service provider: **Barışcan DEDEOĞLU**. Brand: **DEVZASOFT**. Individual developer. Contact: **devzasoft@gmail.com**. App: **MiniVerse Road Puzzle**, package: **com.devzasoft.miniverseroadpuzzle**. No residential address is published in this candidate. A lawful formal request/service channel without disclosing a residential address must be reviewed before publication; email alone is not assumed to satisfy every requirement.

# Data Retention and Deletion Policy

## Existing technical behavior
No general automatic day-based deletion was found for local game files. Progress, energy, achievements, preferences, first-launch and legacy age files serve different purposes. Some stores retain tmp/bak/corrupt/invalid copies. RewardReceipts can retain receipts/used markers/backups; no timed receipt pruning was identified. Event trace rotates to one previous copy near a 262144-byte threshold and keeps 96 in-memory events. Callback trace stops appending after 131072 bytes. These limits are not day/month retention promises.

## Your options
Reset Settings restores music, effects, brightness, tutorial and hint preferences. It does not delete all levels/stars/fuel, language/first-launch, legacy age, receipts, SDK or OS data. Identify what you want removed first. Clearing Android app data may lose local progress without guaranteed recovery. No data was deleted during this document phase.

Uninstalling may remove app-owned files; OS/OEM backups, external email and provider records may remain or return on reinstall. Actual backup/restore has not been tested without risking current saves. Device/OS tools are needed to manage backups; the developer cannot promise remote removal of every copy.

## Provider and support records
UMP reset is a Development testing tool, not deletion of all user/server data; it must not automatically change real consent. OS advertising-ID controls do not delete all App Set IDs/other records. Google's general retention explanation does not establish one definite period for every GMA/UMP record here. [Google retention](https://policies.google.com/technologies/retention).

Complete support [SUPPORT_RETENTION], requests [RIGHTS_REQUEST_RETENTION], providers [PROVIDER_RETENTION_REGISTER] and local corrupt/backup/receipt target periods/methods [LOCAL_RETENTION_SCHEDULE]. No nonexistent automatic deletion schedule will be published.

## Deletion requests
Initial contact devzasoft@gmail.com; formal channel [FORMAL_REQUEST_CHANNEL]. Identify scope and copies actually accessible. Any lawful retention exception needs a specific basis and limit; indefinite retention is not presumed. Report provider referrals, local steps and completed actions separately. Do not claim server deletion of local data not remotely accessible. Statutory response periods are not data-retention periods.

# Privacy Rights and Contact Procedure

## For users
Initial contact is devzasoft@gmail.com. You may use the subject “MiniVerse — privacy request”. Describe the action requested, relevant data and a reply channel. App version/general context may help. Do not send advertising IDs, consent tokens, passwords or identity photos by default. The formal KVKK method/required fields must be finalized at [FORMAL_REQUEST_CHANNEL]; general support is not automatically a sufficient formal channel.

## Publisher workflow
1. [PRIVACY_REQUEST_OWNER] logs the request without asking for unnecessary attachments. Access is restricted to authorized personnel; the actual process needs approval before launch.
2. Separate local game files, support email, Google/UMP and OS backup. Do not invent links to data that cannot be associated with the requester.
3. Apply necessary proportionate verification [REQUEST_VERIFICATION_METHOD]; receive legally required fields through a safe channel. Identity documents are not the default.
4. Assess law, right/exceptions, actual access and recipient roles. Act on accessible support records and explain appropriate provider/OS routes for other copies. Do not claim remote deletion of local progress.
5. Explain outcome/reasons, actions, inaccessible copies and complaint options. Retain request evidence according to [RIGHTS_REQUEST_RETENTION], not an assumed indefinite period.

## Rights and timing
KVKK Article 11 rights are listed in the separate notice; valid requests should be resolved promptly and no later than 30 days. Where GDPR applies, information/access/correction/erasure/restriction/portability/objection and relevant consent withdrawal depend on their conditions; the usual response deadline is one month. Any lawful extension/exception needs a concrete reason; these are not retention periods. The right to complain to the competent authority remains. Younger-user/representative authority and interests need separate assessment; teens are not all adults.

## Account deletion and distinct choices
The game has no user account and does not promise a nonexistent account-deletion screen. Local data clearing can lose progress; Reset Settings is not comprehensive deletion. UMP choices, Terms acceptance, OS ad-ID controls and erasure are different actions. Privacy Options is the existing Settings route when required/eligible; actual form evidence is limited to the Development diagnostic test described below.

[KVKK request route](https://www.kvkk.gov.tr/Icerik/2062/Basvuru-Hakki), [deadlines](https://www.kvkk.gov.tr/Icerik/5358/Kamuoyu-Duyurusu), [EU response guidance](https://commission.europa.eu/law/law-topic/data-protection/information-business-and-organisations/dealing-requests-individuals_en). Finalize the formal channel and operational owner before publication.
## Technical verification scope — not a publication claim
Stage21B.3 on 7 November 2026 observed real UMP 4.0.0 EEA debug form presentation, dismissal callback, Privacy Options, a user preference change and retained SDK state after restart on Android 15 through a Development-only diagnostic route that blocks advertising. The current device hash remains in a local test file only. Regulated-US-state and Other debug runs reported no form required; this does not verify every jurisdiction's legal compliance. Offline Update returned error code 2 without enabling ads. This does not verify the published Production lifecycle or complete network/data behavior. No UMP reset, erasure or Terms acceptance occurred. A privacy-form choice does not erase every provider record.

The last inspected Development APK lacked AD_ID/AdServices permissions and MobileAdsInitProvider; SDK libraries remained included. The final Release manifest, transmitted payloads, alternative identifiers and Backup/Restore scope still require verification. Generic vendor/location text on a consent form is not evidence that the game requests GPS permission. Missing approvals must not be bypassed by removing existing gates.
