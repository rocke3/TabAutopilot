# TabAutopilot – AI Tab Organizer and Manager

> Stop drowning in tabs. TabAutopilot automatically organizes, names, and cleans up your browser tabs using on-device AI — with zero data sent to any server.

[![Version](https://img.shields.io/badge/version-0.5.0-blue.svg)](https://github.com/rocke3/TabAutopilot/releases)
[![Chrome](https://img.shields.io/badge/Chrome-120%2B-green.svg)](https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom)
[![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-blue.svg)](LICENSE)

![TabAutopilot](/marquee-1400x560.png)

---

## Install

**[Get it from the Chrome Web Store](https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom)**

Requires **Chrome 120+**. AI features require **Chrome 127+** (falls back to rule-based grouping on older versions).

---

## Why TabAutopilot?

Most tab managers just group by domain. TabAutopilot is different — it understands what each tab is actually about by reading the page title, not just the URL. A localhost page called "Investment Dashboard" goes into an Investment group, not a Dev group. Open a new Instagram tab while a Social group already exists with Twitter and Reddit — Instagram joins it instantly. And it **learns from you** — move a tab to a different group and it remembers your preference forever.

No account. No server. No tracking. Everything runs locally in your browser.

---

## Highlights

| Feature                     | What it does                                                        |
| --------------------------- | ------------------------------------------------------------------- |
| **AI Smart Grouping**       | Groups tabs by topic using on-device AI — not just domain           |
| **Instant Tab Joining**     | New tabs snap into matching groups automatically, no waiting        |
| **Domain Rules Editor**     | 250+ built-in rules you can add to, edit, filter, sort, or reset   |
| **Auto-Learning (opt-in)**  | Learns from your manual moves and gets smarter over time            |
| **Tab Snooze**              | Close a tab now, it reopens automatically later                     |
| **Crash Recovery**          | Session auto-saved continuously, restore after crash with one click |
| **No Duplicate Groups**     | Tabs merge into existing groups with the same name                  |
| **Glass UI**                | Modern glassmorphism design with frosted cards and ambient glow     |
| **100% Private**            | Everything runs on your device. Zero data leaves your browser       |

---

## Smart Tab Grouping

![Smart Tab Grouping](/public/Screenshot1.png)

- **Smart Group** — one click to auto-group all tabs by topic using AI
- **AI-powered naming** — groups get meaningful names like "Vue Dev" instead of "github"
- **Domain-based mode** — group by website with clean names (GitHub, YouTube, Translate, Docs, etc.)
- **Context-aware** — understands tab titles to determine the right group, not just the domain
- **Instant joining** — open a new tab and it joins the matching existing group automatically
- **No duplicate groups** — if a group already exists, new tabs merge into it
- **Auto-group on new tabs** — optional setting to group tabs as you browse
- **Friendly names for 45+ sites** — Google Translate shows as "Translate", not "translate.google"

---

## Domain Rules

![Domain Rules Editor](/public/Screenshot3.png)

- **250+ built-in rules** — curated domain-to-category mappings covering Development, Social, Work, Shopping, News, Entertainment, Finance, Education, Research, Reference, Travel, and Health
- **Editable from the sidepanel** — add, edit, or delete any rule from the Rules tab
- **Sort** by domain (A–Z / Z–A) or category (A–Z / Z–A)
- **Filter** the table by any single category
- **Search** by domain name
- **Source badges** — each rule is tagged `seed`, `user`, or `learned` so you can see where it came from
- **Reset to defaults** — wipe user and learned rules, keep only built-in rules

---

## Auto-Learning

- **Opt-in toggle** — off by default. Flip "Learn grouping from activity" in the Rules tab to enable
- **Learns from you** — drag a tab to a different group and the extension remembers your preference
- **Immediate effect** — other tabs on the same domain benefit right away
- **Your moves always win** — manual corrections override everything else
- **Gets smarter over time** — the more you use it, the better it gets
- **Domain-level learning** — correct one Reddit tab and all Reddit tabs follow

---

## Settings

![Settings](/public/Screenshot2.png)

- **Auto-group toggle** — enable/disable automatic grouping on tab creation
- **Min tabs per group** — set minimum (2, 3, 4, or 5)
- **Auto-close duplicate tabs** — close duplicates as they appear
- **Duplicate badge** — show/hide duplicate count on extension icon
- **Grouping mode** — choose Domain-based or Smart AI
- **Hibernation timeout** — 15 minutes to 2 hours
- **Theme** — system, light, or dark mode with glassmorphism UI
- **Import/Export** — backup and restore all settings as JSON
- **Learn from activity** — opt-in toggle in the Rules tab

---

## Tab Snooze

- **Snooze any tab** — click the clock icon on any tab to snooze it
- **Preset times** — In 1 hour, In 3 hours, Next Monday
- **Custom time** — pick any date and time with the datetime picker
- **Snooze entire groups** — snooze all tabs in a group at once
- **Snoozed list** — see all snoozed tabs and groups at the bottom of the Tabs section
- **Restore early** — bring back any snoozed tab before the timer fires
- **Cancel snooze** — remove from snoozed list without reopening
- **Group preservation** — snoozed groups reopen as a group with original name and color
- **Survives restart** — snoozed tabs reopen on schedule even after browser restart

---

## Tab Hibernation

- **Auto-hibernate** — inactive tabs hibernated after configurable timeout (15min–2hr)
- **Manual hibernate** — hibernate all inactive tabs with one click
- **Safe** — pinned tabs and tabs playing audio are never hibernated
- **Instant reload** — hibernated tabs stay in the tab bar and reload on click
- **Memory savings** — up to 95% memory reduction per hibernated tab, freeing GBs of RAM

---

## Duplicate Detection

- **Badge count** — extension icon shows how many duplicate tabs you have
- **One-click close** — close all duplicates instantly
- **Smart matching** — recognizes true duplicates even when URLs have different tracking parameters
- **Auto-close** — optionally close duplicates as soon as they're opened

---

## Workspaces & Crash Recovery

- **Save workspace** — snapshot all current tabs and groups with a name
- **Restore workspace** — reopen a saved workspace in a new window
- **Switch workspace** — save current state, close tabs, restore another
- **Full group preservation** — tab group names, colors, and collapsed state are saved and restored
- **Unlimited workspaces** — completely free
- **Auto-save** — session saved every 5 minutes and on every tab change
- **Crash recovery** — if Chrome closes unexpectedly, restore everything with one click

---

## Everything at a Glance

![All Features](/public/Screenshot5.png)

---

## More Features

### Activity Dashboard

Located in the Workspaces view.

- **Memory stats** — see hibernated tab count and estimated memory saved (MB/GB)
- **30-day history chart** — daily memory savings visualized as a bar chart
- **Top domains** — bar chart of your most-visited domains by tab count
- **Category breakdown** — colored pills showing tab distribution (Development, Work, Social, etc.)
- **Quick stats** — open tabs, unique domains, average activity score at a glance
- **Activity levels** — bar chart showing High/Medium/Low/Idle tab distribution

### Tab Info & Sorting

- **Age indicator** — every tab shows how long it's been open (2h, 3d, 5m)
- **Activity score** — visual bar showing how active each tab is (green/yellow/red)
- **Sort tabs** — by title, domain, activity score, or default browser order
- **Sort groups** — by name, tab count, or default order
- **Search** — find tabs instantly by title or URL with match count

### Recently Closed

- **Last 8 tabs** — see recently closed tabs at the bottom of the panel
- **One-click restore** — reopen any recently closed tab instantly

### Undo

- **Undo everything** — last 10 actions are undoable (close, group, ungroup, hibernate)
- **Keyboard shortcut** — `Cmd+Z` / `Ctrl+Z` works in the side panel
- **Undo toast** — notification with undo option after every destructive action

### Keyboard Shortcuts

| Shortcut     | Action                   |
| ------------ | ------------------------ |
| `Alt+G`      | Auto-group all tabs      |
| `Alt+D`      | Close all duplicate tabs |
| `Alt+S`      | Save current workspace   |
| `Cmd/Ctrl+Z` | Undo last action         |

### Context Menu

Right-click any page for quick actions:

- Move current tab to a new group
- Save current group as a workspace
- Hibernate the current group
- Close duplicates of the current tab

### Glass UI

- **Frosted glass cards** — semi-transparent panels with backdrop blur
- **Gradient backgrounds** — deep indigo gradient in dark mode, soft blue in light
- **Ambient glow** — subtle gradient orbs for depth
- **Smooth transitions** — polished animations across all interactions

---

## Privacy

- **No account required** — works out of the box
- **No data collection** — we don't track anything
- **No external API calls** — nothing leaves your browser
- **On-device AI** — all processing runs locally on your machine
- **Local storage only** — all data stays on your device
- **Free** — free to use with all features included

---

## Recommended Tools

- **[NPM Manager](https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager)** — VS Code extension for managing npm packages with a visual interface. Run scripts, install/update/remove packages, and manage dependencies without leaving your editor.

---

## Feedback & Issues

Found a bug? Have a feature request?

**[Open an issue](https://github.com/rocke3/TabAutopilot/issues)**

Please include:

- Chrome version (`chrome://version`)
- Steps to reproduce the problem
- Screenshot if applicable

---

## License

This extension is free to use. All rights reserved.

See [LICENSE](LICENSE) for details.

---

## Author

**Mamunur Rashid** — Senior Software Engineer with 10+ years of experience in web development, specializing in dynamic CMS-based and custom web applications.

[Website](https://mdrashid.com) · [GitHub](https://github.com/rocke3) · [LinkedIn](https://linkedin.com/in/rfmamun) · [Fiverr](https://fiverr.com/mamunurrashi461)
