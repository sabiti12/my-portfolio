# Abraham Isyagi — Portfolio

Personal portfolio site. Single self-contained HTML page, no build step, no
dependencies, no external network requests.

**Live:** _add your URL here once deployed_

---

## Structure

```
index.html            the whole site — markup, styles and script inline
assets/img/           optimised, EXIF-stripped imagery
_headers              security headers for Netlify / Cloudflare Pages
robots.txt
.nojekyll             stops GitHub Pages running Jekyll over the files
```

## Deploying

**GitHub Pages** — Settings → Pages → Deploy from branch → `main` / root.
Note that Pages cannot serve the `_headers` file; set the equivalent headers via
Cloudflare in front of it, or deploy to Netlify / Cloudflare Pages instead where
`_headers` is honoured.

**Netlify / Cloudflare Pages** — connect the repo, no build command, publish
directory `/`. `_headers` is applied automatically.

## Security and privacy decisions

These are deliberate. Please keep them when editing.

| Decision | Why |
|---|---|
| Email address never appears in the HTML source | It is split across two base64 attributes and assembled in-browser only on click. Defeats automated harvesting. **A forwarding alias is still the stronger control.** |
| No phone number | Not needed on a public page. |
| EXIF stripped from every image | The source portrait carried camera model, software and capture timestamp. |
| No third-party scripts, fonts, CDNs or analytics | Zero outbound requests on page load; nothing to compromise, nothing tracking visitors. |
| Content-Security-Policy `default-src 'none'` | Nothing loads that is not explicitly allowed. |
| `rel="noopener noreferrer"` on all external links | Prevents reverse-tabnabbing and referrer leakage. |
| `robots: noarchive` | Keeps stale copies out of search-engine caches. |

## Content accuracy

Copy comes from a maintained content pack and observes fixed claim framings —
AXAM is co-founded (three-person team); Compliance Architect Gem automates
*documentation* and states time saving as design intent, not a measured result;
Bwi-Know is live with game-by-game granularity in progress; the UCU Athletics
Platform is in development; the ISACA placement is a team result; certifications
are described exactly as issued. The full list is in a comment at the top of
`index.html`. Do not upgrade a claim beyond what is written there.

## Still to do

- Two projects (UCU Athletics Platform, Mobile Consultation Application) have no imagery yet
- The Writing section holds three placeholder cards awaiting real Medium posts

---

© Abraham Isyagi. Content and imagery all rights reserved; you are welcome to
read the source for technique.
