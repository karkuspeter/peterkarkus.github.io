# karkuspeter.github.io

Personal research page of Peter Karkus. Plain static HTML — no build step.

## Deploy (one-time)

1. Create a new **public** repo named exactly `karkuspeter.github.io` at https://github.com/new
   (no README/license, so the first push is clean).
2. Add the profile photo: download
   https://static.tildacdn.info/tild6431-3963-4338-b164-376230316362/IMG_8808_Online.JPG
   and save it in this folder as `profile.jpg` (lowercase). A ~800×800 px JPG under 300 KB is ideal.
   Until you do, the page falls back to the Tilda-hosted copy.
3. Push:
   ```bash
   cd karkuspeter.github.io
   git init -b main
   git add .
   git commit -m "Personal website"
   git remote add origin git@github.com:karkuspeter/karkuspeter.github.io.git
   git push -u origin main
   ```
4. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   Branch: `main`, folder `/ (root)` → Save. (Usually already set automatically for `<user>.github.io` repos.)
5. Wait 1–2 minutes, then open https://karkuspeter.github.io/

## Editing

- All content and styling is in `index.html`.
- To add a paper, copy one `<li class="paper">…</li>` block.
- Link color, text color, and page width are CSS variables at the top of the `<style>` block.

## Optional

- Custom domain: add a `CNAME` file containing the domain and configure DNS per
  https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site
- Redirect the old Tilda site to the new URL, or unpublish it, to avoid duplicate pages.
