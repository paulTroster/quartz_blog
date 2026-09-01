<%*
// Prompt for the post title, then derive a URL-friendly slug.
const title = await tp.system.prompt("Blog post title");
const slug = title
  .toLowerCase()
  .replace(/[^a-z0-9]+/g, "-")
  .replace(/^-+|-+$/g, "");
// Move the note into the Quartz-published content folder ("website").
await tp.file.move("/website/" + slug);
-%>
---
title: <% title %>
description: 
created: <% tp.date.now("YYYY-MM-DD") %>
event-date:
tags:
  - blog
draft: true
---
<% tp.file.cursor() %>