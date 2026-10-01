<p align="center">
  <img src="logo.svg" alt="Monoid Studio" width="96" height="96">
</p>

<h1 align="center">Monoid Studio</h1>

<p align="center">
  Source of <a href="https://monoid.studio">monoid.studio</a>, the website of Monoid Studio, an independent software studio in Kawasaki, Japan.
</p>

## Overview

A static site served by GitHub Pages from the `main` branch root. It uses plain HTML and CSS, with no build step or dependencies.

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | Landing page (services, about, contact) |
| `privacy.html` | Privacy policy for apps and services |
| `style.css` | Shared stylesheet |
| `logo.svg` / `logo.png` | Logo mark (favicon, Open Graph image) |
| `logo-square.svg` / `logo-square.png` | Square logo with background, for avatars |
| `apple-touch-icon.png` | 180×180 icon for iOS home screens |
| `CNAME` | Custom domain (`monoid.studio`) |

## Local development

Serve the repository root with any static file server:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deployment

Pushing to `main` publishes the site to GitHub Pages automatically.

## Contact

- Email: [contact@monoid.studio](mailto:contact@monoid.studio)
- GitHub: [@monoid-studio](https://github.com/monoid-studio)
