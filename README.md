# Spades UX-Shield Filters

Community-maintained filter lists for [Spades UX-Shield](https://github.com/vinayak509143/spades-ux-shield).

Install the extension from the [Chrome Web Store](https://chromewebstore.google.com/detail/spades-ux-shield/dmchnhnkofleiokmffmkigfnoeodpemf) or [Firefox Add-ons](https://addons.mozilla.org/en-GB/firefox/addon/spades-ux-shield/) (version 1.0.8).

## Lists

| File | Description |
|------|-------------|
| [`lists/darklist.txt`](lists/darklist.txt) | **Spades Darklist** — cosmetic + procedural rules |

## Raw URLs

- jsDelivr: `https://cdn.jsdelivr.net/gh/vinayak509143/spades-ux-shield-filters@main/lists/darklist.txt`
- GitHub raw: `https://raw.githubusercontent.com/vinayak509143/spades-ux-shield-filters/main/lists/darklist.txt`

## How to Contribute

See **[CONTRIBUTING.md](CONTRIBUTING.md)** for the full checklist.

| Action | Link |
|--------|------|
| Request a new hide rule | [rule-request issue](https://github.com/vinayak509143/spades-ux-shield-filters/issues/new?template=rule-request.yml) |
| Report a dark pattern or a broken page | [report issue](https://github.com/vinayak509143/spades-ux-shield-filters/issues/new?template=breakage.yml) or **Report Dark Pattern & Broken Page** in the extension popup |
| Propose a rule yourself | PR to `lists/darklist.txt` (CI validates syntax + version bump) |

Do not submit rules targeting checkouts, payment gateways, or authentication screens. These will be immediately rejected to prevent accidental transaction breakage.

Out of scope for this list: drip pricing, hard-to-cancel account mazes, and trick wording that cannot be solved with CSS. In scope: cookie walls, newsletter overlays, sticky media, and isolated ATF promo tiles (e.g. Amazon homepage GWM).

## Licenses & Attribution

Original community rules in `lists/darklist.txt` are licensed under [GPL-3.0-or-later](LICENSE). By contributing, you license your rules under the same terms. Imported Fanboy/EasyList and AdGuard Annoyances cosmetics remain under their upstream GPL-3.0 / CC BY-SA 3.0 terms. See [ATTRIBUTION.md](ATTRIBUTION.md).

Engine privacy policy: [PRIVACY.md](https://github.com/vinayak509143/spades-ux-shield/blob/main/PRIVACY.md). Support: [Ko-fi](https://ko-fi.com/spadesxx).
