# anchorkey-site

Source for [anchorkey.io](https://anchorkey.io). Plain static HTML, no build step.

| Path | Content |
|---|---|
| `index.html` | Landing page — drawn from `ONE-PAGER.md` in the [AnchorKey app repo](https://github.com/indiagrams/AnchorKey) |
| `privacy.html` | Privacy policy. Linked from the App Store listing. |
| `styles.css` | Single stylesheet, dark-mode aware. |

## Deploy

Auto-deploys via Cloudflare Pages connected to this repo's `main` branch.

Manual deploy from CLI:
```sh
npx wrangler pages deploy . --project-name anchorkey
```

## Edit

The privacy policy is the only file with constraints — substantive
changes need to bump the "Last updated" date and ship release notes
acknowledgement in the AnchorKey app's next App Store release.

The landing page tracks `ONE-PAGER.md` from the app repo. When the
one-pager moves, this should follow within the same week.
