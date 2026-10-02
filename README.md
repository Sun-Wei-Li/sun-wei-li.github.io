# Teacher Ben — ESL Teacher Portfolio

Live site: https://sun-wei-li.github.io

A simple, static one-page portfolio site. No build tools, no backend —
just two files:

- `index.html` — the page content (text, sections, placeholders)
- `styles.css` — all the styling (colors, fonts, layout)

## Editing in VS Code

1. Open this folder in VS Code (`File > Open Folder...`)
2. Edit `index.html` to change text, or swap a placeholder for real content:
   - Photo placeholders (`<div class="photo-slot">` / `<div class="img-slot">`)
     → replace with `<img src="your-photo.jpg" alt="...">`
   - Video placeholders (`<div class="video-slot">`)
     → replace with a YouTube embed, e.g.:
     ```html
     <iframe width="100%" height="100%" src="https://www.youtube.com/embed/VIDEO_ID"
             title="YouTube video" frameborder="0" allowfullscreen></iframe>
     ```
   - Any `[bracketed text]` → replace with your real info
3. Edit `styles.css` to change colors, fonts, or spacing. Colors are defined
   once at the top under `:root { ... }` — change a value there and it
   updates everywhere on the site.
4. To preview locally: just double-click `index.html` to open it in your
   browser, or in VS Code install the **Live Server** extension and click
   "Go Live" for auto-refresh while you edit.

If you add photos or videos, put image files in this same folder (or an
`images/` subfolder you create) and reference them with a relative path,
e.g. `<img src="images/classroom.jpg">`.

## Hosting for free on GitHub Pages

1. Create a new repository on GitHub (e.g. `my-portfolio`) — public repos
   get free Pages hosting.
2. Upload these files to the repository (drag-and-drop on the GitHub
   website works fine, or use `git`):
   ```
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/my-portfolio.git
   git push -u origin main
   ```
3. On GitHub, go to your repo's **Settings > Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch",
   choose the `main` branch and `/ (root)` folder, then click **Save**.
5. After a minute or two, your site will be live at:
   ```
   https://YOUR-USERNAME.github.io/my-portfolio/
   ```

To use a custom domain (like `teacherben.com`) instead, add a `CNAME`
file with your domain name, and point your domain's DNS at GitHub Pages —
GitHub's Pages settings page will show you the exact records to add once
you type your domain in there.

## File overview

| File | Purpose |
|---|---|
| `index.html` | Page structure and content, organized into commented sections (Hero, Philosophy, Classroom, Lessons + videos, Teacher Tips, Experience, Certificates, Testimonials [hidden], Contact) |
| `styles.css` | All styling, organized into the same commented sections plus shared theme variables at the top |
| `README.md` | This file |
| `.gitignore` | Keeps the large `.mp4` files and Word temp files out of GitHub (the videos are embedded from YouTube) |
| `images/` | Privacy-cleaned classroom photos used on the site (originals in `In the Classroom photos/` are not uploaded) |
| `Recent Certificates/` | Certificate PDFs linked from the Certificates section; `previews/` holds the thumbnail images shown on the page |
