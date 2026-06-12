<p align="center">
  <h1 align="center">📝 markwiki</h1>
  <p align="center"><i>Local markdown wiki — write, organize, search. All in your browser.</i></p>
  <p align="center">
    <img alt="GitHub Pages" src="https://img.shields.io/badge/live-GitHub%20Pages-blue?style=flat">
    <img alt="size" src="https://img.shields.io/badge/size-468%20lines%20pure%20HTML/CSS/JS-purple?style=flat">
    <img alt="license" src="https://img.shields.io/badge/license-MIT-green?style=flat">
  </p>
</p>

**markwiki** is a single-file, browser-based personal wiki for markdown notes. Everything stays in your browser's localStorage — no server, no account, no sync. Write in markdown, preview in real time, organize with tags.

**[→ Open markwiki](https://neocrev.github.io/markwiki/)**

---

## Features

| Feature | Description |
|---|---|
| **Live markdown preview** | See rendered HTML as you type, powered by `marked` |
| **Tag organization** | Add/remove tags to categorize notes |
| **Full-text search** | Search across titles, content, and tags |
| **Keyboard shortcuts** | `Ctrl+N` new note, `Ctrl+S` save, `?` for help |
| **Table of contents** | Auto-generated from headings, with smooth scroll |
| **Heading anchors** | Click the `#` next to any heading to copy a direct link |
| **Word count** | Live word counter in the status bar |
| **Dirty tracking** | Visual indication when a note has unsaved changes |
| **Export/Import** | JSON export/import for backup or transfer; MD button downloads single note as `.md` |
| **Auto-save** | Notes persist to localStorage automatically |
| **Dark theme** | Tokyo Night color scheme, easy on the eyes |

## Usage

1. **Open** `index.html` (or the [GitHub Pages link](https://neocrev.github.io/markwiki/))
2. **Create** a note with `+` or `Ctrl+N`
3. **Write** markdown on the left, see it rendered on the right
4. **Tag** your notes by typing a tag name and pressing Enter
5. **Search** notes with the sidebar search box
6. **Export** your notes as JSON for backup

### Keyboard shortcuts

| Key | Action |
|---|---|
| `Ctrl+N` | New note |
| `Ctrl+S` | Save current note |
| `Ctrl+Shift+,` | Delete current note |
| `/` | Focus search |
| `Escape` | Close modals / blur input |
| `?` | Show help |

## Example

```markdown
# My Project Notes

## Architecture

The system uses a **microservices** approach:

- **API Gateway** — entry point for all clients
- **Auth Service** — handles authentication
- **Data Service** — manages persistence

## TODOs

- [x] Set up CI/CD
- [ ] Write documentation
- [ ] Deploy to production
```

This renders as formatted HTML with proper headings, lists, checkboxes, and code styling — all in real time.

## How it works

A single `index.html` with ~130 lines of CSS and ~200 lines of JavaScript. Notes are stored as JSON in `localStorage` under the `markwiki_notes` key. Markdown rendering uses [marked](https://marked.js.org/) loaded from CDN. Everything happens client-side — your data never leaves your browser.

## Data storage

Notes are stored in the browser's `localStorage` under the key `markwiki_notes`. This means:
- **Data persists** across sessions (as long as you don't clear site data)
- **Data is local** — never sent to any server
- **Export regularly** if you care about backups (use the Export button)

## Tech

- Vanilla JavaScript (ES6+)
- [marked](https://marked.js.org/) via CDN for markdown rendering
- `localStorage` for persistence
- Tokyo Night color theme

