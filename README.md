# Academic Website — GitHub Pages

A lightweight academic website for **Isaiah Gangadeen**.

This version deliberately uses **plain HTML/CSS/JavaScript** instead of Jekyll, Ruby, or `al_folio_core`.
That means there is no theme gem to install and no GitHub Actions build step is required.

## Files

- `index.html` — homepage
- `research.html` — papers and research projects
- `teaching.html` — teaching
- `cv.html` — web CV
- `contact.html` — contact and profile links
- `404.html` — custom error page
- `assets/css/style.css` — all styling
- `assets/js/main.js` — mobile navigation + footer year
- `.nojekyll` — tells GitHub Pages not to run Jekyll

## Publish on GitHub Pages

### Option 1: repository named `YOURUSERNAME.github.io`

1. Create a GitHub repository named exactly:
   `YOURUSERNAME.github.io`
2. Upload all files in this folder to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/(root)**
5. Save.

Your site will appear at:
`https://YOURUSERNAME.github.io`

### Option 2: any repository name

For a repository such as `academic-website`, use the same Pages settings.
GitHub will publish it at:

`https://YOURUSERNAME.github.io/academic-website/`

All links in this template are relative, so it works in either configuration.

## Before publishing

Search the project for `href="#"` and replace those placeholders with your real:
- Google Scholar URL
- ORCID URL
- GitHub profile URL
- LinkedIn URL

### Add a profile photo

Place a photo at:

`assets/img/profile.jpg`

Then replace this line in `index.html`:

```html
<div class="avatar-placeholder" aria-label="Profile photo placeholder">IG</div>
```

with:

```html
<img class="profile-photo" src="assets/img/profile.jpg" alt="Isaiah Gangadeen">
```

Then add to `assets/css/style.css`:

```css
.profile-photo {
  width: 112px;
  height: 112px;
  border-radius: 50%;
  object-fit: cover;
}
```

### Add your CV PDF

Create:

`assets/cv/isaiah-gangadeen-cv.pdf`

Then in `cv.html`, change:

```html
<a class="button primary disabled" href="#" aria-disabled="true">Download PDF CV</a>
```

to:

```html
<a class="button primary" href="assets/cv/isaiah-gangadeen-cv.pdf">Download PDF CV</a>
```

## Custom domain

If you later use a custom domain, add a file called `CNAME` containing only the domain, for example:

`isaiahgangadeen.com`

Then configure the same domain under GitHub **Settings → Pages**.

## Why `.nojekyll`?

GitHub Pages normally recognizes Jekyll conventions. `.nojekyll` tells GitHub to serve these files directly.
This avoids the `al_folio_core theme could not be found` error completely.
