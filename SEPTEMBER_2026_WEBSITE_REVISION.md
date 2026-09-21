# September 2026 website revision

**Implemented:** 19–20 September 2026  
**Status:** source implementation complete; ready for Hugo build/CI and deployment QA.

## Implemented

- Home: new research-lab framing; Work/Notes/About become primary destinations; Methods/Lab demoted to developing materials; selected Notes retained.
- Work: replaced field catalogue and sitemap narration with relevance, reconstruction, examples, outputs, and current-phase/contact logic.
- About: aligned with small independent public-interest research-lab framing and removed duplicate institutional-identity sentence.
- Methods: removed Work/Methods/Lab sitemap narration and “methodological centre” language.
- Legitimacy by Design: two terminology/status patches only.
- Lab: removed speculative future-output catalogue; retained one concrete sketch.
- Contact: clarified source/correction/research/practitioner routes without creating a service funnel.
- Notes index: removed gateway-systems/sequence housekeeping; existing five published Notes remain unchanged.
- Privacy: replaced the June notice with the September 2026 notice covering website hosting, correspondence, research/source exchanges, retention, current AI-assisted tools, third-party services, international processing, and data-subject rights.
- Site metadata: broadened from “digital public systems” to “digital and administrative arrangements.”
- The public Work page no longer uses the `work-gateway` shortcode. The shortcode is retained only because the historical draft `content/en/` Work page still references it; it is not rendered in the ordinary public build.

## Privacy operating baseline

The public notice now reflects the current baseline:

- ordinary Gmail account for correspondence;
- GitHub Pages hosting;
- ChatGPT / OpenAI and Claude / Anthropic used on a limited basis for drafting, review, summarising, and analysis;
- ordinary correspondence retention: normally 12 months after closure;
- substantive research/correction/source exchanges: up to three years after the last substantive exchange where retention remains justified;
- no analytics, advertising, newsletter tracking, contact forms, comments, automated profiling, or automated decision-making;
- private correspondence is not normally published verbatim or attributed by name without discussing attribution;
- identifying information should be minimised before use of consumer AI tools where it is not necessary to the task.

The internal Privacy Operating Record is deliberately **not stored in this public Git repository**. It belongs in PLL’s internal operating pack.

External specialist privacy review is not a precondition for ordinary website/email operation. It becomes a case-level trigger before materially identifiable/high-risk processing, including substantial use of private correspondence in a named case, publication of identifiable non-public material, special-category data, systematic profiling/monitoring, or another activity likely to create high privacy risk.

## Intentionally unchanged

- Accessibility page.
- Stichting page.
- Five published Notes.
- Contestability route sketch.
- Main navigation: Home / About / Work / Notes / Contact.
- Visual identity and overall CSS system, except a small responsive rule supporting the new three-card Home hierarchy.
- Draft-only duplicated `content/en/` and `content/nl/` material.
- Public Gmail address, pending later domain-mail implementation.

## Remaining deployment steps

Privacy is no longer a deployment blocker. Before production deployment:

1. run an actual Hugo Extended build (locally or through GitHub Actions);
2. inspect the rendered site, especially Home, Work, About, Methods, Lab, Notes, Contact, Privacy, Accessibility, and Stichting;
3. verify internal/external links and mobile layout;
4. review `git diff` / `git status`;
5. commit the September revision;
6. push to `main` and confirm the GitHub Pages workflow succeeds;
7. perform live-site QA after deployment.

## Validation performed in this package

Repository-level validation was run before packaging:

- `hugo.yaml` parsed successfully and the main navigation remains Home / About / Work / Notes / Contact;
- YAML front matter parsed across the content tree;
- required public page targets and modified-page internal links resolved against the source tree;
- exactly five root Notes remain public;
- those five published Notes are unchanged from the pre-September canonical source;
- the Contestability route sketch is unchanged;
- changed Go-template files passed a basic block-balance check;
- CSS parsed without syntax errors;
- `git diff --check` passed.

A compiled Hugo build was **not** run in the packaging environment because no Hugo executable was available. The repository’s GitHub Actions workflow builds with Hugo Extended 0.161.1 on push to `main` using `hugo build --gc --minify`.
