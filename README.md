# envol

Source for [jason.envol.at](https://jason.envol.at), Jason's personal homepage.

## Layout

- `public/`: the site, served as-is (plain HTML, no build step).

## Deploy

Cloudflare Pages project `envol`, connected to this repo. Every push to `main` goes live in about 30 s. Build command: none. Output directory: `public`.

- `jason.envol.at` is the Pages custom domain.
- `envol.at` and `www.envol.at` are proxied records carrying a Cloudflare Redirect Rule (302 to `https://jason.envol.at`).
- Mail for envol.at (Cloudflare Email Routing inbound, Purelymail outbound) is independent of the site.

## Local preview

    python3 -m http.server -d public 8000

## Adding a site generator later

Set the build command and output directory in the Pages project settings (Settings → Build). Nothing else changes.
