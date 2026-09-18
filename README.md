# My Portfolio Site

A simple, hand-editable portfolio. No build tools, no framework — just open the
HTML files in a text editor, change the words, and save.

## Files at a glance

| File | What it is |
|------|-----------|
| `index.html` | Home page — intro, projects area (currently "coming soon"), and the custom-request form |
| `about.html` | About page + "About this site" |
| `project-template.html` | The page to copy for each new project (has `[INSERT]` placeholders) |
| `style.css` | All the styling (colors, spacing, fonts) |
| `images/` | Put project photos and thumbnails here |
| `models/` | Put your 3D models (`.glb` files) here |

> No real projects yet: the homepage shows a "coming soon" state. When you have a
> project, the easiest thing is to just tell Claude the details and it builds the
> page and adds the card for you.

## Common things you'll want to do

### Change text
Open any `.html` file, find the sentence, type over it, save. Reload the page in
your browser. In the template, `[INSERT ...]` markers show exactly where your words go.

### Change the colors
Open `style.css`. The block at the very top (`:root { ... }`) controls the whole
site's colors. Change `--accent` to recolor links and buttons everywhere.

### Add a new project
1. Make a copy of `project-template.html` and rename it, e.g. `project-lamp.html`.
2. Replace every `[INSERT ...]` and `[PROJECT NAME]` placeholder with your words.
3. In `index.html`, delete the `.empty-state` block and un-comment the example
   card in the `<div class="grid">`; point its `href` at your new page.
   - Keep the `<span class="printable-dot">` line if it's 3D printable; delete it if not.

### Add a 3D model
1. In Fusion 360, export your part as a **`.glb`** file (File → Export → glTF/GLB).
2. Drop the file into the `models/` folder.
3. In the project page, find the `<model-viewer>` tag and change
   `src="..."` to `src="models/your-file.glb"`.

The template points at a sample model so you can see the viewer working —
just swap in your own file.

### Use a photo instead of a 3D model
In `project-template.html`, the "Final result" section has a commented-out photo
option. Delete the `<model-viewer>` block and use:
`<img class="result-photo" src="images/your-photo.jpg" ...>`

### Make the contact form actually email you
1. Sign up (free) at https://formspree.io
2. Create a form; it gives you a URL like `https://formspree.io/f/abcdwxyz`
3. In `index.html`, find `action="https://formspree.io/f/YOUR_FORM_ID"` and paste
   your URL in place of `YOUR_FORM_ID`. Done — submissions arrive in your email.

## Putting it online (later)
When you're ready, free hosts like **Netlify**, **GitHub Pages**, or **Cloudflare
Pages** will host this folder as a live website. Ask and I can walk you through it.
