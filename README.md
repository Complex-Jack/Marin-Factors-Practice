# Marin Factors Practice (Shigley's)

A standalone student-practice activity for calculating the modified endurance limit
using Table A-20 materials and the Marin-factor equations from the 11th edition of
*Shigley's Mechanical Engineering Design*.

The activity generates random read-only scenarios in either SI or Standard units,
gives students three attempts to enter material properties and Marin-factor results
in the assigned unit system, and provides closeness-based feedback before revealing
the full solution.

The calculator is a single static webpage with no external dependencies, tracking,
or server-side processing.

## Deploy With GitHub Pages

1. Create a new **public** GitHub repository named `marin-factors-shigleys`.
   Do not initialize it with a README, license, or `.gitignore`.
2. From this folder, connect and push the prepared local repository:

```bash
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/marin-factors-shigleys.git
git push -u origin main
```

3. On GitHub, open **Settings > Pages**.
4. Under **Build and deployment**, select:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Click **Save**.

GitHub will publish the calculator at:

```text
https://YOUR-GITHUB-USERNAME.github.io/marin-factors-shigleys/
```

GitHub Pages deployment may take several minutes after the first push.

Alternatively, add this existing local repository in GitHub Desktop, choose
**Publish repository**, keep the name `marin-factors-shigleys`, and then enable
Pages using the settings above.

## Embed In Canvas

First confirm the published GitHub Pages URL opens normally. Then edit a Canvas
Page, switch to the HTML editor, and insert:

```html
<iframe
  src="https://YOUR-GITHUB-USERNAME.github.io/marin-factors-shigleys/"
  title="Marin Factors Practice (Shigley's)"
  width="100%"
  height="1800"
  style="border: 0;"
  loading="lazy"
  allowfullscreen>
</iframe>
```

Replace `YOUR-GITHUB-USERNAME` with the GitHub account or organization name that
owns the repository. If your Canvas institution removes iframe elements, provide
the GitHub Pages URL as an external link or ask the Canvas administrator to allow
the site.

## Local Preview

From this repository folder:

```bash
python3 -m http.server 8765
```

Then open:

```text
http://127.0.0.1:8765/
```

## Updating

Edit `index.html`, commit the change, and push to `main`. GitHub Pages will
republish the site automatically.
