# LumenForge

LumenForge 3D Lampshade Studio: design parametric, 3D-printable lampshades in the browser and export watertight STL files.

## Structure

| File | Route | Purpose |
| --- | --- | --- |
| `index.html` | `/` | Landing page |
| `studio.html` | `/studio` | The 3D lampshade studio (Three.js) |
| `vercel.json` | | Clean URLs, redirect from the old studio filename, security headers |

It's a static site with no build step. Every dependency loads from a CDN.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

`/studio` only resolves on Vercel (clean URLs). Locally, open `/studio.html` instead.

## Deploy to Vercel

1. Import the repo at <https://vercel.com/new>.
2. Framework preset: **Other**. Leave the build command and output directory empty.
3. Deploy.

Or from the CLI: `npx vercel` (preview), then `npx vercel --prod`.
