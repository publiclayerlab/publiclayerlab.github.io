# Public Layer Lab Hugo site

Publication source package v1.0 for the Public Layer Lab website.

This package is intended as the clean working source for first publication. It contains the public root site pages, the first five Notes, the appearance patch, and the upper-menu publication-state fix. It does not include generated `public/` output.

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

## Clean production build

```bash
hugo --cleanDestinationDir
```

Hugo will generate the deployable static output into the `public/` directory unless another destination is configured.

## Publication state

Public in ordinary builds:

- `/`
- `/about/`
- `/work/`
- `/notes/`
- `/notes/digital-public-infrastructure/`
- `/notes/public-authority/`
- `/notes/why-transparency-is-not-the-same-as-accountability/`
- `/notes/what-makes-a-system-contestable/`
- `/notes/repair-is-part-of-public-system-design/`
- `/methods/`
- `/methods/legitimacy-by-design/`
- `/lab/`
- `/lab/contestability-route-sketch/`
- `/stichting/`
- `/privacy/`
- `/accessibility/`
- `/contact/`

Draft-only for now:

- unpublished root notes;
- duplicated `content/en/` tree;
- duplicated `content/nl/` tree.

## Notes

- Do not paste changes into `public/`; edit source files and regenerate output with Hugo.
- The upper menu uses `pageRef` with explicit URL fallbacks.
- The homepage includes one restrained inline SVG concept sketch.
- This package does not make any new licensing, contact, Gmail, branding, or broader architecture changes.
