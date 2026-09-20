# Contributing to Spades Darklist

Rules live in **`lists/darklist.txt`**. The [Spades UX-Shield](https://github.com/vinayak509143/spades-ux-shield) extension syncs this file from jsDelivr (~twice daily). Engine/parser changes belong in the **engine** repo, not here.

## Ways to contribute

| Path | When |
|------|------|
| **[Request a rule](https://github.com/vinayak509143/spades-ux-shield-filters/issues/new?template=rule-request.yml)** | You want something hidden but don’t want to write filter syntax. |
| **[Report breakage](https://github.com/vinayak509143/spades-ux-shield-filters/issues/new?template=breakage.yml)** | The extension broke checkout, login, payment, or something legitimate. |
| **Pull request** | You can add a tested `host##selector` line yourself. |

Extension popup **Report broken page** opens the breakage template with site/path/version prefilled.

## Pull request checklist

1. **Edit only** `lists/darklist.txt` (unless you are updating docs).
2. **Bump** `! Version:` — 12 digits `YYYYMMDDHHMM`, must be **greater** than the previous version on `main`.
3. **One hostname scope per line** — `example.com,www.example.com##.selector` (no global `##` without a host).
4. **Prove a hit** — one URL where the element should disappear with the extension on.
5. **Prove must-not** — at least one URL where the same selector family must **not** clip checkout, login, pay, or core content (see [holdout](https://github.com/vinayak509143/spades-ux-shield/blob/main/docs/HOLDOUT_PROTOCOL.md)).
6. **PR description** — paste hit + must-not URLs; attach before/after screenshots (top document; consent iframe if relevant). No passwords or full DOM dumps.
7. CI must pass — `validate-darklist` runs on every PR touching `lists/darklist.txt`.

## Never submit

- Rules on checkout, cart, payment gateways, login, 2FA, or account-cancellation flows.
- Generic selectors (`[class*="modal"]`, `.banner`, `div[role="dialog"]`) — they false-positive across entire sites.
- Drip pricing, subscription mazes, or copy-only dark patterns CSS cannot fix.

Full engine policy: [CONTRIBUTING.md](https://github.com/vinayak509143/spades-ux-shield/blob/main/CONTRIBUTING.md).

## Filter syntax (short)

```
hostname##.css-selector
hostname##.parent:has-text(/urgency phrase/i)
hostname/path/*##input[name="marketing"]:uncheck
```

Procedural extras match the engine: `:has-text`, `:upward`, `:uncheck`, `:click-dismiss`, etc. Invalid lines are dropped at compile time — CI catches parse errors.

## Shopify app widgets

If the widget uses a stable class prefix (`hurrify-`, `hextom-`, …), request a **vendor prefix** in the [engine repo](https://github.com/vinayak509143/spades-ux-shield) (`cosmetic-vendors.css`), not a one-off hostname line on every store.

Theme-native markup without a prefix (e.g. generic `.product-count`) → hostname rules in **darklist** only when selectors are scoped and reviewed.

## Amazon retail

- **`amazon-retail##`** — PDP/social-proof IDs for all 23 retail marketplaces (engine sets `data-op-amz` on apex/`www` only).
- **`amazon-en##`** — English `:has-text` deal badges (subset of locales).
- **`amazon.in,www.amazon.in##`** — India-only homepage ATF (GWM, cashback, etc.).
- **Banned:** `amazon.com##` or any rule that would match `aws.amazon.com` via hostname suffixes.

## Licenses

Original lines in `darklist.txt` are licensed with this repository. Do not paste full EasyList/AdGuard blobs here.
