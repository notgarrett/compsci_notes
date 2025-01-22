<%* 
let title = await tp.system.prompt("Enter a title for the note:");
await tp.file.rename(title);  
  // Get all unique tags from the vault
  const allTags = new Set();
  const filesPrev = app.vault.getMarkdownFiles();
  const blacklistedFolders = ['Excalidraw'];

  const files = filesPrev.filter(file => {
	  return !blacklistedFolders.some(folder => file.path.startsWith(folder));
  })
  
  // Iterate over all files and extract tags
  for (const file of files) {
    const content = await app.vault.read(file);
    const matches = content.match(/#[a-zA-Z_]+/g); // Regex to find tags
    if (matches) {
      matches.forEach(tag => allTags.add(tag));
    }
  }

	console.log(allTags);
  // Convert the Set to an array and sort it
  const sortedTags = Array.from(allTags).sort();
	console.log(sortedTags);

  // Prompt user to choose a tag
  const selectedTag = await tp.system.suggester(sortedTags, sortedTags[0]);

// This code here sets up our properties window at the start of a note.
 tR += `---
date: ${tp.date.now("YYYY-MM-DD")}$
tags: ${[selectedTag]}$---`;
%>









