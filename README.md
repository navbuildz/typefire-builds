# TypeFire

**A text expander, a clipboard manager and a Markdown notebook, in one Mac app. Your AI apps can use it too, through MCP.**

Download it at **[typefire.ai](https://typefire.ai)** · [Watch the trailer](https://www.youtube.com/watch?v=KnF4mVBFPzM) · [Release notes](https://typefire.ai/releases)

TypeFire 6 is the current release. Keyboard shortcuts reach your snippets, clips and notes from inside whatever you're working in, so you never switch windows to get to any of it.

## What it does

### Snippets

- **Abbreviations that expand everywhere.** Type a few characters and get the whole thing, in every Mac app and every website.
- **Dynamic tokens.** Dates with math and formats (`{{date:+1M:MMMM}}`), the clipboard, the cursor position, fill-in fields you complete at expansion time, and other snippets inside a snippet.
- **Rich text, Markdown and scripts.** Snippets can carry formatting and pictures, or run a shell script, AppleScript or JavaScript and paste its output.
- **AI in a snippet.** `{{ai:rewrite}}` and other AI tokens run a prompt as the snippet expands.
- **Selection Prompts.** Select text in any app, press a shortcut, and AI rewrites it in place.
- **Prompt Chains.** Several prompts in a row, each fed the previous result.
- **Collections, tags and search** to keep hundreds of snippets in order, plus importers from TextExpander and aText.

### Clips

- **Your clipboard history**, kept, encrypted and searchable: text, images, colors, files and links.
- **Search the words inside screenshots**, read on your Mac.
- **Paste anything back** from a panel over the app you're in, with formatting kept or as plain text.

### Notes

- **A real Markdown editor** with live rendering, tables, callouts, code blocks, footnotes and checkboxes.
- **Wikilinks and backlinks**, tags, daily notes, quick capture from any app, and tabs like a code editor.
- **Your own folders.** It writes plain `.md` files and opens an existing Obsidian vault where it sits, with nothing rewritten. Several vaults at once.
- **Quick Look for Markdown.** Press Space on any `.md` file in Finder and see it rendered.
- **Version history** for every note, and AI on a note (summarize, rewrite, your own instruction).

### Search, the graph and Weave

- **One search across everything.** Snippets, clips and notes in one box, with operators like `tag:`, `in:` and `before:`.
- **The graph.** Everything you write, drawn as one board, with the links you made and the ones TypeFire found.
- **Weave** (Apple silicon) finds notes by what they mean, with a small model that runs on your Mac.

### AI apps (MCP)

TypeFire 6 is an MCP server built into the Mac app. Claude, Claude Code, Cursor, Codex, VS Code (GitHub Copilot agent mode), LM Studio, Windsurf and any other MCP client on your Mac can search, read and save your TypeFire notes and snippets, and your clipboard history if you turn it on.

- **Notes, in every vault:** search with tags, folders, dates and properties (or by meaning, with Weave on Apple silicon), read a note or one section, follow links and backlinks, create, edit, rename or move, add to today's daily note, and delete to the Trash. Works with Obsidian vaults, with no plugin and no API key, and Obsidian doesn't need to be open.
- **Snippets:** search, read, and create or edit any type, including Selection Prompts and chains.
- **Clipboard history:** off until you turn it on. Then search it (including text inside screenshots), read a clip, or put one back on the clipboard.
- **The note you have open:** ask "summarize this note" and the AI reads the one open in TypeFire. It can also bring TypeFire forward with a note open.
- **Safety:** an edit is refused if the note changed since the AI read it. Deletes go to the Trash. There's a switch for each world and a Read only mode.
- **Free and Pro:** searching and reading are free. Creating, editing, moving and deleting need TypeFire Pro or the trial.
- **Local:** the connection stays on your Mac. No API key and nothing to host.

#### Connect

In TypeFire, open **Settings → AI apps (MCP)** and click **Connect** beside your AI app. To add TypeFire to any other MCP client by hand, use this stdio server:

```json
{
  "mcpServers": {
    "typefire": {
      "command": "/Applications/TypeFire.app/Contents/MacOS/typefire-mcp",
      "args": []
    }
  }
}
```

Requires TypeFire 6 or later. More: [typefire.ai/mcp](https://typefire.ai/mcp) · Obsidian: [typefire.ai/obsidian-mcp](https://typefire.ai/obsidian-mcp)

### AI providers

Bring your own: **Apple Intelligence** (on-device, no key, macOS 26 on Apple silicon), **Claude**, **OpenAI** and **Gemini** with your API key, or a **local model** through Ollama or LM Studio. Each provider starts on its fast model, and you can pick any other in Settings.

### Sync and languages

- **iCloud sync** for snippets, clips and notes across your Macs, through your own iCloud.
- **In 8 languages:** English, German, Spanish, French, Italian, Dutch, Portuguese (Brazil) and Russian.

## Install

Download **`TypeFire.dmg`** from [the latest release](https://github.com/navbuildz/typefire-builds/releases/latest), or from [typefire.ai](https://typefire.ai). Open it and drag TypeFire to Applications.

- **Requirements:** one download for Apple silicon and Intel Macs, macOS 13 Ventura or later. Apple Intelligence and Weave need Apple silicon.
- **Signed and notarized by Apple.**
- **Updates** arrive inside the app: TypeFire checks for a new version and installs it when you click Update.

### Which file do I want?

Every release carries the same build under a few names. Unless you have a reason otherwise, take the first one.

| File | What it is |
|---|---|
| `TypeFire.dmg` | **The installer. This is the one you want.** Always the newest release. |
| `TypeFire_x.y.z_universal.dmg` | The identical installer, with the version in the filename. Use it to pin a specific version. |
| `TypeFire.app.tar.gz` | Used by the in-app updater. Not a download for people. |
| `TypeFire.app.tar.gz.sig` | Signature for the updater payload. |
| `latest.json` | The update manifest the app polls. |

The two DMGs are byte for byte identical; the release process verifies that before publishing.

## Free, and what Pro adds

Snippets, abbreviations, tokens and AI tokens, Markdown notes, Quick Look, iCloud sync for snippets, the 10 most recent clips, and searching and reading from AI apps are **free** and are not a trial.

**Pro is $18 once**, never a subscription, for three Macs. It adds your full clipboard history, iCloud sync for notes and all your clips, note version history, Selection Prompts and Prompt Chains, and lets AI apps create, edit, move and delete. New installs start with a 7-day Pro trial, no card needed.

## Privacy

- Your snippets, clips and notes are plain files on your Mac, and clips are encrypted there.
- Nothing is uploaded unless you turn on iCloud sync, which uses your own iCloud, or use an AI provider you chose with your own key.
- AI apps reach TypeFire only through the local MCP connection on your Mac, and only after you click Connect.
- Sign-in uses your email address and a one-time code.

## Links

- [Website](https://typefire.ai)
- [Release notes](https://typefire.ai/releases)
- [AI apps (MCP)](https://typefire.ai/mcp)
- [Docs and video tutorials](https://typefire.ai/docs)
- [Snippet templates](https://typefire.ai/templates)
- [Chrome extension](https://chromewebstore.google.com/detail/typefire/ihnpfaogaobdjipdkdpmgbbhncjkbahj)

## About this repository

This repo hosts the built releases and the update manifest. The application source is private. The newest version is always on [the latest release](https://github.com/navbuildz/typefire-builds/releases/latest).
