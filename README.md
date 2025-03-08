# bb

## 1. Check Your GitHub Pages Settings
Go to your repository on GitHub.
Click on Settings → Pages.
Under the Source section, check which branch is selected.
Ensure the correct folder is selected:
If you want to serve README.md, set the source to the root (/).
If it's set to /docs, GitHub will serve the MkDocs site.

## 2. Disable MkDocs (If Not Needed)
If MkDocs is overriding your README.md:

Delete or rename the mkdocs.yml file (e.g., mkdocs_backup.yml).
Remove the docs/ folder if it contains MkDocs files and isn't needed.

## 3. Force Update GitHub Pages
Go to Settings → Pages.
Change the Source to None and save.
Re-enable GitHub Pages and select the branch with your README.md.

## 4. Clear Old MkDocs Deployments (If Any)
If MkDocs was previously deployed:

Delete the gh-pages branch:
git push origin --delete gh-pages
Re-publish GitHub Pages using the correct branch.

## 5. Manually Set README as the Homepage
If you want GitHub Pages to display your README.md, ensure there's no index.html or index.md inside your repository's root directory or docs/ folder. GitHub prioritizes these over README.md.
