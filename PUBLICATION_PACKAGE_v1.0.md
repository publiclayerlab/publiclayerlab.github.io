# Public Layer Lab Website Publication Package v1.0

Status: clean source package for first publication
Date: 2026-06-03

## Purpose

This package consolidates the first-publication website state after:

1. Notes First Publication Patch v0.3;
2. Notes Publication Switch v0.1;
3. Appearance Patch v0.1;
4. Menu Publication State Patch v0.1;
5. Publication Control Review v0.1A.

It is intended to serve as the working source package for local review, build, and deployment.

## Public content included

The following pages are public in ordinary Hugo builds:

- Home
- About
- Work
- Notes
- Contact
- Privacy
- Accessibility
- Stichting
- Methods
- Legitimacy by Design
- Lab
- Contestability route sketch
- Five Public Layer Foundations notes:
  - Digital public infrastructure
  - Public authority
  - Why transparency is not the same as accountability
  - What makes a system contestable?
  - Repair is part of public system design

## Draft content retained

The package keeps unpublished material in the source tree as draft-only content:

- later/unpublished root notes;
- duplicated `content/en/` material;
- duplicated `content/nl/` material.

This avoids accidental duplicate publication before multilingual routing is intentionally configured.

## Design state

The package includes the restrained appearance baseline:

- homepage concept panel;
- inline SVG route sketch;
- light card and menu refinements;
- focus-visible styles;
- reduced-motion safety rule;
- darker muted text.

No second graphic, new visual identity system, logo redesign, animation layer, or broader visual redesign is included.

## Menu state

The upper menu is configured with public page targets and explicit URL fallbacks. This prevents unresolved menu links when draft-only pages are excluded from ordinary builds.

## Not changed

This package does not reopen or change:

- core positioning;
- note body text;
- source-lineage research;
- licensing/footer policy;
- contact/Gmail decisions;
- broader website architecture;
- legal/statutory identity;
- visual identity or logo.

## Local review commands

Ordinary public review:

```bash
hugo server
```

Internal draft review only:

```bash
hugo server --buildDrafts
```

Clean production build:

```bash
hugo --cleanDestinationDir
```

## Control note

This package does not include generated `public/` output. Regenerate `public/` locally from this source package before deployment.
