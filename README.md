# ☕ Java Study Companion

An interactive website for learning Java, **Weeks 1–12**, from the ground up.
Every week has plain-language explanations, verified code examples with their exact output,
step-through tracers, memory diagrams, playgrounds, bug hunts and a quiz. There is also a cheat sheet.

✦ *Designed by Savy*

---

## 📁 What's in this folder

| File / folder | What it is | Needed? |
|---|---|---|
| **`index.html`** | **The whole website**: styles, content for all 12 weeks, quizzes and cheat sheet, in one file | ✅ **Yes, this is the app** |
| `README.md` | This guide | Optional |
| `package.json`, `vite.config.ts`, `tsconfig.json` | Settings for the optional Vite dev server (Method 3) | Only for Method 3 |
| `src/` | Empty React starter left over from Google AI Studio. The site does not use it | No |
| `public/assets/aistudio/` | An older copy of the site and an image, saved by AI Studio | No |
| `metadata.json`, `.env.example` | AI Studio settings. No API key is needed | No |

> The website is a single static page. It needs **no build, no install and no API key**:
> any browser can open `index.html`.

---

## ▶️ Running it in VS Code

### Before you start
1. Unzip the download fully. Right-click the zip and choose **Extract All…**. Do not run it from inside the zip.
2. In VS Code, open the **folder**, not a single file: **File → Open Folder…** → choose `Java_Study_Module-main`.

### Method 1: Live Server (recommended ⭐)
The easiest way. Nothing to install apart from one VS Code extension.

1. Open the **Extensions** panel (`Ctrl+Shift+X`).
2. Search for **Live Server** (by *Ritwick Dey*) and click **Install**.
3. In the Explorer panel, **right-click `index.html` → Open with Live Server**.
   You can also click **Go Live** in the blue status bar at the bottom right.
4. Your browser opens at something like `http://127.0.0.1:5500/index.html`. 🎉
5. Edit `index.html` and save (`Ctrl+S`). The browser reloads on its own.

To stop the server, click **Port: 5500** in the status bar.

### Method 2: No VS Code at all
Double-click `index.html` in File Explorer. It opens in Chrome or Edge and works fully offline,
apart from the web fonts.

### Method 3: Vite dev server (optional, for developers)
Use this only if you want to work with the Node.js tools that AI Studio set up.

1. Install **Node.js 20 or newer** from <https://nodejs.org> (choose the LTS version), then restart VS Code.
2. Open the terminal in VS Code: **Terminal → New Terminal** (`` Ctrl+` ``).
3. Run:
   ```bash
   npm install
   npm run dev
   ```
4. Open **http://localhost:3000** in your browser.
5. Press `Ctrl+C` in the terminal to stop it.

> Methods 1 and 2 are simpler and give the same result. Method 3 downloads about 100 MB of packages
> that this site does not actually need.

---

## 🚫 Things that do NOT work (and why)

| You try… | What happens | Do this instead |
|---|---|---|
| Pressing **F5 / Run ▶** in VS Code | VS Code tries to run the files as a program and shows errors | Use Live Server (Method 1) |
| `node index.html` or opening a `.js` file with Node | Errors like `document is not defined` | It is a website: open it in a browser |
| The **✨ Ask Claude to run it** button | Shows *"Claude is not available where this page is open"* | This button only works on the claude.ai version. Use **⧉ Copy & open OnlineGDB**, which runs real Java |
| Running the Swing (window) examples on OnlineGDB | `HeadlessException` | Online compilers have no screen. Run GUI programs in your own Java IDE |

---

## 🛠️ Troubleshooting

**Blank page or no styles**
Make sure you opened `index.html` from the extracted folder, not from inside the zip, and that the file was not renamed.

**`npm` is not recognized**
Node.js is not installed, or VS Code was open while you installed it. Install Node.js LTS, then **close and reopen VS Code**.

**PowerShell says "running scripts is disabled on this system"** (Windows, when running `npm`)
Switch the terminal to Command Prompt: click the **⌄** next to **+** in the terminal panel → **Command Prompt**, then run the commands again.
You can also run this once in PowerShell: `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`

**Port 3000 or 5500 is already in use**
Close the other server or terminal, or let Live Server pick another port.

**My progress or quiz scores disappeared**
Progress is saved in your browser, separately for each address. `127.0.0.1:5500`, `localhost:3000`,
a double-clicked file and the GitHub Pages site each keep their own progress.
Private or incognito windows forget it when closed. The **↺ Refresh progress** button clears it on purpose.

**Fonts look plain**
The fonts (Baloo 2, Nunito, JetBrains Mono) load from Google Fonts, so they need internet.
Offline, the site still works with your system fonts.

---

## 🌍 Publishing for free with GitHub Pages

1. Push this folder to a **public** GitHub repository (`index.html` must be in the top level of the repo).
2. On GitHub: **Settings → Pages → Build and deployment**.
3. Set **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**, then click **Save**.
   Do not choose GitHub Actions or a Vite workflow: no build is needed.
4. After 1–2 minutes the site is live at
   **https://alien01b1.github.io/Java_Study_Module/**
5. To update it, commit a new `index.html`. GitHub republishes automatically. Press `Ctrl+F5` to see the change.

---

## ✏️ Editing the content

Everything is inside `index.html`. Use **`Ctrl+F`** in VS Code to jump around:

| To find… | Search for |
|---|---|
| The design (colours, rounded "clay" shapes) | `:root {` |
| The watermark | `Designed by Savy` (text) or `.watermark` (style) |
| A week's content, e.g. Week 9 | `id: 'w9'` |
| A section, e.g. collectors | `id: 'w9-collect'` |
| A week's quiz | `quiz: [` (the one after that week's sections) |
| The cheat sheet | `Core.cheatsheet(` |

Tips:
- Text inside `{{ }}` shows up as inline code, for example `{{System.out.println}}`.
- Keep a backup copy before big edits. If the page goes blank after an edit, press **F12 → Console**
  in the browser to see which line has the error, which is usually a missing comma, quote or bracket.

---

## 🧭 Using the site

- Use the **sidebar** to jump to any week or section. ✓ marks the ones you have visited.
- The **Previous / Next** buttons at the bottom of each page take you through the course in order.
- **▶ Edit & run** on any code block lets you change the code and run it on OnlineGDB, or on Python Tutor for short Java 8 programs.
- Every week ends with a **quiz** that explains each answer.
- Open the **📒 Cheat sheet** from the home page for a quick revision of the whole course.

---

✦ Designed by Savy
