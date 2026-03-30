# TabAutopilot — AI-Powered Tab Manager for Chrome

> Stop drowning in tabs. TabAutopilot automatically organizes, names, and cleans up your browser tabs using on-device AI — with zero data sent to any server.

[![Version](https://img.shields.io/badge/version-0.2.5-blue.svg)](https://github.com/rocke3/TabAutopilot/releases)
[![Chrome](https://img.shields.io/badge/Chrome-120%2B-green.svg)](https://chrome.google.com/webstore)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Built with WXT](https://img.shields.io/badge/built%20with-WXT-purple.svg)](https://wxt.dev)

---

## What It Does

TabAutopilot reads your open tabs and groups them by **what you're actually doing** — not just by domain. A tab titled "Investment Manager" running on `localhost` goes into an Investment group, not a Dev group. An unused research paper from 3 days ago gets collapsed out of the way automatically.

**Everything runs on-device using Gemini Nano. Your browsing data never leaves your browser.**

---

## Features

### Smart Grouping

- **AI-first grouping** — Gemini Nano reads page titles to decide groups by topic and purpose
- **Local Dev detection** — `localhost`, `*.test`, `*.local`, and private IPs grouped as "Local Dev"
- **Activity-based groups** — unused tabs (5h+) and low-activity tabs (1–5h) automatically collapsed
- **Domain fallback** — 2+ tabs from the same domain get a domain group if AI doesn't claim them
- **Auto-group on new tabs** — optional setting to group automatically as you browse

### Tab Management

- **Duplicate detection** — badge shows duplicate count; one click closes them all
- **Tab hibernation** — discard inactive tabs to free memory; reload on demand
- **Sort tabs** — by title, domain, activity score, or default browser order
- **Sort groups** — by name, tab count, or default order
- **Auto-ungroup** — when a group shrinks to 1 tab, it's automatically ungrouped

### Group Actions

- **Rename inline** — click the ⋮ menu → Rename, type in place, press Enter
- **Close all tabs** in a group with one click
- **Move group to new window** — reopens all tabs in a fresh window with the same group name and color

### Recently Closed

- See the last 8 closed tabs at the bottom of the panel
- One-click restore any of them

### Tab Info

- **Age indicator** — every tab shows how long it's been open (`2h`, `3d`, `5m`)
- **Activity score bar** — visual indicator of how active each tab is (green/yellow/red)

### Workspaces

- **Save workspace** — snapshot all current tabs and groups by name
- **Restore workspace** — reopen a saved workspace in a new window
- **Switch workspace** — save current state and restore a different one

### Memory Dashboard

- Track daily tab hibernation stats
- See estimated memory saved (MB)
- 30-day history chart

### Undo Everything

- Last 10 destructive actions are undoable (close, group, ungroup, hibernate)
- `Cmd+Z` / `Ctrl+Z` works in the side panel

### Keyboard Shortcuts

| Shortcut     | Action                   |
| ------------ | ------------------------ |
| `Alt+G`      | Auto-group all tabs      |
| `Alt+D`      | Close all duplicate tabs |
| `Alt+S`      | Save current workspace   |
| `Cmd/Ctrl+Z` | Undo last action         |

### Context Menu (right-click any page)

- Move current tab to a new group
- Save current group as a workspace
- Hibernate the current group
- Close duplicates of the current tab

---

## Privacy

- **No account required**
- **No data collection**
- **No external API calls**
- AI runs entirely on-device via Chrome's built-in Gemini Nano
- All data stored locally in your browser (`chrome.storage` + IndexedDB)

---

## Installation

### From Chrome Web Store

_(Coming soon)_

### Manual Install (Developer Mode)

1. Clone the repo and install dependencies:
   ```bash
   git clone https://github.com/rocke3/TabAutopilot.git
   cd TabAutopilot
   pnpm install
   ```
2. Build the extension:
   ```bash
   pnpm build
   ```
3. Open Chrome → `chrome://extensions/`
4. Enable **Developer mode** (top-right toggle)
5. Click **Load unpacked** → select the `chrome-mv3/` folder

---

## Development

### Prerequisites

- Node.js 18+
- pnpm 8+
- Chrome 120+ (for Gemini Nano support, Chrome 127+)

### Setup

```bash
pnpm install
pnpm dev        # Start with hot reload
```

Chrome will open automatically with the extension loaded. The side panel and popup update instantly on save. Background script changes require a manual reload in `chrome://extensions/`.

### Scripts

```bash
pnpm dev          # Development with HMR
pnpm build        # Production build
pnpm zip          # Package for Chrome Web Store submission
pnpm test         # Run unit tests
pnpm typecheck    # TypeScript check
pnpm lint         # ESLint
pnpm format       # Prettier
```

### Project Structure

```
src/
├── entrypoints/
│   ├── background/     # Service worker — all business logic
│   ├── popup/          # Opens the side panel
│   └── sidepanel/      # Main UI (Vue 3)
├── ai/
│   ├── gemini-nano.ts  # Gemini Nano session + prompting
│   ├── categorizer.ts  # 5-layer categorization pipeline
│   └── rule-based.ts   # 100+ domain rules + keyword matching
├── services/
│   ├── grouping.ts     # Smart grouping algorithm
│   ├── activity-scorer.ts
│   ├── hibernation.ts
│   ├── workspaces.ts
│   ├── memory-stats.ts
│   └── undo.ts
├── components/
│   └── tabs/           # TabCard, TabGroupCard, TabList, TabSearchBar
├── composables/        # Vue composables (useTabs, useGroups, etc.)
├── storage/            # Dexie.js IndexedDB schema
└── types/              # TypeScript interfaces
```

### AI Architecture

Categorization uses a 5-layer pipeline with fallbacks:

```
1. User corrections  (100% confidence) — learned from manual overrides
2. Domain rules      (95%)             — 100+ hardcoded mappings
3. Keyword matching  (40–85%)          — TF-IDF on title + URL
4. Gemini Nano       (80%)             — on-device LLM
5. "Other" fallback  (0%)              — uncategorized
```

Grouping uses a 6-pass algorithm — AI first, so a tab titled "Investment Manager" on `invest.test` goes to the Investment group, not Local Dev:

```
Pass 1: AI clusters all tabs by title/purpose
Pass 2: Remaining local dev tabs → Local Dev group
Pass 3: Unused (5h+) → Unused group (collapsed)
Pass 4: Low activity (1–5h) → Low Activity group (collapsed)
Pass 5: Same-domain tabs (2+) → domain group
Pass 6: Same-category tabs (2+) → category group
```

---

## Tech Stack

| Layer               | Technology                      |
| ------------------- | ------------------------------- |
| Extension framework | [WXT](https://wxt.dev)          |
| UI framework        | Vue 3 + Composition API         |
| Language            | TypeScript                      |
| Styling             | Tailwind CSS v4                 |
| AI                  | Gemini Nano (Chrome Prompt API) |
| Local database      | Dexie.js (IndexedDB)            |
| Build tool          | Vite (via WXT)                  |
| Package manager     | pnpm                            |

---

## Requirements

- **Chrome 120+** for full functionality
- **Chrome 127+** for Gemini Nano AI features (falls back to rule-based grouping on older versions)

---

## Contributing

Pull requests are welcome. For major changes, open an issue first.

1. Fork the repo
2. Create a branch: `git checkout -b feature/your-feature`
3. Commit your changes
4. Open a pull request

---

## License

MIT © [Mamunur Rashid](https://www.spidernow.com/about.php)

---

## Author

**Mamunur Rashid** — Senior Software Engineer & Co-Founder at [SpiderNow](https://www.spidernow.com)

8+ years building custom web and SaaS applications. Former lead developer at AirportShuttles.com. Specializing in Vue.js, Nuxt.js, Node.js, and Chrome extension development.

- GitHub: [@rocke3](https://github.com/rocke3)
- LinkedIn: [rfmamun](https://linkedin.com/in/rfmamun)
- Also built: [npm-manager](https://github.com/rocke3/npm-manager) (VS Code extension)
