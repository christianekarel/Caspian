# Caspian

**The control plane for AI coding agents.**

Run multiple agents in parallel, with curated workflows that fit your team.

https://github.com/user-attachments/assets/3b154018-6e2e-462b-9621-1b92354ffef7

---

## The Problem

AI coding agents are powerful. But using them is completely ad-hoc.

You open a terminal, start prompting, and hope for the best. There's no structure. No workflow. No way to coordinate when you want multiple agents working on different parts of your codebase.

**When you want to scale AI across your team:**
- Everyone does it differently
- There's no visibility into what's running where
- No consistent workflow to follow

## Caspian

A control plane for AI-powered development. Spin up agents in isolated workspaces, run them in parallel, and manage everything from one place.

**Structure your AI workflows. Scale them across your team.**

---

## Features

| What | Why it matters |
|------|----------------|
| **Isolated Workspaces** | Each agent gets its own worktree. Clean separation between tasks. |
| **Parallel Execution** | Run multiple agents on different features simultaneously. |
| **Live Monitoring** | See what every agent is doing in real-time. |
| **Curated Workflows** | Define how your team uses AI. Consistent process, every time. |
| **PR Integration** | Ship completed work directly as pull requests. |
| **Claude Code Native** | Built for Anthropic's Claude Code CLI. |

---

## Quick Start

### You'll need
- [Node.js](https://nodejs.org/) 18+
- [Rust](https://rustup.rs/) 1.77+
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code)

### Get running

```bash
git clone https://github.com/TheCaspianAI/Caspian.git
cd Caspian
npm install
npm run tauri:dev
```

### Build for production

```bash
npm run tauri:build
```

Find your app in `src-tauri/target/release/bundle/`

---

## How It Works

```
1. Add repo     →  Point Caspian at your project
2. Create node  →  Spin up an isolated workspace
3. Run agent    →  Let Claude Code do its thing
4. Watch        →  See everything in real-time
5. Review       →  Check the changes
6. Ship         →  Create a PR, merge when ready
```

---

## Architecture

```
┌────────────────────────────────────────────────┐
│              Caspian Desktop App               │
├────────────────────────────────────────────────┤
│  Frontend (React + TypeScript)                 │
│  • Real-time agent streaming                   │
│  • Multi-agent grid view                       │
│  • Diff viewer & review mode                   │
├────────────────────────────────────────────────┤
│  Backend (Rust + Tauri)                        │
│  • Git worktree orchestration                  │
│  • Agent process management                    │
│  • File system watching                        │
│  • SQLite persistence                          │
└────────────────────────────────────────────────┘
```

---

## Tech

**Frontend:** React 19, TypeScript, Tailwind, Zustand, Vite

**Backend:** Rust, Tauri 2, libgit2, SQLite, Tokio

---

## Contributing

We welcome PRs. Check out [CONTRIBUTING.md](CONTRIBUTING.md) for the details.

```bash
npm install        # deps
npm run tauri:dev  # dev server
npm run lint       # check your work
```

---

## License

MIT

---

## Links

[Website](https://caspian.ai) · [Docs](https://docs.caspian.ai) · [Discord](https://discord.gg/caspian) · [Twitter](https://twitter.com/CaspianAI)
