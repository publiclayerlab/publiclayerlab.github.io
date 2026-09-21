# Public Layer Lab Hugo site

Canonical Hugo source for `publiclayerlab.eu`.

## Current working state

This working tree contains the **September 2026 website revision**, including the completed public Privacy baseline adopted on 20 September 2026.

Implemented in the public source:

- revised Home hierarchy and framing;
- rewritten Work page;
- revised About page;
- revised Methods page;
- narrow Legitimacy by Design terminology/status patch;
- trimmed Lab index;
- revised Contact page;
- simplified Notes index;
- revised Privacy notice;
- existing five published Notes retained unchanged;
- Contestability route sketch retained unchanged;
- Stichting and Accessibility retained unchanged.

The public Gmail address remains in place until a domain mailbox is configured and tested for receive/send, SPF, DKIM, DMARC, and delivery. This is not a deployment blocker for the September revision.

The internal Privacy Operating Record is **not stored in this public repository**. It belongs in the private PLL operating pack.

## Local review

Run from the project root:

```bash
hugo server
```

Review the public site in ordinary mode first. Do not use `--buildDrafts` for the public publication check.

For internal draft inspection only:

```bash
hugo server --buildDrafts
```

## Production-style build

The GitHub Actions workflow uses Hugo Extended 0.161.1 and runs:

```bash
hugo build --gc --minify
```

Do not edit or commit generated `public/` output. GitHub Pages deployment rebuilds it from source.

## Publication state

Public in ordinary builds:

- `/`
- `/about/`
- `/work/`
- `/notes/`
- five published foundational Notes;
- `/methods/`
- `/methods/legitimacy-by-design/`
- `/lab/`
- `/lab/contestability-route-sketch/`
- `/stichting/`
- `/privacy/` (September 2026 notice)
- `/accessibility/`
- `/contact/`

Draft-only material remains under the existing unpublished root Notes and duplicated `content/en/` / `content/nl/` source trees. That historical cleanup is deliberately outside the September website revision.

`PUBLICATION_PACKAGE_v1.0.md` is retained as the historical June 2026 publication record.
