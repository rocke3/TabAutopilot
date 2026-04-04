# TabAutopilot — AI-Powered Tab Manager for Chrome

> Stop drowning in tabs. TabAutopilot automatically organizes, names, and cleans up your browser tabs using on-device AI — with zero data sent to any server.

[![Version](https://img.shields.io/badge/version-0.3.0-blue.svg)](https://github.com/rocke3/TabAutopilot/releases)
[![Chrome](https://img.shields.io/badge/Chrome-120%2B-green.svg)](https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom)
[![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-blue.svg)](LICENSE)

![TabAutopilot](/marquee-1400x560.png)

---

## Install

**[Get it from the Chrome Web Store](https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom)**

Requires **Chrome 120+**. AI features require **Chrome 127+** (falls back to rule-based grouping on older versions).

---

## Why TabAutopilot?

Most tab managers just group by domain. TabAutopilot is different — it reads your tab **titles** and uses **on-device AI** (Chrome's built-in Gemini Nano) to understand what you're actually working on. A localhost tab called "Investment Dashboard" goes into an Investment group, not a Dev group. And it **learns from you** — move a tab to a different group and it remembers your preference forever.

No account. No server. No tracking. Everything runs locally in your browser.

---

## Highlights

| Feature                 | What it does                                                        |
| ----------------------- | ------------------------------------------------------------------- |
| **AI Smart Grouping**   | Groups tabs by topic using on-device AI — not just domain           |
| **Auto-Learning**       | Learns from your manual moves and gets smarter over time            |
| **Tab Snooze**          | Close a tab now, it reopens automatically later                     |
| **Crash Recovery**      | Session auto-saved continuously, restore after crash with one click |
| **No Duplicate Groups** | Tabs merge into existing groups with the same name                  |
| **Glass UI**            | Modern glassmorphism design with frosted cards and ambient glow     |
| **100% Private**        | Everything runs on your device. Zero data leaves your browser       |

---

## All Features

### Smart Tab Grouping

- **Smart Group** — one click to auto-group all tabs by topic using AI
- **AI-powered naming** — groups get meaningful names like "Vue Dev" instead of "github"
- **Domain-based mode** — group by website with clean names (GitHub, YouTube, Translate, Docs, etc.)
- **AI-first approach** — reads tab titles to understand context, not just domain
- **No duplicate groups** — if a group with the same name exists, tabs merge into it
- **Auto-group on new tabs** — optional setting to group tabs automatically as you browse
- **Friendly names for 45+ sites** — Google Translate shows as "Translate", not "translate.google"

### Auto-Learning

- **Learns from you** — drag a tab to a different group and the extension remembers your preference
- **Corrections override AI** — your manual moves always take priority (Pass 0 runs before AI)
- **Gets smarter over time** — past corrections are fed into AI prompts for better future accuracy
- **Domain-level learning** — correct one Reddit tab and all Reddit tabs follow

### Tab Snooze

- **Snooze any tab** — click the clock icon on any tab to snooze it
- **Preset times** — In 1 hour, In 3 hours, Tomorrow 9am, Next Monday, Next Week
- **Custom time** — pick any date and time with the datetime picker
- **Snooze entire groups** — snooze all tabs in a group at once from the kebab menu
- **Snoozed list** — see all snoozed tabs and groups at the bottom of the Tabs section
- **Restore early** — bring back any snoozed tab or group before the timer fires
- **Cancel snooze** — remove from snoozed list without reopening
- **Group preservation** — snoozed groups reopen as a group with original name and color
- **Survives restart** — overdue snoozed tabs reopen when you start Chrome

### Duplicate Detection

- **Badge count** — extension icon shows how many duplicate tabs you have
- **One-click close** — close all duplicates instantly
- **Smart matching** — strips tracking parameters (UTM, fbclid, gclid) to find true duplicates

### Tab Hibernation

- **Auto-hibernate** — inactive tabs discarded after configurable timeout (15min-2hr)
- **Manual hibernate** — hibernate all inactive tabs with one click
- **Safe** — pinned tabs and tabs playing audio are never hibernated
- **Instant reload** — hibernated tabs stay in the tab bar and reload on click
- **Memory savings** — up to 95% memory reduction per hibernated tab

### Workspaces

- **Save workspace** — snapshot all current tabs and groups with a name
- **Restore workspace** — reopen a saved workspace in a new window
- **Switch workspace** — save current state, close tabs, restore another
- **Full group preservation** — tab group names, colors, and collapsed state are saved and restored

### Auto-Save & Crash Recovery

- **Automatic backup** — your session is saved every 5 minutes and on every tab open/close
- **Crash recovery** — if Chrome closes unexpectedly, your session is safe
- **Restore banner** — on next startup, a banner offers to restore your previous session
- **One-click restore** — reopen all tabs and groups exactly as they were
- **Dismiss option** — skip restore if you don't need it

### Activity Dashboard

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

### Settings

- **Grouping mode** — choose Domain-based or Smart AI
- **Min tabs per group** — set minimum (2, 3, 4, or 5)
- **Auto-group toggle** — enable/disable automatic grouping on tab creation
- **Hibernation timeout** — 15 minutes to 2 hours
- **Duplicate badge** — show/hide duplicate count on extension icon
- **Theme** — system, light, or dark mode with glassmorphism UI
- **Import/Export** — backup and restore all settings as JSON

### Glass UI

TabAutopilot features a modern glassmorphism design:

- **Frosted glass cards** — semi-transparent panels with backdrop blur
- **Gradient backgrounds** — deep indigo gradient in dark mode, soft blue in light
- **Ambient glow** — subtle gradient orbs for depth
- **Smooth transitions** — polished animations across all interactions

---

## Privacy

- **No account required** — works out of the box
- **No data collection** — we don't track anything
- **No external API calls** — nothing leaves your browser
- **On-device AI** — Gemini Nano runs locally through Chrome
- **Local storage only** — all data in chrome.storage + IndexedDB
- **Open source** — verify everything yourself

---

## Built With

- **[WXT](https://wxt.dev/)** — Next-gen browser extension framework
- **[Vue 3](https://vuejs.org/)** — Composition API + TypeScript
- **[Tailwind CSS v4](https://tailwindcss.com/)** — Utility-first styling with custom glass utilities
- **[Dexie.js](https://dexie.org/)** — IndexedDB wrapper for local data
- **[Gemini Nano](https://developer.chrome.com/docs/ai/built-in)** — Chrome's on-device AI for tab categorization

---

## Recommended Tools

If you're developing TabAutopilot, check out:

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

**Tech Stack:** PHP, Laravel, Node.js, TypeScript, Vue.js, React.js, C#/.NET, MySQL, PostgreSQL, Docker, AWS

[Website](https://mdrashid.com) · [GitHub](https://github.com/rocke3) · [LinkedIn](https://linkedin.com/in/rfmamun) · [Fiverr](https://fiverr.com/mamunurrashi461)
