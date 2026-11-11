# Telegram

Last verified: 2026-11-11. Links and menu paths change: re-check before proposing them.

## See yourself as a stranger
- A public username makes you findable in Telegram Global Search; `https://t.me/<username>` opens the app/chat with you. Logged-out check on 2026-11-11: `https://t.me/telegram` and `https://t.me/durov` (both channels) show a public preview page with name, subscriber count, description and a "Preview channel" link without login. Whether a private user's `t.me/<username>` page shows name, bio and photo was not tested (no personal username available): open it in a private window (to verify).
- A `t.me` link built from a phone number only works if your privacy settings let others find you by number.
- Public groups/channels: everything posted there is "accessible to everyone" and may be indexed or mirrored by third-party sites. Search your username and name with `site:t.me`.
- Read-only: do not log in to Telegram for reconnaissance; use the user's own session only.

## What to check (logged in, in the user's own session)
- Username (Settings > Edit Profile), bio, profile photos (old ones stay in the photo list), birthday.
- Messages posted in public groups and channels (they persist and may be quoted or forwarded by others).
- Phone number visibility and "who can find me by number".
- Contact sync: Settings > Privacy and Security > Data Settings (delete synced contacts).
- People Nearby / Live Location: make sure "Make Myself Visible" is off.
- Active sessions and connected bots/mini apps.

## Settings to tighten
Menu path: Settings > Privacy and Security (confirmed in the official FAQ https://telegram.org/faq, which uses it for last seen, auto-delete and gifts; submenu labels vary by client/version).
- Phone Number → Nobody (default: visible to contacts only); "Who can find me by my number" → My Contacts.
- Last Seen & Online, Profile Photo, Bio, Birthday → My Contacts or Nobody.
- Forwarded Messages → Nobody (removes the link to your profile when your messages are forwarded).
- Groups & Channels (who can add you) → My Contacts.
- Data Settings → delete synced contacts, disable contact sync.
- Auto-delete / account self-destruct period (default 18 months of inactivity) → shorten if desired.

## Get your data (export / GDPR art. 15)
- Self-service: Telegram Desktop > Settings > Export Telegram data (HTML or JSON; chats, media, contacts). The official announcement https://telegram.org/blog/export-and-more (2018) says "Settings > Export Telegram data"; recent Desktop versions put it under Settings > Advanced (not confirmed on an official page, to verify). The privacy policy itself describes no self-service tool.
- Formal request: the controller for EEA users is Telegram Messenger Inc.; the Article 27 EU representative is the European Data Protection Office (EDPO), Brussels, form at `https://edpo.com/telegram-gdpr-data-request`. The policy lists no privacy email. Other route: in-app Volunteer Support (Settings > Ask a Question). The policy sets no response deadline: GDPR's one month applies.
- Note: the EDPO link inside the policy text pointed to an unrelated domain at the time of checking; use the edpo.com URL cited in the sources and confirm it is the EDPO site.

## Remove
- Delete the account: `https://telegram.org/deactivate` (confirm via Telegram login code; irreversible; removes cloud messages, media and contacts). Messages you sent stay in other people's chats; deleted channel/supergroup messages remain visible to admins for 48 hours.
- Before deleting: delete your own messages in public groups/channels you care about, release the username (Edit Profile), remove profile photos.
- Content by others about you: report in-app (Report) and, for a GDPR art. 17 request, use the EDPO form above. Public channels may be copied by third-party sites: contact those separately, see `references/removal-eu.md`.
- Search engines / archive.org copies of `t.me` pages: see `references/removal-eu.md`.

## Sources
- https://telegram.org/privacy/eu (EU privacy policy: controller, EDPO, access, deletion, retention), checked 2026-11-11
- https://telegram.org/faq (phone number visibility, find-by-number, forwarded messages), checked 2026-11-11
- https://telegram.org/deactivate (deletion page, linked from the privacy policy sections 9.3 and 10.1), checked 2026-11-11
- https://edpo.com/telegram-gdpr-data-request (EDPO request form, as cited in the policy), checked 2026-11-11
- https://telegram.org/blog/export-and-more (Export Telegram data announcement; official, read in browser), checked 2026-11-11
- https://t.me/telegram and https://t.me/durov (logged-out channel previews; read in browser), checked 2026-11-11
