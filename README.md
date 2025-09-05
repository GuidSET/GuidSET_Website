# GuidSET Static Site (GitHub Pages)

A clean, professional landing site for **GuidSET, Inc.** — ready to deploy on GitHub Pages with a custom domain.

## Features
- Modern look with a gradient hero, glass cards, and responsive layout
- No build tools, no dependencies — pure HTML/CSS
- Sections: Hero, Products (ThoraSET/OptiSET), Evidence, Team, News, Contact
- SEO + Open Graph tags
- Optional Netlify form handling baked in (`netlify` attribute)
- 404 page and CNAME placeholder

## How to deploy (GitHub Pages)
1. Create a new GitHub repo. For a user-wide site use `<your-username>.github.io`. For a project site, choose any repo name.
2. Upload all files from this folder to the repo root (including `CNAME` if you want the custom domain).
3. In **Settings → Pages**, set:
   - **Build and deployment** → Source = **Deploy from branch**
   - **Branch** = `main` (or `master`) and `/root` folder
4. Wait for Pages to publish. Your site will be live at `https://<username>.github.io/<repo>/` (or directly at the user domain for `<username>.github.io` repos).

## Custom domain (guidset.com)
- Keep the `CNAME` file with `guidset.com` in the repo root.
- In your DNS provider (currently Squarespace for your domain), add:
  - **CNAME** record for `www` pointing to `<your-username>.github.io`
  - **ALIAS/ANAME** for root (`@`) to `<your-username>.github.io` **or** the A records recommended by GitHub Pages docs.
- In the GitHub Pages **Custom domain** box, enter `guidset.com` (or `www.guidset.com`) and enable **Enforce HTTPS** after the certificate is issued.

> Tip: If you prefer `www.guidset.com` as canonical, set that in the CNAME file and redirect root to `www` via your DNS provider.

## Edit content
Open `index.html` and update text in each section. Update team headshots by replacing files in `/assets` and editing names/roles.

## Style tweaks
Adjust colors in `styles.css` (`:root` tokens) and spacing as desired.

---

**Note:** Products are under development and not for clinical use. Keep disclaimers current for regulatory accuracy.
