# Certificate badge images

This folder contains placeholder SVGs for your certificates. To replace them with the official issuer badges, follow one of the methods below.

## Option A — Download badge assets from issuer pages (recommended)
1. Open each verification URL in your browser:
   - Databricks: https://credentials.databricks.com/5dc40b77-9345-4587-8dde-7ab8e62b013e#acc.7VZo6Kw2
   - Skilljar: https://verify.skilljar.com/c/cbrd2fbmreay
   - Microsoft: the two Microsoft Learn share links in the README
2. Right-click the badge image and choose "Save image as..." or copy the image URL.
3. Save the file into this folder with the exact filename:
   - databricks-credential.svg (or .png)
   - skilljar-credential.svg (or .png)
   - microsoft-credential-1.svg (or .png)
   - microsoft-credential-2.svg (or .png)

## Option B — Download via curl (if URL available)
If you have the direct image URLs you can run:

````bash
mkdir -p images/certs
curl -L "<IMAGE_URL_FOR_DATABRICKS>" -o images/certs/databricks-credential.svg
curl -L "<IMAGE_URL_FOR_SKILLJAR>" -o images/certs/skilljar-credential.svg
curl -L "<IMAGE_URL_FOR_MS1>" -o images/certs/microsoft-credential-1.svg
curl -L "<IMAGE_URL_FOR_MS2>" -o images/certs/microsoft-credential-2.svg
````

Replace the <IMAGE_URL_...> placeholders with the actual image addresses you copied from the verification pages.

## Commit and push changes
Once you've replaced the placeholder files, run:

````bash
git add images/certs/* README.md
git commit -m "Add official certificate badge images"
git push origin main
````

Notes:
- Prefer SVG when available for best scaling. If issuer provides PNG only, PNG is fine.
- Keep the filenames exactly as above so README links work without changes.
