# jukenzie.com

The Jukenzie website, served by GitHub Pages from `main` at the repo root.
Plain HTML and CSS, no build step.

| Path | What |
|---|---|
| `index.html` | Home: who Jukenzie is, and links to the public projects |
| `soapcap/` | Soapcap's download page (its own styles; the Download button follows GitHub's latest release, so a release needs no edit here) |
| `matchsticks/` | Matchsticks' page, which is its App Store support URL |
| `matchsticks/privacy/` | Matchsticks' privacy policy, its App Store privacy URL |
| `style.css` | Styles for the home and Matchsticks pages |
| `CNAME` | The custom domain, `jukenzie.com` |

DNS is at Porkbun: four A records for `jukenzie.com` (185.199.108–111.153)
and a `www` CNAME to `pglockner.github.io`. They point at GitHub Pages, not at
this repo; the `CNAME` file and the repo's Pages settings claim the domain.

Preview locally with any static server from the repo root, for example
`python3 -m http.server`, then open http://localhost:8000.
