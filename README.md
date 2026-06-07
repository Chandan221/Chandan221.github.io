# Chandan – Personal Academic Website

Personal website for **Chandan**, PhD Research Scholar, Department of Electrical Engineering, IIT Delhi.

Modeled after the reference site at <https://web.iitd.ac.in/~eez218527/>, with an added **Papers** section (placed right after *Awards and Honors*) listing publications from [Google Scholar](https://scholar.google.com/citations?user=y23ylpgAAAAJ&hl=en).

## Project structure

```
chandan-website/
├── index.html          # Main single-page site
├── bio.html            # Extended biography page
├── cv.html             # Curriculum vitae (web version)
├── Chandan.pdf         # CV (downloadable PDF)
├── images/
│   ├── Chandan.jpeg            # Profile (large)
│   ├── Chandan_small.jpeg      # Profile (header)
│   ├── iitd_logo.png           # IITD logo (favicon + navbar)
│   ├── rank.jpeg               # Gold-medal proof image
│   ├── qr_code.png             # Office map QR code
│   └── vcard.png               # VCard image
├── .nojekyll           # Disables Jekyll on GitHub Pages
└── README.md
```

## Local preview

Simply open `index.html` in a browser, or run a tiny static server:

```powershell
# from inside the project folder
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. **Create a new GitHub repository** (e.g. `chandan.github.io` for a user site, or any name like `personal-website` for a project site).
2. **Push the contents of this folder** to that repository:

   ```powershell
   git init
   git add .
   git commit -m "Initial commit: personal academic website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repo on GitHub → **Settings** → **Pages**
   - Under *Source*, select **Deploy from a branch**
   - Choose branch **`main`** and folder **`/ (root)`**
   - Click **Save**

4. Your site will be live in 1–2 minutes at:
   - `https://<your-username>.github.io/` (if repo is named `<your-username>.github.io`)
   - `https://<your-username>.github.io/<your-repo>/` (otherwise)

## Customizing

- **Photo / images**: replace files in `images/`.
- **Text / contact info**: edit `index.html` directly.
- **Add a new paper**: copy any `<div class="paper-item">…</div>` block inside the `#papers` section and update the fields.
- **Colors**: tweak the CSS variables `--brand`, `--brand-dark`, `--accent` at the top of the `<style>` block in `index.html`.

## Credits

Inspired by the reference site of Chandan @ IITD. Built with Bootstrap 5 and Font Awesome (loaded from CDN).
