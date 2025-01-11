<%* 
let title = await tp.system.prompt("Enter a title for the note:");
await tp.file.rename(title + ".md");  
%>

<%*
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
  tags: ${[selectedTag]}$
  ---` 

  const dv = app.plugins.plugins.dataview.api;
  const dateLimit = this.date;

  const nextNote = dv.pages("" + selectedTag)
  .where(p => p.date && p.date > dateLimit)
  .sort(p => p.date, 'asc')
  .limit(1);
  
  const prevNote = dv.pages("" + selectedTag)
  .where(p => p.date && p.date < dateLimit)
  .sort(p => p.date, 'asc')
  .limit(1);


  if (prevNote && prevNote.length > 0) {
    const prevLink = prevNote[0].file.link;
    tR += `[<- Prev](${prevLink}) `;
  } else {
    tR += `End `;
  }

  if (nextNote && nextNote.length > 0) {
    const nextLink = nextNote[0].file.link;
    tR += `| [Next ->](${nextLink})\n`;
  } else {
    tR += `| Next -> [No more notes]\n`;
  }

 tp.frontmatter["tags"] += selectedTag;
%>









