---
date: <% tp.date.now("YYYY-MM-DD") %>
tags:
---
<%* 
let title = await tp.system.prompt("Enter a title for the note:");
await tp.file.rename(title + ".md");  
%>

