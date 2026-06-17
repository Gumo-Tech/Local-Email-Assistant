# Lokal Email Assistant — by Morving Tech

A local, AI‑powered email assistant for Windows. It reads, sorts and replies to your email
using AI — **running on your own computer**. Your mail and passwords stay on your machine; they
are only ever sent to the AI provider *you* choose (and with a local model, not even there).

**Demo video:** _add link_ · **Website:** www.morving-tech.dk

---

## 1. Download & run

1. Download **`LokalEmailAssistant.exe`** from this page (click the file, then **Download raw file**).
2. Double‑click it. A small console window starts the program, and your default browser opens
   the app automatically at **http://127.0.0.1:3001**.
   - If Windows SmartScreen warns (unsigned app): **More info → Run anyway**.
3. Leave the little console window open while you use the app. Close it to stop the program.

> No installation, no Node, nothing else to set up — everything is bundled in the one `.exe`.
> Requires Windows 64‑bit and an internet connection at startup (for the licence check).

---

## 2. First‑time setup (3 steps)

### Step 1 — Licence
Right now access is **free** — the app opens straight away with no key needed. If you ever see a
licence screen, paste the key you received and click **Activate** (you only do this once). No key?
Contact **gustav@morving-tech.dk**.

### Step 2 — Connect your email account
Click **⚙ Accounts** (top right) → **+ Add new account**.

**Gmail (and most providers) — App Password:**
1. Google won't accept your normal password, so create an **App Password**:
   - Go to your Google Account → **Security** → turn on **2‑Step Verification** (if not already).
   - Open **App passwords**, create one, and copy the 16 characters.
2. In the app: enter your **name**, your **email address**, pick the **provider** (this fills in the
   IMAP/SMTP servers automatically), and paste the **App Password**. Click **Test & Save**.
3. A green confirmation means it works, and your inbox loads.

**Outlook / Office 365:** choose Outlook and sign in with the Microsoft pop‑up instead.

**Just want to look around?** Use the built‑in **Demo account** — a sample inbox with no real
mailbox, perfect for trying every feature safely.

### Step 3 — Choose your AI
Two options, switch any time with the **🧠 Model** picker:

- **Local model (Ollama)** — free and fully private; nothing leaves your computer. Install
  [Ollama](https://ollama.com), then pick/download a model in **🔑 API → Ollama**.
  - ⚠️ **Pick a model that fits your machine.** Big models (12B+) need a strong graphics card —
    on a normal laptop they fall back to the CPU and become very slow. A **small model
    (3–4B)**, e.g. `llama3.2` or `gemma`, is fast and fine for email.
- **Cloud model (Claude / Gemini)** — fastest and highest quality, regardless of your hardware.
  Add your own API key under **🔑 API**. (You pay your provider for usage.)

---

## 3. Using the app

The app has four tabs:

- **✉️ Email** — your inbox. Click an email, press **✦ Generate draft**, watch the AI write a reply
  (live), edit it, then **Send reply**. You're always in control — nothing sends by itself here.
- **💬 Chat** — the same mail shown as message threads, with the whole conversation as context.
- **🔀 Flow** — a visual pipeline you build from nodes to automate things: **Inbox → AI Sorting →
  AI Reply → Approval → Send**. The AI sorts each email into a category and drafts a reply; those
  drafts go to the **Approval** tab for you to review (or, if you choose, send automatically). Drag
  from a node's **right** port to another node's **left** port to connect them.
- **✅ Approval** — your review queue for AI‑drafted replies. Each item shows the conversation, the
  proposed reply (editable) and **which category it was sorted into** — with a filter to focus on a
  single category. Read it, tweak if needed, and **Send reply** — or **Discard**. Nothing is sent
  until you approve it.

**Sorting tip:** in **AI Sorting**, give each category a clear, specific description — that's what
the AI uses to decide where each email belongs. Few, distinct categories beat many overlapping ones.

---

## 4. Privacy

- Your **emails, passwords and AI keys** stay in local files on your machine — they are never sent
  to Morving Tech.
- At startup the app sends only your **IP address, app version and an anonymous device id** to the
  Morving Tech licence server to verify your licence. This is logged with a timestamp for licence
  and security purposes and **automatically deleted after 90 days**.
- If you choose a cloud AI (Claude/Gemini), your email content is sent **only** to that provider.

---

## 5. Troubleshooting

- **The app didn't open in the browser** — go to **http://127.0.0.1:3001** manually.
- **AI replies are very slow** — it's almost always the model, not the app. Switch to a small local
  model or to Claude. A healthy reply should arrive within a few seconds.
- **Port already in use** — close any old console window still running the app, then start it again.
- **Stuck on "Loading…"** — make sure your email account test passed (⚙ Accounts) and, for local AI,
  that Ollama is running.

---

## Licence

Proprietary software. © 2026 Morving Tech. Copying, modifying, reverse‑engineering or
redistributing without written permission is not allowed. Support & licences:
**gustav@morving-tech.dk**.
