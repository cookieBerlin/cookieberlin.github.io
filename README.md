# cookieberlin.github.io

Start page for [cookieberlin.github.io](https://cookieberlin.github.io/), linking to the project sites:

- [Engelsystem Client](https://cookieberlin.github.io/EngelsystemClient/) ([repo](https://github.com/cookieBerlin/EngelsystemClient))
- [kv4p HT (by DB3AC)](https://cookieberlin.github.io/kv4p-ht/) ([repo](https://github.com/cookieBerlin/kv4p-ht))

Plain HTML and CSS, no build step. GitHub Pages serves the `main` branch as is (`.nojekyll`).

## Files

| File | Purpose |
|---|---|
| `index.html` | Start page with the project list, SEO meta tags, structured data and the Search Console verification tag |
| `style.css` | Shared stylesheet for all pages (light and dark colours as CSS variables) |
| `404.html` | Error page for the whole host (also used by project sites without their own 404) |
| `robots.txt` | Applies to the whole host; points to the sitemaps |
| `sitemap.xml` | Start page and the kv4p-ht pages (kv4p-ht has no sitemap of its own) |

## Adding a project

1. Add a card to the project list in `index.html` and an entry to the `ItemList` in its JSON-LD.
2. If the project has its own `sitemap.xml`, add it to `robots.txt`; otherwise list its pages in `sitemap.xml`.
3. Do not create folders named like a project repo here; they would collide with the project site.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000/>.
