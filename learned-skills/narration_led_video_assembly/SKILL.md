# Narration Led Video Assembly

## Measure narration before you promise a runtime

- Record the first scene in the chosen narrator voice and measure its exact duration.

- Divide the recorded words by the recorded minutes to get the actual pace and use that pace for the remaining script instead of an assumed pace.

- Compare total narration duration with total picture duration before assembly and list every scene where narration outruns picture.

- Give a total runtime only after that comparison and revise the estimate after the first part is rendered when rendering proves heavier than expected.

## Check scene grouping before you render

- Map every picture segment to the script scene that will play over it and write the mapping down before rendering.

- Compare the picture grouping with the script grouping and flag every segment where the topic of the picture differs from the topic of the narration.

- Present each mismatch to the user before rendering with the choice to reorder picture to match narration or to keep the original order with the offset disclosed.

- Keep the original picture order unchanged unless the user chooses a reorder.

## Retime picture to narration

- Keep every narration word and keep the narration speed unchanged.

- Stretch picture to narration duration with slow holds or slow movement where a scene needs more time.

- Add a scene title card at the start of each scene in one consistent style for the whole film.

- Add a main title only on a segment the user or the shot list left blank for that purpose.

- Verify that the finished total equals the narration total and that no narration is cut or overlapped.

## Deliver in parts with an editing map

- Deliver each finished part as soon as it is verified instead of holding all parts for one final delivery.

- Report progress from disk state by naming parts finished, renders still remaining, and a revised time estimate when the user asks how long is left.

- Cancel a scheduled delivery report when the user is already awake and the delivery has already been given in chat.

- Send an editing map with the delivery that lists part durations, slow hold sections, topic offsets, title card positions, and flawed shots left as is with their part locations.

- Send the separate shot masters and narration files with the parts so the user can reorder shots in a later edit.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Offer a shorter review copy beside each master so the user can check a part quickly before opening the large master file.

- Keep the first rendered part as the timing sample for later parts instead of reusing the first optimistic estimate for the whole film.
