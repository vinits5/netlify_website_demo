# vinitsarode.com

Personal site. Single static page, no build step.

## Structure

    index.html      whole site — inline CSS, inline three.js hero
    netlify.toml    publish dir, security headers, cache policy
    favicon.svg     concentric-ring mark (flange in section)
    robots.txt

## Local preview

    python3 -m http.server 8000

Then open http://localhost:8000

`index.html` also opens directly by double-clicking. The hero uses the
classic (non-module) three.js build specifically so it works over `file://`.

## Deploying

Netlify builds from `main`. Push to `main` and it goes live in ~30 seconds.
Push to any other branch to get a deploy preview URL instead.

## External dependencies

- three.js r128 — cdnjs
- Newsreader, Instrument Sans, IBM Plex Mono — Google Fonts

Both load from CDN. To go fully self-hosted, vendor them into `/assets`
and update the two `<link>`/`<script>` tags in the head.
