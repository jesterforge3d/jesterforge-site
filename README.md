# JesterForge one-page site — source of record

Built 2026-11-09 by Lane PA (record: Roadie `council/surge-20261109/lane-pa.md`).

- `index.html` — the whole site. Single static file, inline CSS, zero JS, zero build chain.
- `assets/` — real workshop photos only (web-sized derivatives; originals in the fleet photo library).
- `_build/` — preview screenshots + `jesterforge-site.zip` (drag-and-drop deploy package).
- Mirror: Bastion `~/fleet-archive/jesterforge-site/` (index.html + assets, byte-identical size 441,358 B).

## Status

Site is BUILT and verified locally (desktop + mobile renders, all links checked — see lane record).
Deploy state (2026-11-09, Lane PC): the deploy payload is corrected and final — `_build/
jesterforge-site.zip` rebuilt from the current source WITH the verified Gumroad link
(payload index.html md5 = source md5, readback-verified). The public deploy itself runs
through a new free-host account (Cloudflare Pages preferred) created on Shawn's go —
see Roadie `council/surge-20261109/lane-pc.md` for the staging URL once live.

## To deploy (any free static host)

Upload `index.html` + `assets/` (or drop `_build/jesterforge-site.zip` into Netlify Drop /
Cloudflare Pages direct upload). No build command, publish dir = root.

## Domain hookup (after Shawn registers jesterforge.com at Porkbun)

Full step-by-step with exact DNS records is in the lane record, §Domain hookup.
Short version (Cloudflare Pages path): add the `jesterforge.com` zone in Cloudflare → at Porkbun
replace the domain's nameservers with the two Cloudflare nameservers → in the Pages project add
custom domains `jesterforge.com` + `www.jesterforge.com` (DNS + SSL auto-configure). The
ALIAS `@` → `<project>.pages.dev` variant (DNS stays at Porkbun) is the fallback only.
Reconciled 2026-11-09 by Lane PC — lane-pc.md §Domain governs where this short version differs.

## Known content swaps pending

- Hero/cards: swap in tonight's Rock Sliders (Kobra) + Stock Skid (FlashForge) finished-print
  photos when the print lanes publish their media packages — photos are card slots in
  `index.html`, one-line `src` changes.
- Shop cards currently link to the Cults3D storefront (per-design URLs were not verifiable —
  Cults returns 403 to automated fetches). Swap in per-design URLs from the signed-in
  watchdog/listing records when available.
- Stock slots: all 8 agencies render linkless ("Portfolio opening") until Lane OX's created
  accounts produce real contributor portfolio URLs. Never invent a URL.
- Gumroad: SETTLED 2026-11-09 (Lane PB verdict (a), Lane PC firsthand re-fetch): the store
  is LIVE at `https://jesterforge.gumroad.com` (HTTP 200, nothing stocked yet). The 404 was
  the wrong subdomain (`jesterforge3d.gumroad.com` does not exist). The link ships in
  `index.html` (Shop section + footer, 2 anchors).
