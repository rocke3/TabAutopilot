# Privacy Policy — TabAutopilot

**Last updated:** September 17, 2026

TabAutopilot is a browser extension that organizes your tabs. Here's how it handles your data, in plain English.

## The Short Version

TabAutopilot runs locally. It has no backend, no analytics and no tracking, and the developer never receives your data. One feature — Google Drive backup — is optional, off by default, and sends a copy of your TabAutopilot profile to **your own** Google Drive when you turn it on. Nothing else leaves your device.

## What We Access

TabAutopilot reads your **tab URLs and titles** to:

- Group tabs by topic
- Find and close duplicate tabs
- Track which tabs are inactive for hibernation
- Save and restore workspaces

This data is processed locally inside your browser.

## AI Processing

TabAutopilot uses the browser's built-in **Gemini Nano** model for smart tab categorization. This AI runs entirely on your device — it is part of the browser itself, not an external service. No tab data is sent to Google, OpenAI, or any other AI provider for categorization.

If your device doesn't support Gemini Nano, we fall back to a rule-based system that also runs locally.

## What We Store

All data is saved locally in your browser using the browser's storage and IndexedDB:

- Your settings (theme, hibernation timeout, grouping preferences)
- Saved workspaces (tab URLs, group names, colors)
- Snoozed tabs (tab URLs and titles, until they reopen)
- Tab activity data (when you last used each tab)
- Usage stats (per-site browse time and hourly activity, stored as **domain names only** — never full URLs or page titles)
- Any category corrections you make

This data stays on your machine. If you uninstall the extension, it's deleted.

## Optional Google Drive Backup

TabAutopilot offers an **opt-in** Google Drive backup so you can restore your profile on another computer. It is **off by default** and only runs after you explicitly sign in from Settings → Cloud backup. If you never enable it, the extension makes no network requests at all.

**What is uploaded:** your settings, saved workspaces (which contain tab URLs and titles), snoozed tabs (tab URLs and titles), custom categories, domain rules, category corrections, learning signals, group affinities, and per-day domain usage counts. Your general browsing history is **not** uploaded — only the tabs you chose to save or snooze.

**Where it goes:** directly from your browser to a hidden per-app folder in your own Google Drive (`appDataFolder`). That folder is invisible in your Drive file list and unreadable by any other app. The developer operates no server and never receives, stores or sees this data. It is not shared with, sold to, or transferred to any third party.

**Your email address:** read once from Google's userinfo endpoint so the extension can display which account is signed in. It is stored locally for that display only, and is never transmitted anywhere else.

**Limited Use:** TabAutopilot's use of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements. The data is used solely to provide the backup and restore feature you asked for, is never used for advertising, and is never sold or transferred, except as required by law.

**How to revoke:**

- Sign out from Settings → Cloud backup, or
- Remove access at [myaccount.google.com/permissions](https://myaccount.google.com/permissions), or
- Delete every cloud backup from Settings → Cloud backup → Delete cloud backups.

## What We Don't Do

- We **don't** operate a server or receive your data
- We **don't** use analytics, telemetry or tracking
- We **don't** use cookies
- We **don't** show ads
- We **don't** sell or transfer your data to third parties
- We **don't** require an account to use any feature except the optional Drive backup
- We **don't** load or execute any remote code

## Your Control

- Uninstalling the extension deletes all locally stored data
- You can export and import your profile as a local JSON file from Settings
- You can disable AI categorization at any time
- You can turn off usage-stats tracking, and clear your usage history, from the Usage stats dashboard
- You choose when to save or restore workspaces
- Google Drive backup stays off unless you turn it on, and can be signed out and deleted at any time

## Open Source

TabAutopilot is open source. You can review the code yourself to verify everything in this policy:
[github.com/rocke3/TabAutopilot](https://github.com/rocke3/TabAutopilot)

## Changes

If we change this policy, we'll update the date above and note it in the extension's changelog.

## Contact

Questions about privacy? Reach out:

- GitHub Issues: [github.com/rocke3/TabAutopilot/issues](https://github.com/rocke3/TabAutopilot/issues)
- Email: mail@mdrashi.com
