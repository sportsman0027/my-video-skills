# Code Animation Documentaries

## Invent an original design before you build

- Study a reference only for story, pacing, beats, and the quality bar such as resolution, type weight, motion energy, and sound fullness.

- Invent a different visual language before rendering and name its palette, world, typography, and character treatment in the plan.

- Show that design plan to the user before building on new reference audio and name what is deliberately different from the reference.

- Keep the quality bar from the reference and never copy its visual language even when the user challenges you to beat it.

- Follow an explicit same to same recreation order when the user gives one and state the fidelity ceiling before you start.

## Measure word timings from the voice

- Build the timing map from the supplied voice before animating text or beats.

- Find speech chunks with fine silence detection and place onsets with a short window RMS envelope inside each chunk.

- Save the word timing table beside the master and use its measured beats for stamps, reveals, and impacts.

- Treat intra chunk onsets as approximate within about 0.1 to 0.2 seconds and correct any beat that lands visibly off the voice.

- Never use proportional estimates across the whole narration when a voice file is available.

## Build the sound bed and event sound

- Keep a continuous sound bed under the narration so pauses stay filled instead of falling to raw silence.

- Match event sound to on screen events such as stamps, impacts, cracks, sweeps, and glitches.

- Keep event sound and the bed below the voice so narration stays intelligible.

- Mix a loud clean master and check pause levels and peaks before delivery.

## Render, verify, and deliver with flaws disclosed

- Render at the promised resolution and keep one consistent design language across every scene instead of hopping between styles.

- Give planets and objects procedural texture instead of flat colour where texture carries the shot.

- Inspect frames from every scene before delivery and fix a delivered part before starting the next part when a fix is ordered.

- Deliver the master beside a smaller review copy when the master is large.

- Disclose every remaining flaw in the same delivery and name its scene and location.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Confirm the design plan and timing method before costly generation and flag the cost before running large parallel builds.

- Prefer code animation for flat 2D documentary work where it fits and reserve AI generation for footage code cannot produce.
