<div align="center">

#  Chat Context Extractor

**Extract structured AI-optimized context from any AI chat and paste into any other AI to continue seamlessly.**

![Version](https://img.shields.io/badge/version-1.0.0-6c63ff?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-00e5a0?style=flat-square)
![Manifest](https://img.shields.io/badge/manifest-v3-ffaa3c?style=flat-square)
![No API](https://img.shields.io/badge/no%20API-free%20forever-ff5e6c?style=flat-square)

</div>

---

## What It Does

When you have a great conversation with an AI, switching to a different AI means losing all context — the other AI has no idea what you discussed, what was built, or where you left off.

**Chat Context Extractor** solves this. It:

1. **Auto-scrapes** your current ChatGPT, Claude, or Gemini conversation
2. **Extracts structured context** — intent, memory, skills, goals, named entities, conflicts
3. **Generates an AI Mega-Prompt** you paste into any AI to continue the conversation instantly

No API. No account. No cloud. Runs entirely in your browser.

---

## Features

### 🔍 Auto-Scrape
- One-click scraping on ChatGPT, Claude, Gemini
- Detects the platform automatically
- Retry logic for dynamic content
- Clean fallback to manual paste for any other AI

### 🧠 Smart Local Extraction
- Intent verb detection — understands if you're trying to build, fix, debug, optimize, or deploy
- Sentence importance scoring — weights by action verbs, questions, tech mentions
- Resolution detection — marks each block RESOLVED or OPEN
- Named entity extraction — files, URLs, version numbers, error types
- Skill level detection — NOVICE through ADVANCED
- Conflict detection — catches goal changes and contradictions
- Topic clustering — groups by vocabulary, not just keywords

### 📁 Output Files Context
- Upload or paste any file the AI produced
- Auto-summarized by type: Python, JS, JSON, YAML, HTML, CSS, Markdown, Shell
- Toggle SUMMARY (compact) or FULL (embed entire file) per file
- Bundled into the context package automatically

### ✉️ AI Mega-Prompt
- Fully editable before copying
- Lock Edits toggle — prevents template changes from overwriting your edits
- 7 Quick Inject Templates:
  - **Continue Project** — picks up where you left off
  - **Continue Conversation** — neutral, works for any chat type
  - **Debug Code** — focuses the AI on finding and fixing bugs
  - **I'm a Beginner** — adjusts depth and tone
  - **Review & Improve** — asks for critique and suggestions
  - **New AI, Same Project** — seamless handoff to a new AI
  - **Expand on This** — takes the project further

### 💾 Sessions
- Save and name sessions
- Load, delete, export as JSON, import JSON
- Merge multiple sessions for multi-chat projects
- Auto-saves form state — survives popup close

### 📊 Token Counter
- Live token estimate with usage bars for GPT-3.5, GPT-4o, Claude

### 🖥️ Full Mode
- Opens in a new Chrome tab at full browser width
- All functionality, more space

---

## Installation

### Clone or download

```bash
git clone https://github.com/YOUR_USERNAME/chat-context-extractor.git
```

Or download as ZIP and extract.

### Load in Chrome

1. Go to `chrome://extensions`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked**
4. Select the `chat-context-extractor` folder
5. Pin the extension to your toolbar

---

## How to Use

### Auto-Scrape
1. Open any ChatGPT, Claude, or Gemini conversation
2. Click the extension icon in your toolbar
3. Hit **⚡ Auto-Scrape This Chat**
4. If it fails, paste manually in the text area

### Extract Context
1. Optionally add output files in the **Files** tab
2. Hit **⚡ Extract Everything**
3. **Extract tab** — instant local analysis, copy as context
4. **AI Prompt tab** — full mega-prompt, paste into any AI

### Use in a New Chat
Paste the copied context at the top of any new AI conversation, then say:

> *"This is structured context from a previous conversation. Use it to understand my background and continue helping me."*

---

## Platform Support

| Platform | Auto-Scrape | Notes |
|----------|-------------|-------|
| ChatGPT | ✅ Full | chatgpt.com and chat.openai.com |
| Claude | ✅ Full | claude.ai |
| Gemini | ⚡ Best effort | Falls back to manual if DOM changes |
| Others | ➕ Manual paste | Paste conversation in the text area |

---

## Keyboard Shortcut

| OS | Shortcut |
|----|----------|
| Windows / Linux | `Ctrl+Shift+E` |
| Mac | `Cmd+Shift+E` |

Customize at `chrome://extensions/shortcuts`

---

## Security

- **No external API calls** — fully offline, your data never leaves your browser
- **No analytics, no tracking, no telemetry**
- **Content Security Policy** enforced in manifest and HTML
- **Sender validation** on all message listeners
- **No inline scripts or event handlers** — CSP compliant
- **XSS prevention** via escaping on all external data
- **`web_accessible_resources`** scoped to extension pages only
- **500KB file size limit** to prevent freezing

---

## File Structure

```
chat-context-extractor/
  manifest.json       — extension config (Manifest V3)
  popup.html          — UI markup
  popup.js            — all logic and event wiring
  styles.css          — all styling
  content.js          — DOM scraper for AI platforms
  background.js       — service worker
  icons/
    icon16.png        
    icon48.png
    icon128.png
  README.md
  CONTRIBUTING.md
  CHANGELOG.md
  LICENSE
  .gitignore
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for setup instructions, code rules, and areas open for contribution.

---

## Troubleshooting

**Could not load manifest**
→ Make sure all 3 PNG icons exist in the `icons/` folder before loading

**Auto-scrape returns 0 messages**
→ Scroll through the full conversation first, then re-scrape

**Gemini scrape fails**
→ Paste manually — Gemini's DOM changes frequently

**Extension popup loses my work**
→ Form state is auto-saved every second — reopen and it will be restored

**Full mode won't scroll**
→ Refresh the extension at `chrome://extensions` after updating files

---

## License

MIT [LICENSE](LICENSE)

---

<div align="center">
Built with zero dependencies · Runs entirely in your browser · Free forever
</div>
