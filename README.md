# RIDA website

Static website for **Runge Infectious Disease Analytics (RIDA)**, the professional technical platform of infectious-disease epidemiologist Dr Manuela Runge.

The site is intentionally lightweight. It uses plain HTML, CSS and a small JavaScript file, with no framework, database or installation step.

## Files

- `index.html` — all visible website content and links
- `styles.css` — colours, typography, layout and responsive design
- `script.js` — automatically updates the copyright year
- `.github/workflows/pages.yml` — publishes the site to GitHub Pages after pushes to `main`
- `AGENTS.md` — guidance for working on the site with Codex or another coding assistant
- `.nojekyll` — tells GitHub Pages to publish the files without Jekyll processing

## Edit in Cursor

1. Extract the downloaded ZIP.
2. Open Cursor.
3. Select **File → Open Folder** and choose the `RIDA-website` folder.
4. Edit the wording in `index.html`.
5. Save the file and open `index.html` in a browser to inspect it.

For automatic browser refresh, install a local preview extension such as Live Server. Alternatively, from a terminal in the project folder, run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` and stop the server with `Ctrl+C` when finished.

## Work with Codex

Open this folder as the workspace and describe the changes you want. For example:

> In the RIDA website, revise the Evidence Review & Synthesis description without changing the layout. Validate the links and responsive styling afterwards.

The `AGENTS.md` file gives Codex the project-specific boundaries.

## Create a GitHub repository

1. Sign in to GitHub and create a new repository, such as `rida-website`.
2. Do not initialize it with a README, license or `.gitignore`; these are already included.
3. In a terminal opened in this folder, run:

```bash
git init
git add .
git commit -m "Initial RIDA website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/rida-website.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

## Publish with GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **GitHub Actions**.
4. Push a commit to `main`, or run the **Deploy GitHub Pages** workflow manually from the **Actions** tab.
5. Wait for GitHub to show the published URL.

The initial address will normally follow this pattern:

`https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

## Connect a custom domain

Once the site works at its GitHub address:

1. Add the domain under **Settings → Pages → Custom domain**.
2. Apply the DNS records requested by GitHub through the company where the domain is registered.
3. Wait for GitHub's DNS check to succeed.
4. Enable **Enforce HTTPS**.

GitHub may create a `CNAME` file in the repository. Keep that file once a custom domain is connected.

## Before public launch

- Replace the email address if a dedicated RIDA address becomes available.
- Confirm the final professional and conflict-of-interest wording.
- Decide whether to add a short legal notice and privacy statement.
- Test every link on desktop and mobile.
- Consider replacing the externally loaded Google fonts with locally hosted or system fonts if avoiding third-party font requests is important.
- Avoid adding analytics, cookies or a contact form until there is a clear need and an appropriate privacy setup.

## Updating the live site

After editing and reviewing locally:

```bash
git add .
git commit -m "Describe the website update"
git push
```

The GitHub Actions workflow will publish the updated version automatically.
