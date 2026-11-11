# Truecaller

Last verified: 2026-11-11. Links and menu paths change: re-check before proposing them.

## See yourself as a stranger
- Truecaller builds its database largely from the address books of users who upload their contacts, and from tags on calls. You can be listed without ever having an account, and you are not notified (Privacy International explainer).
- Logged-out web search: the site has historically required login to search numbers (not tested in the 2026-11-11 browser pass, to verify). Do not log in or create an account for reconnaissance. The user can check from their own session.
- What a listing can show: name as saved by other people, number, carrier/location, sometimes email, photo, spam score and tags (to verify against the user's own view). The EU policy confirms Truecaller shows names against numbers and creates spam classifications from user reports.

## What to check (logged in, in the user's own session)
- Whether the user has (or had) the app installed and an account (including old phones).
- Search the user's own number(s) in every format in the app/web search to see the displayed name and tags.
- Contacts upload / "Contacts" permission in the app; linked Google/Facebook/Microsoft login.
- Whether the profile is public ("Who can see my profile").

## Settings to tighten
Menu paths inside the app change often (to verify).
- App settings > Privacy Center: turn off "Appear in search" / listing and contact sharing options (labels to verify; the web Privacy Center only offers sign-in, policy and FAQ, and the EU policy says profile visibility and account deactivation are managed in the app and the Privacy Center).
- Revoke the Contacts permission in the phone's system settings.

## Get your data (export / GDPR art. 15)
- Self-service: in-app Privacy Center; the Privacy Center page says users can download "a copy of all their information in a readable digital format" (exact button label not seen without login, to verify).
- Formal request: EU/EEA/UK/CH policy `https://www.truecaller.com/privacy-policy-eu` (updated 2026-06-03): the policy names **True Software Scandinavia AB** (Reg. No. 556784-0912, Mäster Samuelsgatan 56, 111 21 Stockholm, Sweden) as the entity behind "Truecaller", and Truecaller as data controller for GDPR-covered processing. Important: the search database (truecaller.com) holds a Swedish publishing certificate (utgivningsbevis, responsible publisher named in the policy) that exempts part of its processing from the GDPR, so art. 15/17 rights on the search database may be limited; use the unlisting page for it. DPO: `dpo.eu@truecaller.com` or post to "Data Protection Officer" at the address above; support: `support.eu@truecaller.com`. Complaints: Swedish Authority for Data Protection (IMY). Privacy Center: `https://www.truecaller.com/privacy/privacy-center` (the old `/privacy-center` URL returns 404; `privacy.truecaller.com` redirects there).
- If there is no answer within one month: complaint to the national data protection authority (see `references/removal-eu.md`).

## Remove
- Non-users and users: unlisting page `https://www.truecaller.com/unlisting`. Enter the number with country code, solve the captcha, confirm; reports say removal takes about 24-48 hours (third-party, unverified). Older guides cite `truecaller.com/unlist`: use `/unlisting`.
- Do you need to deactivate the app account first? Sources conflict (Privacy International describes the page for non-users; some guides say deactivate first). The official unlisting page (read 2026-11-11) does not say you must deactivate first: it warns that unlisting "can't be reversed" and that you lose caller ID, spam protection and one-tap sign-in, and offers a "No, I want to unlist" button (not clicked: it leads to the number form). The Privacy Center says users deactivate the account in the Privacy Center. Whether a user with an account must deactivate first remains unconfirmed (to verify): if the user has an account, deactivating it in the app/Privacy Center and then unlisting is the cautious order, otherwise a reinstall or login may relist the number.
- Unlisting is not reversible and only affects Truecaller's own database: other users still have the number in their contacts.
- Repeat for every phone number, and re-check after 3-6 months.
- Erasure request (art. 17): send it to the privacy contact above if the page does not work.

## Sources
- https://privacyinternational.org/explainer/2998/never-heard-truecaller-they-might-have-heard-about-you-here-how-you-can-unlist (how non-users get listed; unlisting URL), checked 2026-11-11
- https://www.truecaller.com/unlisting (official unlisting page; read in browser, form not submitted), checked 2026-11-11
- https://www.truecaller.com/privacy-policy-eu (official EU/EEA/UK/CH policy: entity, DPO, publishing certificate; read in browser), checked 2026-11-11
- https://www.truecaller.com/privacy/privacy-center and https://www.truecaller.com/privacy/privacy-faq (official; read in browser), checked 2026-11-11
- https://blog.incogni.com/truecaller-opt-out/ (third-party guide, conflicting info on deactivation and timing), checked 2026-11-11
