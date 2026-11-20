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

## From the Instagram "best skills" videos (added 2026-11-20, security-audited)

Source: three Instagram reels about the best Claude skills for video. Video 1 named bradautomates/claude-video — already forked above (the /watch skill), so nothing new was added from it. Each new repo below was downloaded locally, read and scanned for dangerous patterns before forking. Forking copies code only — nothing runs. Any repo must be re-checked before it is actually run.

- [open-higgsfield-skills](https://github.com/sportsman0027/open-higgsfield-skills) — forked from mojomast/open-higgsfield-skills. A 37-skill pack that turns Claude into a video director driving a local ComfyUI install (FLUX stills, LTX/Wan video) as a free alternative to the paid Higgsfield platform. Audit: CAUTION — no malicious patterns (no telemetry, no credential harvesting); cautions are the Colab runner notebooks it generates, bundled third-party ComfyUI node packs (untrusted until sandboxed), and mixed model-weight licences (LTX-2 is non-OSI). Reality check: 28 of the 37 skills need a GPU (16 GB minimum even for its draft tier), so the generation half cannot run on the current machine; 3 method-only skills were adopted locally instead — **story-bible** (locked character descriptors against design drift), **continuity-check** (shot-join continuity sweep) and **still-qa** (5-axis still judging rubric). Forked as a reference library so the exact audited version stays in the toolkit.

## Skills learned from my own documentary work (added 2026-11-20)

These three skills are not forks — they are method skills written from lessons learned while making this account's own documentary videos (the code-animation film, narration-led assemblies, AI clip clean-up). They live in the `learned-skills/` folder of this repo so the toolkit is complete in one place and portable: any of the owner's Muse accounts connected to this GitHub can install the same methods from here. Note: skills are methods only — they do not carry the agent's memories or the owner's preferences, which stay with each account.

- **code_animation_documentaries** (`learned-skills/code_animation_documentaries/`) — Build flat 2D code-animated documentaries with an original design, voice-measured timing, and filled sound design.
- **narration_led_video_assembly** (`learned-skills/narration_led_video_assembly/`) — Assemble a multipart scripted video to uncut narration, checking scene grouping and picture duration first, delivering parts with an editing map.
- **clean_ai_video_clips** (`learned-skills/clean_ai_video_clips/`) — Generate AI video clips without baked text or branding, verify every clip by its frames, and fix flaws in post before delivery.

### Also from the Instagram "best skills" videos — video 2 (added 2026-11-20, security-audited)

Source: the second Instagram reel of the same batch. Each repo was downloaded locally, read in full and scanned for dangerous patterns before forking; nothing was executed. Any repo must be re-checked before it is actually run.

- [bang-motion](https://github.com/sportsman0027/bang-motion) — forked from bangtutorial/bang-motion (2,804 stars, MIT). A methodology skill for HTML/GSAP motion graphics: mechanical anti-slide tests, mandatory style-brief discipline ("reference = rhythm, not skin"), 19 opener concepts, 6 explainer starters. Audit: CLEAN — helper scripts are localhost-only (static server, Puppeteer frame capture), no binaries, zero dangerous-pattern hits. Not an engine; it is the design-law layer that pairs with HyperFrames. Note: SKILL.md is written in Bahasa Indonesia. Installed locally.
- [huashu-art-motion](https://github.com/sportsman0027/huashu-art-motion) — forked from alchaincyf/huashu-art-motion (7,295 stars, MIT with font/data exceptions noted; actively maintained). The batch's main prize: 36 code-drawn art-style recipes + 9 explainer animation grammars (Kurzgesagt/Vox/whiteboard/3B1B/storytime/kinetic-type/keynote/finance/presenter) as parameterized, frame-accurate local clips via Playwright — no AI models, no per-use cost — plus breakdown.py (measures a reference clip's transitions/beat-grid/motion heatmap), a film_gate.py anti-slideshow delivery gate, and code-synthesized music. Audit: CAUTION (manageable) — network census clean (localhost, Wikimedia Commons for public-domain art, Volcengine's official endpoint only if the user configures his own TTS keys; shipped unconfigured, policies default to "ask"). One catch handled: SKILL.md instructs a git ls-remote version check when used — openly documented with an opt-out; the locally installed copy has it disabled, the fork preserves the original. Docs are in Chinese. Installed locally (49 MB showcase gallery excluded).
- [claude-drawing-skill](https://github.com/sportsman0027/claude-drawing-skill) — forked from cloveric/claude-drawing-skill (313 stars, MIT). A procedural-illustration library in 83 styles using only numpy + Pillow: fully offline, deterministic, no network/subprocess/credential access anywhere (verified by import census and greps). The repo's 320 MB is just example images/GIFs. Reusable brush/medium library (ink wash, impasto, watercolour, paper/newspaper collage, blueprint, chalkboard) with per-style failure checklists and draw-on GIF export — a direct fit for paper-documentary treatments and title cards. Stills, not a video engine. Installed locally (example image bulk excluded; dependencies not pip-installed).

### Considered and deliberately NOT forked from video 2
- **vox-explainer-skill** (CK42BB/vox-explainer-skill, 283 stars, MIT): pure-markdown repo (zero code risk), but the workflow it prescribes runs every stage through the paid Atlas Cloud API with the user's own key (~$3–8 per 60-second film: Seedream keyframes, Gemini image-to-video, xAI TTS, MiniMax music). Conflicts with standing rules: no paid keys without approval, token economy, and no recognizable-AI look (this pipeline is 100% AI-generated, with burned-in subtitles and a music bed by default). The local muse-documentary-engine already covers its pipeline shape for free. Transferable ideas (style-anchor consistency, beat discipline) were captured in the audit summary. Installed locally as reference only, with an explicit do-not-run-without-approval caution.

## Free alternatives to the paid pieces (searched and audited 2026-11-20)

On request, GitHub and skills.sh were searched for free, open-source replacements for the toolkit's two paid-dependent pieces (vox-explainer-skill's paid Atlas Cloud pipeline; the Kling nodes' paid API key), applying the only-new rule: nothing was added that this GitHub or Muse's local skills already cover. 20+ repos fact-checked via the API, 11 cloned and audited; nothing was executed. Honest headline: no new SKILL.md skill was installed — every skill-shaped candidate was paid, platform-bound, or a duplicate. Three repos were forked:

- [OpenMontage](https://github.com/sportsman0027/OpenMontage) — forked from OpenMontageInc/OpenMontage (81,800 stars, AGPL-3.0). A free explainer/documentary platform with a documented zero-API-key mode (Piper TTS + Remotion) — including a documentary-montage pipeline over free/open archives (Archive.org, NASA, Wikimedia Commons) with CLIP search, the one capability absent from both this toolkit and the local engine. Audit: CAUTION — one curl|bash installer string for an optional third-party CLI (never run blindly), AGPL copyleft, and an optional Atlas client among many providers. Forked as a reference/adoption candidate; NOT installed locally (its 141 skills drive its own runtime, and its platform role overlaps the local muse-documentary-engine). Re-check before any run.
- [Wan2.2](https://github.com/sportsman0027/Wan2.2) — forked from Wan-Video/Wan2.2 (Apache-2.0). Free text/image-to-video models — the free Kling replacement, for a future GPU machine only: the 5B model needs at least 24 GB VRAM; it cannot run in the current VM (no GPU). Reference-only.
- [LTX-Video](https://github.com/sportsman0027/LTX-Video) — forked from Lightricks/LTX-Video (Apache-2.0 code). Free text/image-to-video; the 2B model runs on ~8 GB VRAM — the low-VRAM companion for a future GPU machine. Reference-only; check model-weight licences at adoption time.

### Considered and deliberately NOT forked in this search
- **vox-ai-motion-graphics-generator** (363 stars, NO licence): a "vox-style" skill whose every stage runs on the paid MuAPI API with a burned-in watermark — the same paid disease as Atlas under a new name.
- **purffle-shorts** (99 stars, MIT): audit-clean and honestly free (Ollama + Edge-TTS) — the best free MoneyPrinter-style clone found — but a duplicate of the already-forked MoneyPrinterTurbo, so left out under the only-new rule.
- **OpenReels** (246 stars, MIT): polished, but visuals/music are paid Veo/Kling/Lyria; duplicates MoneyPrinterTurbo + the local engine.
- **Pixelle-Video** (30,351 stars, Apache-2.0): clean, but generation needs a local GPU ComfyUI or paid APIs; duplicate.
- **NarratoAI** (11,886 stars, MIT): film-commentary recuts built around sponsored cloud LLM APIs; the local engine's home ground.
- **ShortGPT** (8,185 stars): unmaintained since 2025-02 and a duplicate. Also considered and left: MoneyPrinterV2, Maestro, dramaclaw, topic2manim, ComfyUI itself (reasons in the audit summary).
- Note: the free "faceless-explainer" skill on skills.sh ships inside heygen-com/hyperframes — already owned via the existing hyperframes fork, so no action was needed.

## Real sound design — from the "Claude Sound Design Tips" reel (added 2026-11-20)

Source: an Instagram reel by Aevy Video School arguing that code-synthesized SFX sound fake, and Claude should be given REAL recorded sounds instead. Three tools were named; each was verified live via the GitHub API, downloaded, read and scanned for dangerous patterns before any fork. Nothing was executed.

- [clipwing-skills](https://github.com/sportsman0027/clipwing-skills) — forked from Clipwing/skills (156 stars; scripts declared MIT in its README, no LICENSE file; fork named clipwing-skills because "skills" was already taken). Ships the **real-sfx** skill: sound-design motion videos with REAL recorded sounds from the user's own libraries — never synthesized — placed on the exact frame, replacing baked-in synthesized layers instead of doubling them, returning an MP4 + separate SFX WAV + cue report + self-critique. Audit: no malicious patterns (no telemetry or exfiltration; the one download is the YAMNet model, size-checked; the listen-page is a localhost review server). Bundled: the uisfx pack (936 mp3s, sounds CC0). Honest catch: the video's "619-sound library" is the author's own pack and is NOT in the repo — a main library must be built from free sources (the skill itself points to Freesound CC0, Sonniss GDC, Mixkit, Pixabay). Installed locally as real-sfx. The repo's second skill, hyperframes-to-after-effects, was not installed (no After Effects here).
- [earshot](https://github.com/sportsman0027/earshot) — forked from Leonxlnx/earshot (5,302 stars, MIT). "Ears for coding agents": CPU-only audio analysis — judges whether audio reads as a real recording or code-synthesized, critiques mixes, A/Bs changes, forges sounds in code. Its optional LLM critique uses the user's own Gemini key from the environment (sent in a header only, never stored). Audit: CLEAN. Two method skills installed locally: **earshot** and **real-sound** (a full real-recording soundtrack methodology: Freesound/Mixkit sourcing with licence checks, cue lists, measured QA, mastering, credits and mux). The earshot TOOL itself (uv install + ~1.1 GB of CLAP/AudioSet models) is NOT installed yet — re-check before running.
- **Openverse (WordPress/openverse)** — deliberately NOT forked: it is a 1.6 GB platform monorepo (the Openverse search engine itself), not a skill or tool to possess. Its value is the free website/API for finding CC-licensed sounds and music, used directly as a sound source; recorded here as a reference only, like agent-browser.
