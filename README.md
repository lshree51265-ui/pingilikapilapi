# A Letter For You

A single-page site: a wax-sealed envelope that cracks open on click, revealing
a letter whose words fade in one at a time.

Everything lives in one file, `index.html` — no build step, no dependencies
besides two Google Fonts loaded over CDN.

## Host it on GitHub Pages (free)

1. **Create a repository**
   - Go to [github.com/new](https://github.com/new)
   - Name it whatever you like (e.g. `for-daddy` or `a-letter`)
   - Set it to **Public** (required for free GitHub Pages)
   - Click **Create repository**

2. **Upload the file**
   - On the new repo's page, click **"uploading an existing file"**
   - Drag in `index.html` (and this `README.md` if you want)
   - Click **Commit changes**

3. **Turn on Pages**
   - Go to the repo's **Settings** tab
   - In the left sidebar, click **Pages**
   - Under **Build and deployment → Source**, choose **Deploy from a branch**
   - Under **Branch**, choose `main` and folder `/ (root)`, then **Save**

4. **Wait ~1 minute, then visit your link**
   - GitHub will show a banner: *"Your site is live at
     `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`"*
   - That's the link you can send.

### Using git from the command line instead (optional)

```bash
git init
git add index.html README.md
git commit -m "the letter"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Then repeat step 3 above to switch on Pages.

## Customizing

- **Letter text** — edit the `greeting` and `paragraphs` array near the
  bottom of `index.html`, inside the `<script>` tag.
- **Reveal speed** — change `wordStep` (seconds between each word appearing).
- **Colors** — all colors are CSS variables at the top of the `<style>`
  block (`--wax-red`, `--parchment`, `--ink`, etc).
- **Seal emblem** — the pacifier is drawn as inline SVG in the `.wax-seal`
  block; swap the `<g>` shape there for a different icon if you ever want to.

Works on mobile and desktop, respects "reduce motion" accessibility settings,
and is keyboard-operable (Tab to the envelope, press Enter/Space to open).
