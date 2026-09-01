<%*
// Prompt for the thing's name and rename this note to match.
const name = await tp.system.prompt("Thing's name");
await tp.file.rename(name);
-%>
---
tags:
  - thing
unlisted: true
---
<% tp.file.cursor() %>
