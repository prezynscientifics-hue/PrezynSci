# Prezyn Scientifics website

Static website (one file: `index.html`). Free to host, HTTPS included.

## Publish on GitHub Pages (free)
1. Sign up at github.com and click **New repository**. Name it `prezyn-website`, set it to **Public**, and click **Create repository**.
2. Click **uploading an existing file**, drag in everything from this folder (`index.html`, `.nojekyll`, `robots.txt`, `_headers`, `README.md`), then **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, Folder to **/ (root)**, and click **Save**.
4. After 1–2 minutes your site is live at `https://YOUR-USERNAME.github.io/prezyn-website/`.
5. Turn on **Enforce HTTPS** on the same Settings → Pages screen.

Account security: enable two-factor authentication on GitHub, since anyone who gets into your account can change the site.

## Custom domain (optional, about ₹800/year)
Buy a domain, then in **Settings → Pages → Custom domain** enter it (for example `www.prezynscientifics.com`) and follow the DNS instructions shown there.

## Updating products and brands on the live site
The admin panel (`your-site-address/#admin`) saves only in your own browser, so visitors do not see its changes. To change the public catalogue:
1. Use the admin panel to try changes, then click **Export JSON**.
2. In GitHub, open `index.html` and click the pencil icon (Edit).
3. Find `const D={products:[` near the bottom and edit the `products` and `brands` lists there. Each product looks like `{n:"Name",c:"Category",b:"Brand",d:"Description"}` and brands are plain text in quotes, for example `brands:["Brand A","Brand B"]`.
4. Click **Commit changes**. The site updates in about a minute.

## Optional: Cloudflare Pages
`_headers` adds extra security headers on Cloudflare Pages or Netlify (GitHub Pages ignores it). In Cloudflare, choose **Workers & Pages → Create → Pages → Connect to Git**, select this repository, leave the build command empty, and deploy.

## Next step
For a real admin login with a database, add Supabase (free tier). Ask Claude to build it.
