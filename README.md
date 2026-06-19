# Claude Code Workshop — Berlin

Build and deploy your own website in 2 hours using Claude Code. No prior coding experience needed.

---

## What you'll build

Choose one starter template:

| Template | Description |
|---|---|
| `templates/portfolio/` | Personal portfolio with an about section, projects, and contact info |
| `templates/landing/` | Small-business landing page with a hero, services, and contact section |

By the end of the workshop, your site will be live on the internet at a Vercel URL you can share with anyone.

---

## Before the workshop

Make sure you have accounts set up for:

- **GitHub** — to store your code
- **Claude** — to power Claude Code
- **Vercel** — to deploy your site

You should have received a setup email with the checklist. If you missed it, ping the organizer.

---

## Getting started

### 1. Fork this repo

Click the **Fork** button (top-right on GitHub) to copy this repo to your own account.

### 2. Open in Codespaces

On your fork, click the green **Code** button → **Codespaces** tab → **Create codespace on main**. Wait about 60 seconds for the environment to load.

### 3. Pick your template

In the Codespace terminal, run:

```bash
cd templates/portfolio   # or: cd templates/landing
npm install
npm run dev
```

Click the **"Open in Browser"** popup that appears — that's your live preview on port 3000. Every change you make will appear there instantly.

### 4. Open Claude Code

In a second terminal, run:

```bash
claude
```

Then start chatting. A good first prompt to try:

> *"Change the headline to say 'Hi, I'm [your name]'"*

---

## Deploying to Vercel

### Option 1 — Vercel CLI (recommended)

Run this from inside your template directory:

```bash
vercel login    # one-time setup
vercel --prod
```

A live URL will appear. That's your site.

### Option 2 — Vercel dashboard (GitHub integration)

1. Go to [vercel.com/new](https://vercel.com/new) and import your fork
2. Click **Edit** next to **Root Directory** and set it to `templates/portfolio` or `templates/landing`
3. Vercel will auto-detect Next.js once the root directory is set
4. Click **Deploy**

> **Why set the Root Directory?** Your site lives inside `templates/portfolio/` (or `templates/landing/`), not at the top level of the repo. Without this setting, Vercel won't know where to look and will return a 404 or "no Next.js version detected" error.

If you hit that error after deploying, go to your project's **Settings → Build & Development Settings**, set the Root Directory, save, then click **Redeploy** from the Deployments tab.

---

## Reference docs

| Doc | What's in it |
|---|---|
| [docs/01-terminal-basics.md](./docs/01-terminal-basics.md) | The dozen terminal commands you'll actually need (`pwd`, `cd`, `mkdir`, etc.) |
| [docs/02-claude-commands.md](./docs/02-claude-commands.md) | Every Claude Code slash command, keyboard shortcut, and launch mode |
| [docs/03-prompts.md](./docs/03-prompts.md) | A library of useful prompts, organized by what you're trying to do |
| [docs/04-next-steps.md](./docs/04-next-steps.md) | Going further: custom slash commands, MCP servers, skills, and extending your site |
