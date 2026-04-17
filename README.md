# DCT Field SOP — Hardware Installation & Replacement

A mobile-first field guide for CoreWeave Data Center Technicians. Open it on your phone in the cage and follow along step by step — no app install, no login required to use the SOP itself.

**Live tool:** `https://your-username.github.io/dct-field-sop/`

---

## What's in this repo

| File | Description |
|------|-------------|
| `index.html` | The full DCT field SOP tool with live Jira integration |

---

## What the tool does

Five tabs, built for one-handed use on a phone:

- **Pre-work** — Checklist to complete before touching any hardware
- **Steps** — Step-by-step procedure with progress tracking
- **Decisions** — Tap-to-reveal answers for the situations not covered by the happy path
- **Escalate** — 4-tier escalation path with contact method and response SLA
- **Jira ↗** — Create a ticket directly in the DO project without leaving the tool

---

## How to use the Jira tab

The Jira tab creates tickets directly in the **DO (dct-ops)** project on `coreweave.atlassian.net`. It uses your personal Jira API token — stored only in your browser's memory for that session, never saved to disk or sent anywhere except Jira's API.

### Step 1 — Get your API token

1. Go to **[id.atlassian.com](https://id.atlassian.com)**
2. Click **Security** in the left sidebar
3. Click **Create and manage API tokens**
4. Click **Create API token**
5. Name it something like `DCT Field SOP Tool`
6. Click **Create** — copy the token immediately, you only see it once
7. Save it somewhere safe (your password manager, notes app, etc.)

### Step 2 — Use the tool

1. Open the tool URL on your phone
2. Tap the **Jira ↗** tab
3. Enter your CoreWeave Jira email (e.g. `yourname@coreweave.com`)
4. Paste your API token
5. Tap **Save & continue**
6. Fill in the ticket details and tap **Create Jira Ticket ↗**

The tool will return the new ticket key (e.g. `DO-106883`) with a direct link to open it in Jira.

> **Note:** You'll need to re-enter your token each time you open the tool in a new browser session. This is intentional — it keeps your credentials out of browser storage.

---

## Hosting on GitHub Pages

This repo is set up to serve `index.html` automatically via GitHub Pages.

To enable it on a fork or new repo:

1. Go to **Settings → Pages**
2. Under **Branch**, select `main`
3. Click **Save**
4. Your URL will be: `https://your-username.github.io/your-repo-name/`

> **Important:** The Jira tab requires the tool to be served over `https://` — it won't work if you open the HTML file directly from your computer as a `file://` URL. GitHub Pages handles this automatically.

---

## Security notes

- **No credentials are stored** — API tokens are held in memory only and cleared when the browser tab is closed
- **No data is logged** — the tool makes direct calls from your browser to `coreweave.atlassian.net`; nothing passes through any third-party server
- **Each DCT uses their own token** — tickets are created under your Jira identity, so the audit trail is accurate
- **Don't commit tokens** — never paste an API token into the HTML file or any file in this repo

---

## SOP reference

| Field | Value |
|-------|-------|
| Doc ID | DCT-SOP-HW-001 |
| Version | v1.0 |
| Project | DO (dct-ops) |
| Applies to | All DCTs — US-WEST-04, US-WEST-04A |
| Owner | DC-OPS Lead |

---

## Making updates

To update the SOP content:

1. Edit `index.html` directly in GitHub (click the file → pencil icon)
2. Commit the change to `main`
3. GitHub Pages rebuilds automatically — changes are live within ~60 seconds

---

## Questions or issues

Open a GitHub Issue in this repo, or reach out to the DC-OPS Lead directly.
