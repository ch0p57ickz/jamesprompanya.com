# Portfolio site guide

This repository contains James Prompanya's single-page portfolio. Use this file when changing its content, layout, or deployment. The user-provided mock is the visual reference; the current site and facts below are the implementation baseline.

## Project and local preview

- Site source: `site/dist/index.html` (HTML, CSS, and a small amount of JavaScript in one file).
- Professional header photo: `site/dist/james-header.jpg` (supplied by James).
- Selected Work cards use three illustrative stock photos in `site/dist/work-*.jpg`. Their photographers, source pages, and licenses are recorded in `site/PHOTO_CREDITS.md`. They do not depict James's actual team or systems.
- Background listings use company marks in `site/dist/brands/`. Their sources are recorded in `site/BRAND_ASSETS.md`; keep the historical Niantic mark distinct from Niantic Spatial.
- Sites hosting manifest: `site/.openai/hosting.json`. The current Sites deployment is private to James. Do not create a replacement Site when updating it; use the existing project ID from the manifest and preserve its audience.
- There is no build step. Preview locally with `cd site && python3 -m http.server 8000 --directory dist`, then open `http://localhost:8000`.
- The static `site/dist` directory is also suitable for Cloudflare Pages. A separate Cloudflare Pages deployment has not been set up in this repository.

## Purpose and structure

Visitors should be able to understand James's professional work and explore his personal interests without leaving the page. The header has a centered two-option switch. The Professional view is the default; Personal is the second view. Both use the same name and overall layout, with different accent colors and content. Hash links (`#professional`, `#personal`, `#work`, `#interests`, `#running`, `#photography`, and `#lab`) make the views and sections shareable. Keep the switch usable by mouse, touch, and keyboard, and maintain the current tab semantics.

### Professional view: current content

- Hero: James's supplied photo on the left and his introduction on the right. The headline is “I build systems that help engineers move faster.” A prominent LinkedIn link points to `https://www.linkedin.com/in/jamesprompanya`.
- Role: Director of Engineering at Scopely Explore (formerly Niantic), working on Pokémon GO. The location is **San Francisco Bay Area, CA**, shown with a location marker.
- Expertise tags, in order: Engineering Leadership; AI Developer Platforms; Infrastructure Engineering; Internal Tools; Site Reliability Engineering.
- Selected work: (1) leading adoption of agentic and AI-assisted development workflows, including RAG patterns and realistic expectations; (2) modernizing tooling and infrastructure to reduce manual work and human error; (3) improving infrastructure resiliency during events and machine stock outages. Do not add numerical impact claims without James's source material.
- Supporting sections: “How I work” and a concise background listing Scopely Explore, Niantic, and Microsoft.

### Personal view: current content

The personal hero uses an orange accent and James's supplied portrait with the headline "Software engineer. Marathoner. Gamer. Tinkerer." It introduces three interests presented as numbered sections: running, photography, and the lab (local AI agent experiments). Each section has a header with a disabled "view all" button and a four-up card grid. The race cards, photo tiles, and lab setup cards are currently placeholder skeletons (Race / Year / Time, Photo 1–4 of 4, Setup / Placeholder — awaiting details) because James has not supplied personal galleries, race results, or details of specific home projects. The "Camera and category details to come." line under the photography grid is a placeholder and should be replaced once James confirms his gear and category list. The section leads reuse James's approved copy from the previous version of the site.

## Design direction from the supplied mock

The mock shows both views side by side for comparison; the actual site presents one view at a time. Carry forward these design traits when extending the page:

- A dark outer canvas framing a bright, rounded page surface.
- A narrow header: uppercase name at the left, centered pill-shaped Professional/Personal switch, compact navigation and theme control at the right.
- A split hero with a large image or visual panel on the left and generous editorial typography on the right. The current professional and personal views use the supplied portrait photos. Keep the text readable and the important people visible at desktop and phone widths.
- Professional palette: deep navy, cool blue-gray, white surfaces, subtle borders, and small topic chips. Personal palette: warm rust/orange accents and a softer warm background. The theme toggle also supports a dark palette.
- Clear section numbering, short headings, restrained cards, modest spacing between groups, and strong contrast between large headings and quiet supporting text.
- The mock's Professional view suggests Selected Work cards, a “How I Work” row, and a Lab row. Its Personal view suggests horizontal groups for Running, Photography, Games, and a Lab. These are layout and expansion ideas; only the content listed above is currently confirmed.
- The mock shows many illustrative photos, marathon times, named games, projects, social accounts, a résumé link, and a different location. **Do not treat those as facts about James or copy them into the site without his confirmation and assets.**

## Change guidance

- Keep the two views visually related and make content changes in the relevant view only. Preserve the supplied professional photo unless James asks to replace it.
- Use James's own wording and examples for claims about work or personal accomplishments. Link to LinkedIn instead of assuming its content can be fetched reliably.
- Prefer real, supplied images for personal galleries. Do not create a fake portrait or imply a stock image is James's own photography.
- Check desktop and phone layouts after visual changes; tag rows should wrap without horizontal scrolling. Keep accessible labels, visible focus states, and reduced-motion support.
- For site edits, publish the updated version to the existing private Site unless James explicitly asks for local-only work or another hosting target. Documentation-only edits do not require a site deployment.
