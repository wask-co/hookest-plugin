<p align="center">
  <a href="https://hookest.com">
    <img src="assets/banner.png" alt="Hookest for Claude Code: viral hooks, inside Claude Code" width="100%">
  </a>
</p>

<p align="center">
  <a href="https://hookest.com"><img src="https://img.shields.io/badge/hookest.com-FF3D71?style=flat-square&labelColor=1E1440" alt="hookest.com"></a>
  <img src="https://img.shields.io/badge/Claude%20Code-plugin-FF3D71?style=flat-square&labelColor=1E1440" alt="Claude Code plugin">
  <img src="https://img.shields.io/badge/MCP-remote-FF3D71?style=flat-square&labelColor=1E1440" alt="Remote MCP">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-FF3D71?style=flat-square&labelColor=1E1440" alt="MIT license"></a>
</p>

<p align="center">
  <b>Find real viral Instagram Reels hooks, see which categories are gaining,<br>and write new opening lines for your ads, without leaving Claude Code.</b>
</p>

<br>

## Install

Run these two commands inside Claude Code:

```
/plugin marketplace add wask-co/hookest-plugin
/plugin install hookest@hookest
```

The first time a Hookest tool runs, your browser opens so you can sign in to
Hookest and approve access. A free account is enough to start.

<br>

## How it works

<p align="center">
  <img src="assets/how-it-works.png" alt="1. Ask in plain words. 2. Claude searches the Hookest library. 3. You get a brief grounded in real examples." width="100%">
</p>

<br>

## What's inside

### Skills

Skills run on their own when your request matches. You don't need to name them.

| | Skill | What it does |
|---|---|---|
| 🔎 | **`hook-research`** | Pulls real hooks for your product or niche, opens the best ones for metrics and comment insights, and writes a short brief |
| ✍️ | **`write-hooks`** | Writes 5 to 8 hooks for your product, each tied to a real library example, and checks how long each one takes to say |
| 🎬 | **`video-check`** | Uploads a video from your machine to the Hookest Virality Predictor, returns its 0 to 100 opening score and turns it into concrete edits |
| 👀 | **`competitor-watch`** | Reports new posts and follower changes for the accounts you track, and adds new ones only after you confirm |
| 🗂️ | **`swipe-file`** | Reviews your saved hooks, finds more like them, and gets the hook clip or Hook Editor link |

### Commands

| Command | What it does |
|---|---|
| `/hookest:hooks <topic>` | Real viral hooks for a topic |
| `/hookest:write <product>` | New hooks for your product |
| `/hookest:score <video.mp4>` | Score your video's opening before you post |
| `/hookest:trends [window]` | Categories gaining or losing momentum |
| `/hookest:weekly [category]` | This week's new viral hooks |
| `/hookest:competitors [@handle]` | What changed for your competitors |
| `/hookest:saved` | Your saved hooks |
| `/hookest:account` | Your plan and remaining quota |

### Hookest MCP

All 29 Hookest tools, including `find_hooks`, `get_hook`, `find_similar_hooks`,
`discover_trends`, `generate_hooks`, the Virality Predictor, saved hooks and
creator tracking. Ask in plain words and Claude picks the right one.

<br>

## Try it

```
What hooks are working for restaurant Reels right now?
```
```
Write 5 hooks for my burger place Reel. Audience: students.
```
```
/hookest:score ~/Movies/launch-reel.mp4
```
```
/hookest:weekly
```

<br>

## Good to know

- **Instagram Reels only.** The library does not cover TikTok or YouTube yet.
- **Quota.** `generate_hooks`, `lookup_creator` and `search_creators` use your
  Hookest quota. The skills ask you before calling them.
- **Video scoring.** Your first analysis is free, then it needs Hookest Pro.
  Uploads are mp4, up to 32 seconds and 40 MB; `/hookest:score` offers to trim
  longer videos to their opening (it needs `ffmpeg` for that).
- **Library items only.** Hookest analyses hooks in its library. It cannot
  analyse any Instagram URL you paste.

<br>

## Use Hookest in other apps

The same server works in Claude, ChatGPT and Gemini. Add this address as a
custom connector:

```
https://hookest.com/mcp
```

<br>

<p align="center">
  <a href="https://hookest.com"><img src="assets/mark.svg" alt="Hookest" height="36"></a>
  <br>
  <sub>Made by <a href="https://hookest.com">Hookest</a> · MIT licensed</sub>
</p>
