# blaze-redirect 🔥

Free permanent subdomain + auto HTTPS + instant redirect — zero cost, no browser warning.

Deploy this repo to **Netlify** or **Cloudflare Pages** (both free) and it will redirect every visitor to your target URL with a `301`.

## 1. Set your target URL

Edit `_redirects` and replace `YOUR-TARGET-URL.com`:

```txt
/*  https://YOUR-TARGET-URL.com/:splat  301!
```

Also update `index.html` (fallback) with the same URL.

## 2. Deploy

**Option A — Netlify (easiest)**
1. Go to https://app.netlify.com/drop and drag this folder, OR
2. Netlify → "Import from Git" → pick this repo. Publish directory: `.` (root), no build command.

You get `https://<name>.netlify.app` — free, valid HTTPS, no warning.

**Option B — Cloudflare Pages**
1. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git → pick this repo.
2. Build command: *(empty)*, Output directory: `/`.
3. You get `https://<project>.pages.dev` — free, valid HTTPS.

## Notes
- `/*` matches everything, `:splat` carries the path, `301!` forces permanent redirect.
- Works with any hostname — point `CNAME yourname.is-a.dev -> <project>.pages.dev` for a custom free subdomain.
