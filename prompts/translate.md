# Translation Prompt

Read everything in `/raw`. Update or create matching markdown files in `/wiki` so the wiki reflects what's in `/raw`. Then move each processed file from `/raw` to `/archive`.

## General Rules
- One topic per file in `/wiki`, kebab-case filenames.
- Merge into existing entries, never overwrite blindly.
- Link related entries with relative markdown links.
- Move processed files from `/raw` to `/archive` with the same filename. Never delete.
- If a raw note or asset relates to a folder in `/projects`, also surface it in that project's notes (add reference, embed, or note in the project README).
- When uncertain, note it inside the entry rather than guessing.

## Handling Non-Text Files (Images, Binaries, etc.)
- For **images** (PNG, JPG, etc.): Use vision analysis tools to generate a clear description, alt text, and any visible text/logos. Create a dedicated wiki entry describing the asset (purpose, visual details, dimensions if available, usage).
- For **other file types** (PDFs already handled, videos, audio, archives, etc.): Note file type, size, and infer purpose from filename/context. Create a concise wiki entry.
- Always produce a `.md` wiki entry for discoverability and linking, even for binary assets.
- If the asset belongs to a project, add a reference or embed in the relevant `/projects/<name>/README.md` (e.g. "Logo: ![logo](relative/path)").
- Preserve original filename when moving to `/archive/`.