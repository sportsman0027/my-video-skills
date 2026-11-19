# my-video-skills

My video toolkit for Muse: documentary, animation, map animation and motion graphics tools and notes.

This is my master repo. The actual tools live in my forks (below); this repo indexes them and holds my own notes and project code.

## My forks

### Documentary / programmatic video
- [remotion](https://github.com/sportsman0027/remotion) — forked from remotion-dev/remotion. Make videos programmatically with React. Main tool for documentary and motion-graphics videos.
- [video-shotcraft](https://github.com/sportsman0027/video-shotcraft) — forked from Vincentwei1021/video-shotcraft. AI video skill with Remotion shot recipes, beat sync and sound design.

### Animation
- [manim](https://github.com/sportsman0027/manim) — forked from ManimCommunity/manim. Python framework for explanatory animations (ManimCommunity edition).

### Map animation
- [map-animation-skills](https://github.com/sportsman0027/map-animation-skills) — forked from iart-ai/map-animation-skills. Animated map skills for AI coding agents: routes, zoom-to-location, data-driven map animations. Note: small/new repo — test before relying on it.

### Motion graphics
- [movis](https://github.com/sportsman0027/movis) — forked from rezoo/movis. Python library for video editing, presentation videos and motion graphics.

## How these are used
Muse reads a fork when a video project needs it, sets the code up locally, and renders with it. Forking alone does not generate video — the setup and render happen per project.

## From the Claude-skills reel (added 2026-11-19, security-audited)

Source: an Instagram reel counting down the most-installed Claude skills (skills.sh leaderboard). Each skill's SKILL.md was read in full and scanned for dangerous patterns (hidden downloads, credential/token access, eval, destructive commands, external URLs) before forking. Forking copies code only — nothing runs, and the original authors get no access to this account. Any skill must be re-checked before it is actually run.

- [skills](https://github.com/sportsman0027/skills) — forked from vercel-labs/skills. Contains **find-skills** (the reel's #1, ~4.1M installs): discovers and installs other agent skills via the official `npx skills` CLI. Audit: SKILL.md clean; note its job is installing other skills, so every future install needs its own check first.
- [hyperframes](https://github.com/sportsman0027/hyperframes) — forked from heygen-com/hyperframes. Contains **HyperFrames** (the reel's #3): write code (HTML), get a video. Most relevant to documentary/animation work here. Audit: main and CLI SKILL.md files clean, no external URLs.
- [mattpocock-skills](https://github.com/sportsman0027/mattpocock-skills) — forked from mattpocock/skills. Contains **grill-me** (the reel's #2): a plan/design stress-test interview. Audit: SKILL.md is a two-line prompt wrapper, no code at all — lowest risk of the set.

### Not forked (deliberately)
- **agent-browser** (vercel-labs/agent-browser, the reel's #4): SKILL.md audited clean, but the tool gives an AI full browser control — the highest capability/risk surface of the set — and it is not needed for video work (Muse already has a browser). Listed here only; can be forked in minutes if ever needed.

## Kling AI (added 2026-11-19, security-audited)

- [ComfyUI-KLingAI-API](https://github.com/sportsman0027/ComfyUI-KLingAI-API) — forked from KlingAIResearch/ComfyUI-KLingAI-API. The Kling team's own ComfyUI custom node for the official Kling AI API: Text2Video, Image2Video, image generation, lip sync and effects nodes — the motion-graphics route into Kling from a node workflow. Audit before forking: code read and scanned — it talks only to the official endpoints (api.klingai.com / api-beijing.klingai.com), signs requests locally with the user's own API key (kept in a local config.ini, empty by default), no eval/exec/subprocess, requirements are standard libraries only (pyjwt, httpx, pydantic, pillow, numpy). Notes: running it needs a paid Kling AI API key, and re-check before any run. Rejected alternatives: reverse-engineered Kling API repos (account-ban risk) and spammy "motion prompts" API-gateway repos.

## From the GitHub-trending video (added 2026-11-19, security-audited)

Source: a Portuguese short listing 4 GitHub repos trending that week. Each repo was downloaded locally, read in full and scanned for dangerous patterns before forking. Forking copies code only — nothing runs. Any repo must be re-checked before it is actually run.

- [MoneyPrinterTurbo](https://github.com/sportsman0027/MoneyPrinterTurbo) — forked from harry0703/MoneyPrinterTurbo. Give it a topic: it writes the script, finds footage, narrates, adds captions and music, and assembles a finished short video (Python/Streamlit + MoviePy). Audit: clean — subprocess is ffmpeg only; every external host is a user-keyed provider API. Running needs an LLM API key plus a free Pexels key; no GPU. Note: use official providers only, not the sponsored reseller APIs its README promotes.
- [voicebox](https://github.com/sportsman0027/voicebox) — forked from jamiepine/voicebox. Local voice studio: 8 TTS engines (incl. Kokoro), zero-shot voice cloning from a few seconds of audio, 23 languages, runs on your own machine. Audit: clean — the eval hits are PyTorch model.eval(); suspicious-looking hosts appear only in SSRF test fixtures; the one optional cloud auth endpoint can be overridden to stay fully local. Running on Linux needs Docker or a source build plus HuggingFace model downloads; GPU recommended. Note: clone only voices you have the right to use.
- [claude-video](https://github.com/sportsman0027/claude-video) — forked from bradautomates/claude-video. The /watch skill: give it a video link and it extracts timestamped frames (scene-change detection) plus a transcript and writes an analysis report — the tool for studying a reference video frame by frame. Audit: clean — list-form subprocess only (yt-dlp/ffmpeg); hosts are Google/Groq/OpenAI with the user's own keys; one optional, user-triggered WhisperX installer downloads Astral's official uv installer. Also installed locally as a Muse custom skill (~/workspace/custom-skills/claude-video); its scripts have not been run yet.
- [t3code](https://github.com/sportsman0027/t3code) — forked from pingdotgg/t3code. One screen for several coding agents (Claude Code, Codex, Cursor, OpenCode): hand tasks between agents mid-conversation. Audit: clean — telemetry is local and env-gated; the official install is a checksum-verified curl|sh (not run) and pnpm install would trigger a prepare hook (not run). Not a video tool — kept for agent orchestration.

## From the "Secret GitHub Repos for Claude" reel (added 2026-11-19, security-audited)

Source: @sybrainofficial's reel counting down 10 GitHub repos for Claude. Each repo was identified by name + description + star count, downloaded, its README/SKILL.md read, and scanned for dangerous patterns (curl|bash, eval, base64 decode-exec, credential exfiltration, rm -rf, sudo, mining, unknown-host calls) before forking. Forking copies code only — nothing runs. Full audits: local `~/workspace/github-tools-10/SUMMARY.md`.

- [rea](https://github.com/sportsman0027/rea) — forked from morluto/rea. REA: reverse-engineer anything with agents (MCP server + skill driving Ghidra/IDA/Hopper). Audit: CAUTION — powerful dual-use tool, curl|bash installer by design; server not installed locally, only its workflow skill copied. Lawful/owned-software use only.
- [ponytail](https://github.com/sportsman0027/ponytail) — forked from DietrichGebert/ponytail. "Laziest senior dev" skill: smallest complete change, YAGNI ladder. Audit: CLEAN (skills); its plugin hooks run Node if plugin-installed — skill folders only were installed locally.
- [hallmark](https://github.com/sportsman0027/hallmark) — forked from Nutlope/hallmark. Anti-AI-slop design skill (Together AI): 50 material themes + browser lint against machine-made tells. Audit: CLEAN.
- [impeccable](https://github.com/sportsman0027/impeccable) — forked from pbakaus/impeccable. Design vocabulary/polish/audit commands for coding agents. Audit: CAUTION — its launcher downloads a binary on first run (stated in its SKILL.md); launcher not run locally.
- [ui-ux-pro-max-skill](https://github.com/sportsman0027/ui-ux-pro-max-skill) — forked from nextlevelbuilder/ui-ux-pro-max-skill. Design-intelligence skill: searchable local database of styles, palettes, font pairings and UX rules (+ 6 sibling skills). Audit: CLEAN.
- [diagram-design](https://github.com/sportsman0027/diagram-design) — forked from cathrynlavery/diagram-design. Editorial technical diagrams (45 types) as self-contained HTML+SVG in your brand. Audit: CLEAN.
- [humanizer](https://github.com/sportsman0027/humanizer) — forked from blader/humanizer. Skill that removes AI-writing tells from prose. Audit: CLEAN — markdown only, lowest risk of the set.
- [onyx](https://github.com/sportsman0027/onyx) — forked from onyx-dot-app/onyx. Open-source AI platform: chat with your own documents, works with every LLM. Audit: CAUTION — a full self-hosted app (not a skill); downloaded/audited only, not deployed.
- [last30days-skill](https://github.com/sportsman0027/last30days-skill) — forked from mvanhorn/last30days-skill. Research skill: what people actually said in the last 30 days across Reddit, X, YouTube, HN, Polymarket and the web. Audit: CAUTION — clean code, but by design sends queries to third-party APIs with your own keys and can opt-in to browser cookies for X.
- [Scrapling](https://github.com/sportsman0027/Scrapling) — forked from D4Vinci/Scrapling. Adaptive web-scraping framework (single request → full crawl) + official agent skill. Audit: CLEAN; library not pip-installed locally, skill copied. Respect site terms when scraping.
