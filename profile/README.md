# millfolio

**A private, on-device document vault.** Ask questions about your own documents —
statements, PDFs, spreadsheets, notes — **without the data ever leaving your
device**.

### 🔗 [millfolio.app](https://millfolio.app) — the product
### 💻 [millfolio/millfolio](https://github.com/millfolio/millfolio) — the code (monorepo / superproject)

---

## How it works

An *untrusted* frontier model writes a small program over an **aliased** manifest —
it never sees your data or your file names. That program runs in a
**network-denied sandbox** on your machine, calling a *trusted* on-device model and
local tools to read the real content. The answer is computed and printed locally.

- **Frontier model = untrusted planner** — sees only aliases + your question.
- **Local model = trusted reader** — runs on-device, sees real content, returns
  only the minimal answer.
- **Sandbox** — the generated program has network access **denied** except
  loopback, and an egress guard that fails closed. Your data stays on the device.

## Get started

```sh
brew install millfolio/tap/mill
mill install      # provision inference + weights + vault tools + web app
mill start        # serves the millfolio web app at http://localhost:10000
mill index ~/Documents
mill ask "how much did I spend on groceries last month?"
```

See **[millfolio.app](https://millfolio.app)** for the full walkthrough, and the
[millfolio/millfolio](https://github.com/millfolio/millfolio) superproject for the
architecture, the repo map, and how to build from source.

## Community

Questions, ideas, and show-and-tell live in
[GitHub Discussions](https://github.com/millfolio/millfolio/discussions).
