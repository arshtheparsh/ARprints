# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

This site is a **dedicated storefront for the 3D-print/CAD commission business**, linked out from a separate, broader "main portfolio" (everything Arshdeep does, not just this business — out of scope for this project). Primary audience here is narrower than a general portfolio:

1. **Potential customers** (the primary audience) considering a custom 3D-printed or CAD-designed part, deciding whether to trust Arshdeep enough to pay for custom work. Most arrive already somewhat warmed up via the main portfolio link.
2. **Evaluators** (college admissions, internship/scholarship reviewers) may still click through from the main portfolio, but this site does not need to carry that burden alone — the main portfolio is their primary stop.

## Product Purpose

A focused, conversion-oriented storefront for Arshdeep's 3D-printing/CAD commission work: show enough real, honestly-documented project evidence to build trust, then convert that trust into a custom-request submission. It is one linked destination within a larger personal portfolio, not the sole place Arshdeep's overall work is judged.

## Positioning

Custom 3D-printing/CAD commission work is not a novel category — many people already offer it (Etsy, Fiverr, etc.), and out-innovating that market is not the goal. Differentiation instead comes from: (1) documenting real process including what broke and was fixed, rather than polished-only results, and (2) being a known, trusted individual (school/local network, direct portfolio evidence) rather than an anonymous marketplace listing. Transparent, simple pricing supports this rather than trying to look impressive.

## Operating Context

This site is one linked destination inside a larger main portfolio (separate project, not yet built/scoped here) that covers everything Arshdeep does. Visitors mostly arrive here already having seen the main portfolio, so this site can stay narrowly focused on the print/CAD business rather than re-proving general credibility from scratch.

Solo high school student. Designs in Fusion 360, prints on a personal FDM printer, and takes physical measurements (caliper, protractor) as part of the design process. This is a side project alongside schoolwork — time and filament budget are limited, so volume/turnaround are inherently small-scale. The site itself is hand-edited static HTML/CSS/JS with Claude Code's help, no build tooling. Local development requires serving over HTTP (`python3 -m http.server`), not opening the file directly — `<model-viewer>`'s GLB loading fails under `file://`.

## Capabilities and Constraints

- Plain static HTML/CSS/JS, no framework or bundler.
- 3D models shown via `<model-viewer>` from `.glb` files exported out of Fusion 360.
- Custom-request form submits via Formspree (free tier: 250 submissions/month cap; first submission requires a one-time email confirmation before the form goes live).
- Pricing: 10¢/gram of filament for printing an existing design, $5 minimum order. Custom design-from-scratch work is quoted separately and has no fixed rate yet.
- Only one real project is documented so far (Headphone Stand). Two homepage project slots are still placeholder "Coming soon" cards — future work must not fabricate content for these.
- Not yet deployed publicly; currently local-dev only.

## Brand Commitments

Name: "Arshdeep" (site title: "Arshdeep — Hardware & CAD Design"). Voice, stated directly in the hero copy: "High school student designing and building hardware... I share the whole process, including what broke along the way." This is a binding tone commitment — first-person, transparent about failures, not corporate/polished-only.

## Evidence on Hand

One fully documented project: **Headphone Stand** (wall-mounted, extra hook, Fusion 360, 3D printed), with a problem → design process → what-went-wrong → final-result structure and a working 3D model (`models/headphone-stand.glb`). No testimonials, press, or case studies exist beyond this — do not invent any.

## Product Principles

1. Honesty over polish — document real iteration and failure, not just the finished part.
2. Niche trust over global novelty — win on being a known, reliable option, not on inventing an unprecedented idea.
3. Low-friction commissioning — pricing and the request path should let a visitor self-qualify without back-and-forth.
4. Customer-first, but not evaluator-hostile — project write-ups should primarily build a paying visitor's trust; that same honesty happens to also read well to an evaluator who clicks through from the main portfolio, but this site doesn't need to be optimized for them.
