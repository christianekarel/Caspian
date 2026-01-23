# Caspian

**Run more AI agents. Ship faster. Stay sane.**

Caspian is the control plane for AI-powered development. Manage multiple coding agents in parallel, each in its own isolated workspace.

https://github.com/user-attachments/assets/3b154018-6e2e-462b-9621-1b92354ffef7

---

## The Problem

AI coding agents are insanely productive. You want to use them everywhere.

But right now you're running Claude Code in a terminal tab, hoping you remember which task is where, manually switching branches, and praying two agents don't touch the same file.

**This doesn't scale.** When you want to run 5 agents on 5 different features:
- Where do they all live?
- How do you see what each one is doing?
- How do you keep their changes from colliding?

## The Fix

Caspian gives each agent its own isolated workspace (git worktree). Run as many as you want, in parallel, with a single dashboard to monitor them all.

**More agents. Less chaos. Faster shipping.**

---

## Features

| What | Why it matters |
|------|----------------|
| **Isolated Worktrees** | Each task = its own branch + working directory. No cross-contamination. |
| **Live Monitoring** | Watch your agents work in real-time. See every file touch, every command. |
| **Multi-Agent Grid** | Run 5 agents on 5 tasks. Monitor all of them from one screen. |
| **Diff Review** | Review all changes before they go anywhere. |
| **PR Integration** | Ship clean PRs directly from completed work. |
| **Claude Code Native** | Built for Anthropic's Claude Code CLI. First-class support. |

---

## Quick Start

### You'll need
- [Node.js](https://nodejs.org/) 18+
- [Rust](https://rustup.rs/) 1.77+
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (for the AI part)

### Get running

```bash
git clone https://github.com/TheCaspianAI/Caspian.git
cd Caspian
npm install
npm run tauri:dev
```

That's it. No 47-step setup guide.

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
5. Review       →  Check the diff, approve what's good
6. Ship         →  Create a PR, merge with confidence
```

---

## Architecture

```
┌────────────────────────────────────────────────┐
│              Caspian Desktop App               │
├────────────────────────────────────────────────┤
│  Frontend (React + TypeScript)                 │
│  • Real-time chat streaming                    │
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

MIT. Do what you want.

---

## Links

[Website](https://caspian.ai) · [Docs](https://docs.caspian.ai) · [Discord](https://discord.gg/caspian) · [Twitter](https://twitter.com/CaspianAI)

---

**10x your AI coding. Without 10x the chaos.**
