<p align="center">
  <img src="assets/loupe.svg" width="120" alt="loupe">
</p>

<h1 align="center">loupe</h1>

<p align="center">
  <b>A calm, precise Git client for looking closely at a repository's history.</b><br>
  The commit graph is the product; the diff is the lens.
</p>

<p align="center">
  <a href="https://github.com/fabiombc-org/loupe-releases/releases/latest"><img alt="Latest version" src="https://img.shields.io/github/v/release/fabiombc-org/loupe-releases?label=latest&color=D4A256&style=flat-square"></a>
  <a href="https://github.com/fabiombc-org/loupe-releases/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/fabiombc-org/loupe-releases/total?color=6FA8DC&style=flat-square"></a>
  <img alt="macOS · Windows · Linux" src="https://img.shields.io/badge/macOS%20·%20Windows%20·%20Linux-16191D?style=flat-square">
  <img alt="MIT license" src="https://img.shields.io/badge/license-MIT-7FC08F?style=flat-square">
</p>

---

## ⬇️ Download

<!-- downloads:start -->
<sub>Version **0.5.0** · [release notes and every file](https://github.com/fabiombc-org/loupe-releases/releases/tag/v0.5.0)</sub>

| | | Get it | Also |
|---|---|---|---|
| 🍎 **macOS** | Apple Silicon (M1 and later) | [**Download .dmg**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe_0.5.0_aarch64.dmg) |  |
| 🪟 **Windows** | 10 and 11, x64 | [**Download installer**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe_0.5.0_x64-setup.exe) | [**.msi**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe_0.5.0_x64_en-US.msi) |
| 🐧 **Linux** | x64 | [**Download .AppImage**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe_0.5.0_amd64.AppImage) | [**.deb**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe_0.5.0_amd64.deb) · [**.rpm**](https://github.com/fabiombc-org/loupe-releases/releases/download/v0.5.0/loupe-0.5.0-1.x86_64.rpm) |
<!-- downloads:end -->

> [!TIP]
> **Install it once, then forget about it.** loupe looks for new versions by itself and offers them with
> their notes: one click on *Update and restart* and you're on the latest. (Settings → About can check now,
> or turn that off.)

### First launch

The builds aren't signed with an Apple or Microsoft certificate yet, so the system asks once before opening them.

<details>
<summary><b>🍎 macOS</b> — “loupe can't be opened” / “is damaged”</summary>
<br>

Open the `.dmg` and drag **loupe** into **Applications**. If macOS refuses to open it the first time, either:

- right-click **loupe** in Applications → **Open** → **Open**, or
- **System Settings → Privacy & Security**, scroll down and choose **Open Anyway**, or
- in Terminal:

  ```sh
  xattr -cr /Applications/loupe.app
  ```

</details>

<details>
<summary><b>🪟 Windows</b> — “Windows protected your PC”</summary>
<br>

Click **More info → Run anyway**. The installer sets up WebView2 if it's missing, and later updates install
over the same copy. Use the same kind of installer (`.exe` or `.msi`) each time, so you don't end up with two
copies.

</details>

<details>
<summary><b>🐧 Linux</b> — AppImage, Debian/Ubuntu, Fedora</summary>
<br>

```sh
# AppImage: no install, updates itself
chmod +x loupe_*_amd64.AppImage && ./loupe_*_amd64.AppImage

# Debian / Ubuntu (22.04 or later)
sudo apt install ./loupe_*_amd64.deb

# Fedora / openSUSE
sudo dnf install ./loupe-*.x86_64.rpm
```

</details>

---

## ✨ What's inside

<table>
<tr>
<td width="50%" valign="top">

### 🌳 A graph you can read
Every branch, remote branch and tag in **stable lanes** with continuous edges. History loads as you scroll,
search finds any commit, and **solo** a branch to see only its story.

</td>
<td width="50%" valign="top">

### 🔍 Diffs as a lens
Unified or **side by side**, just the changes or the whole file, with syntax highlighting. Stage or discard
a **file, a hunk or single lines**.

</td>
</tr>
<tr>
<td valign="top">

### 🗂️ Tabs, groups and an overview
One tab per repository, kept exactly as you left it. Group them (*Work*, *Games*, *Open source*…) and see
every one at a glance: branch, what to push or pull, changes, last commit and **12 weeks of activity**.

</td>
<td valign="top">

### 🔀 Pull requests, reviewed properly
List, review and comment on **GitHub** pull requests without leaving loupe: see what changed **since your last
review**, mark files viewed, draft comments and submit. Create pull requests too.

</td>
</tr>
<tr>
<td valign="top">

### ✦ Claude Code built in <sup>optional</sup>
With [Claude Code](https://claude.com/claude-code) installed, loupe uses **your own sign-in** (no API key) to
**pre-review pull requests**, **summarise commits**, **resolve merge conflicts**, write **commit messages**
and analyse your changes. Watch what Claude is doing, live, in its own tab, and put a review aside while it works.

</td>
<td valign="top">

### 🧩 Conflicts without fear
A three-way **conflict resolver**: pick a side per conflict, both, or edit by hand, and nothing is written
until you save. Cherry-pick, revert, stash and reset are a right-click away.

</td>
</tr>
<tr>
<td valign="top">

### 🔐 Accounts that just work
**GitHub, gitlab.com and self-hosted GitLab**, several accounts per host (personal and work), tokens in the
OS keychain. SSH follows your `~/.ssh/config`; HTTPS asks once.

</td>
<td valign="top">

### 🐧 At home in WSL and the terminal
Open repositories inside **WSL** on Windows and loupe works there natively. A built-in **terminal**
per repository, and the graph refreshes as you run commands.

</td>
</tr>
</table>

<p align="center">
  🎨 <b>Nine colour themes</b>, each dark and light: Graphite · JetBrains · GitHub · One Dark · Dracula · Tokyo Night · Monokai · Nord · Catppuccin
</p>

---

## 💻 Requirements

| | |
|---|---|
| **macOS** | Apple Silicon (M1 or later), macOS 11 Big Sur or later |
| **Windows** | Windows 10 or 11, x64 |
| **Linux** | x64 with WebKitGTK 4.1 (Ubuntu 22.04, Debian 12, Fedora 38 or later) |
| **Claude features** | Optional: [Claude Code](https://claude.com/claude-code) installed and signed in |

No `git` needed: loupe does every Git operation itself.

## 💬 Found a bug? Have an idea?

[Open an issue](https://github.com/fabiombc-org/loupe-releases/issues/new): what you did, what you expected and
your loupe version (Settings → About).

<p align="center"><sub>Made with Rust, Tauri and a magnifying glass · MIT License</sub></p>
