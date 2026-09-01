<%*
// Prompt for the person's name and rename this note to match.
const name = await tp.system.prompt("Person's name");
await tp.file.rename(name);
-%>
---
tags:
  - person
unlisted: true
---
<% tp.file.cursor() %>
