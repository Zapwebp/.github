<div align="center">
  <img src="https://zapwebp.vercel.app/assets/zapwebp.svg" width="96" height="96" alt="Zapwebp logo" />
  <h1>Zapwebp</h1>
  <p><strong>Convert correctly.</strong></p>
  <p>
    <a href="https://zapwebp.vercel.app/">Web App</a> ·
    <a href="https://zapwebp-docs.vercel.app/">Documentation</a> ·
    <a href="https://open-vsx.org/extension/ebula/zapwebp-vscode">VS Code</a> ·
    <a href="https://zapwebp.vercel.app/llms.txt">llms.txt</a> ·
    <a href="https://www.npmjs.com/org/zapwebp">NPM</a>
  </p>
</div>

Zapwebp is a universal image conversion engine that preserves transparency, strips metadata, and runs everywhere—from the browser and terminal to build tools and AI agents. 

Unlike legacy tools that composite transparent SVGs onto black backgrounds, Zapwebp uses a two-stage pipeline to guarantee bit-for-bit alpha preservation.

---

## 🛠 The Ecosystem

Zapwebp is split into dedicated, focused repositories to keep the footprint small and the integrations flexible.

| Repository | Description | Surface |
| :--- | :--- | :--- |
| [**core**](https://github.com/Zapwebp/core) | The engine behind Zapwebp. | Shared conversion engine (`@zapwebp/core`) |
| [**cli**](https://github.com/Zapwebp/cli) | Terminal CLI and MCP server. | `zap`, `zapwebp` & `@zapwebp/mcp` |
| [**web**](https://github.com/Zapwebp/web) | The browser interface. | [zapwebp.vercel.app](https://zapwebp.vercel.app) |
| [**docs**](https://github.com/Zapwebp/docs) | Markdown documentation. | [zapwebp-docs.vercel.app](https://zapwebp-docs.vercel.app) |
| [**plugins**](https://github.com/Zapwebp/plugins) | Build tools and CI actions. | Vite, Next.js, GitHub Actions |
| [**storage**](https://github.com/Zapwebp/storage) | Cloud storage adapters. | Supabase, Firebase, Neocities |
| [**ui**](https://github.com/Zapwebp/ui) | Design system and error components. | Universal UI kit (`@zapwebp/ui`) |
| [**vscode**](https://github.com/Zapwebp/vscode) | Right-click to convert. | Editor extension (Open VSX) |
| [**laravel**](https://github.com/Zapwebp/laravel) | Image conversion for PHP. | Composer package (`zapwebp/laravel`) |
| [**lens**](https://github.com/Zapwebp/lens) | Read-only image inspector. | CLI (`zapwebp-lens`) |

---

## 📐 Architecture Principles

- **Drop. Convert. Done.** No signup, no waitlists, no ads, no telemetry. Instant results.
- **Fail Loudly.** Refuse to silently discard alpha channels, leak metadata, or overwrite untracked files.
- **Minimum Sufficient Architecture.** Zero bloated dependencies; native Web APIs, WebAssembly, and standard CJS/ESM modules.
- **Agentic Readiness.** Structured machine-readable JSON schemas, `llms.txt`, and an MCP server designed for AI pair programmers (Cursor, Claude, Antigravity).
- **Deterministic Output.** Same input + same options = byte-identical output. Guaranteed.

---

## 🚀 Quick Start

Run it locally, entirely in-memory:

```bash
# Convert a folder of SVGs to WebP, preserving transparency
npx zapwebp ./src/icons --to webp --clean
```

Give your AI agent superpowers:

```json
{
  "mcpServers": {
    "zapwebp": {
      "command": "npx",
      "args": ["-y", "@zapwebp/mcp"]
    }
  }
}
```

---

## 👥 Governance

Designed and operated by **Eldrex Delos Reyes Bula** in the Republic of the Philippines.

- 🌐 [Documentation](https://zapwebp-docs.vercel.app/)
- 📦 [npm Organization](https://www.npmjs.com/org/zapwebp)
- 📫 [Contact](mailto:eldrexdelosreyesbula@gmail.com)
- 📄 [MIT License](https://github.com/Zapwebp/zapwebp/blob/main/LICENSE)
