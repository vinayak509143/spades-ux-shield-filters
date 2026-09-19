# Attribution

Spades UX-Shield’s **original community lists** in this repository (`lists/darklist.txt` and rules authored here) are original work. Packaged third-party cosmetics are **not**.

## Upstream filter lists

The engine’s `npm run update-filters` (`scripts/fetch-third-party.mjs` in [spades-ux-shield](https://github.com/vinayak509143/spades-ux-shield)) downloads public filter lists and writes `third-party-rules.txt`. Any copy of that extract published here is an **extract**, not a relicense.

### Fanboy’s Annoyance List (EasyList)

- **Maintainer:** Ryan “Fanboy” and EasyList contributors  
- **Source:** [https://secure.fanboy.co.nz/fanboy-annoyance.txt](https://secure.fanboy.co.nz/fanboy-annoyance.txt)  
- **Project:** [https://easylist.to/](https://easylist.to/)  
- **License:** GNU GPL v3 **and** Creative Commons Attribution-ShareAlike 3.0 Unported ([CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/))  
- **GPL text:** [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

EasyList-family lists require **attribution** and **share-alike** when you redistribute derived filter text. Shipping imported Fanboy/EasyList cosmetics in this repo is that redistribution.

### AdGuard Annoyances

- **Maintainer:** AdGuard Software Ltd  
- **Source (Chromium filter 14):** [https://filters.adtidy.org/extension/chromium/filters/14.txt](https://filters.adtidy.org/extension/chromium/filters/14.txt)  
- **Repository:** [https://github.com/AdguardTeam/AdguardFilters](https://github.com/AdguardTeam/AdguardFilters)  
- **License:** [GNU GPL v3](https://github.com/AdguardTeam/AdguardFilters/blob/master/LICENSE)

## What we extract

Spades UX-Shield extracts and redistributes only hostname-scoped cosmetic element-hiding selectors (`##`) from these lists via `scripts/fetch-third-party.mjs`. Upstream network-filtering, scriptlets, and procedural rules remain the property of their respective maintainers under their original licenses.

Imported third-party rules (Fanboy/AdGuard) **retain** their original GPL-3 / CC BY-SA 3.0 licenses. We redistribute **only** the cosmetic `##` subset. Do not paste full EasyList/AdGuard blobs into this repository.

The extract also **drops** generic (`##` with no host), HTML filters (`##^`), snippets (`#$#`), scriptlets (`+js`), and checkout/payment/auth **critical-flow** cosmetics.

## This list repo (not the extract)

Original rules authored in `lists/darklist.txt` are intended to be licensed with this repository. **MIT (or any engine license) does not replace GPL/CC-BY-SA on imported third-party cosmetics.** Combined distributions that include the extract must honor upstream terms (attribution, share-alike / GPL as applicable).

Engine source: [spades-ux-shield](https://github.com/vinayak509143/spades-ux-shield) — see that repo’s `ATTRIBUTION.md` and `CONTRIBUTING.md`.
