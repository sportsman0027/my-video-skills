# Clean AI Video Clips

## Generate without baked text

- Write every prompt to request no readable text, no logos, no labels, no watermarks, and no flags on people, vehicles, buildings, or equipment.

- Describe the scene, the camera, and the motion only, and leave every label, title, caption, and diagram for post production.

- Treat the prompt as a request, not a guarantee, because a generator can still add text or branding even when the prompt forbids it.

- State sizes and counts in the prompt in plain relative terms, such as one planet about half the size of the other, and check that relation in the finished clip.

## Frame out branding

- Prefer a close detail or a distant wide view when a full view keeps attracting logos, labels, or signage.

- Keep uniforms, hulls, modules, and screens out of close readable range unless the script itself requires a readable mark.

- Avoid a straight alignment of planets or objects when the script forbids it, and avoid a morph that changes one subject into another across the clip.

## Verify frames before delivery

- Extract and inspect frames from the start, middle, and end of every clip before you call it done.

- Count objects in the end frame and compare them with the start frame, so a duplicate planet or a changed subject cannot pass unnoticed.

- Read every mark in the frames as if it were final, including small badges, panels, captions, and background signage.

- Reject a clip with readable baked text, branding, a wrong size relation, a morph, or a duplicate subject, and keep the rejected file for comparison.

## Fix, keep, and report

- Sort every rejected clip into rebuild, edit fix, or acceptable note, and work through rebuilds before starting the next part of the film.

- Save the old version before a remake, and replace it only when the new version is clearly better on the frames you inspected.

- Cover a baked caption in post only when a clean cover leaves the picture readable and matches the surrounding style.

- Add all labels, titles, and map text by hand in post, using one consistent style for the whole film.

- Report the finished set with the total count, the total duration, and the exact flaw list, including every clip still on the fix list.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Build a text free still and add slow movement in post when generation keeps adding text to a moving scene.

- Reuse a verified frame or clip for a repeated setting instead of generating the same setting again.

- Ask the user to choose between a clean version and a version with a flaw when the two versions trade one problem for another.

- Pause a batch and return to one by one work when repeated clips in the batch carry the same contamination.
