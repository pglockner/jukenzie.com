# jukenzie.com

The Jukenzie website, served by GitHub Pages from `main` at the repo root.
Plain HTML and CSS, no build step.

| Path | What |
|---|---|
| `index.html` | Home: who Jukenzie is, and links to the public projects |
| `soapcap/` | Soapcap's download page (its own styles; the Download button follows GitHub's latest release, so a release needs no edit here) |
| `matchsticks/` | Matchsticks' page, which is its App Store support URL |
| `matchsticks/privacy/` | Matchsticks' privacy policy, its App Store privacy URL |
| `radio-globe/` | Sweep Radio's page for testers; its Download button follows the latest release in `pglockner/radio-globe-releases`, so a build needs no edit here, and the line under it shows that release's version and date, read from GitHub in the visitor's browser (hidden if that fails) |
| `radio-globe/privacy/` | Sweep Radio's privacy policy, the privacy URL for TestFlight and both stores |
| `404.html` | The page Pages shows for a missing address (root-relative links, since it is served at any depth) |
| `jukenzie.jpg`, `icon.png` | The home page's picture, and the site icon cut from it |
| `style.css` | Styles for every page but Soapcap's |
| `CNAME` | The custom domain, `jukenzie.com` |
| `.nojekyll` | Tells Pages to serve the files as they are, without a Jekyll build |

DNS is at Porkbun: four A records for `jukenzie.com` (185.199.108–111.153)
and a `www` CNAME to `pglockner.github.io`. They point at GitHub Pages, not at
this repo; the `CNAME` file and the repo's Pages settings claim the domain.
Mail, such as support@jukenzie.com, goes through Porkbun's email forwarding:
MX records to `fwd1.porkbun.com` (10) and `fwd2.porkbun.com` (20), and an SPF
record, `v=spf1 include:_spf.porkbun.com ~all`. There is no DMARC record.

Preview locally with any static server from the repo root, for example
`python3 -m http.server`, then open http://localhost:8000 (that server
doesn't use `404.html`; open http://localhost:8000/404.html to see it).
