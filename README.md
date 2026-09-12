# TapSafe demo tap pages

Static pages for the TapSafe school ID card. Each card's NFC chip and printed QR point to `/c/{code}`, an 8-character random code that carries no school or student information.

## Files

```
index.html          demo landing page linking the sample cards
404.html            "card not yet activated" page, served for any unknown code
_redirects          Netlify rule: /c/* falls through to 404.html
assets/style.css    shared styles
c/2SOXhptD/         Aarav S.
c/cTAoxjfw/         Meera K.
c/twxIeSlL/         Zoya A.
```

No build step. Deploy the folder as-is.

- **Cloudflare Pages**: upload or connect the repo, output directory `/`. Cloudflare serves `404.html` for unknown paths automatically.
- **Netlify**: drag the folder onto the dashboard. `_redirects` routes unknown `/c/*` codes to the not-activated page.

To add a card, copy one of the `c/{code}/` folders, rename it to a new random code and edit the details in `index.html`.

Card pages carry `noindex` so search engines never list them.
