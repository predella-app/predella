# Predella (beta)

*A predella is the row of small paintings beneath the main panel of an altarpiece: the gallery under
the big picture.*

**A gallery, viewer and note editor for your folders.** See your newest files as big pictures, open
anything without leaving the app, and write and link your notes, all in one window.

Free to use. Linux for now (Ubuntu, Debian, Linux Mint, Pop!_OS, Fedora). This is a **beta**: expect rough
edges, and tell us about them.

## What it does

- **A gallery of your newest files**, with real previews: pictures (iPhone HEIC too), PDFs, web pages,
  spreadsheets, Word and PowerPoint files, text.
- **A viewer** for all of them, with zoom, full screen and stepping through a folder.
- **A Markdown note editor** with live formatting, autosave, `[[links]]`, "Linked from" and a graph of
  how your notes connect.
- **Search inside your files**, a folder view with sorting, and a split view for two files side by side.
- **Home**: one picture tile per project folder.

## Install

1. Download **`predella_0.3.4_amd64.deb`** from the [latest release](../../releases).
2. Double-click it. App Center opens: click **Install**.
3. Open **Predella** from your apps. The first time, it asks which folders to show. Change them
   later: press **Alt**, then **File → Choose Folders**.

Or download and install it in one go: paste this into a terminal (it asks for your password).

```
cd ~/Downloads && wget -O predella_0.3.4_amd64.deb https://github.com/predella-app/predella/releases/download/v0.3.4/predella_0.3.4_amd64.deb && sudo apt install ./predella_0.3.4_amd64.deb
```

### Fedora

Download **`predella-0.3.4.x86_64.rpm`** from the [latest release](../../releases) and double-click it
(Software opens: click **Install**), or paste this into a terminal:

```
cd ~/Downloads && curl -fLo predella-0.3.4.x86_64.rpm https://github.com/predella-app/predella/releases/download/v0.3.4/predella-0.3.4.x86_64.rpm && sudo dnf install ./predella-0.3.4.x86_64.rpm
```

## Updates

Predella tells you when a new version is out (and **Help → Check for Updates**). Click **Install and
Restart**: it downloads the new version, checks it, asks for your password, installs it and restarts.
Your folders and settings stay. (Versions before 0.3.2 only open the download page. On Fedora, Predella
opens the download page: install the new `.rpm` the same way as the first one.)

## With an AI assistant

If an AI assistant keeps notes on your projects, Predella can show where each one stands on its Home
tile: what's happening now, countdowns to dates, and how many things are waiting on you. It reads a
file named `CurrentState.md` in each project folder. Paste this into your assistant's instructions
(`AGENTS.md` for most coding assistants, `CLAUDE.md` for Claude Code, or a chat assistant's custom
instructions):

```
Keep a file named CurrentState.md in each project folder:
- "## Now": one or two bullets on what is happening right now.
- "## Open items": one bullet per open task. Put its date in it when it has one (2026-12-04).
- When a task needs me, write "waiting on me" in that bullet.
- Only what is true now. Move finished items to Completed.md in the same folder.
```

Without these files, Predella works the same, just without the status on Home.

## Privacy

Everything stays on your computer. No account, no tracking, no data collection. Predella reads the
folders you pick and changes nothing in them, except a note's text when you edit it. Predella itself
contacts only GitHub, to see whether a newer version exists (turn that off with
`"checkForUpdates": false` in `~/.config/file-gallery/config.json`). A web page you open in Predella
may load its own pictures and scripts from the internet, as it would in a browser.

## Problems and ideas

[Open an issue](../../issues), or write to hello@predella.org. Please include the version (**Help → About Predella**).

## License

Free to use; not open source. See [LICENSE.txt](LICENSE.txt). Predella is built with Electron,
Python and other open-source components, each under its own license: **Help → Third-Party Licenses**
in the app, or `/usr/share/doc/file-gallery/` after installing. Source code for the LGPL components is
attached to each release.

## Coming later

Fedora and other Linux packages, automatic updates, Windows and Mac.
