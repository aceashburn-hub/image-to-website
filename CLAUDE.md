This folder builds websites from images (screenshots, mockups, sketches, wireframes).
Every request follows the 3-step workflow below. Never skip step 2.

## Step 1: Receive the image
- The user provides an image by pasting it, dragging it in, or giving a file path.
- If no image was provided, ask for one. Don't guess.
- If the image is blurry, cropped, or ambiguous, say what's unclear.

## Step 2: Verify before building (required)
Before writing any files, analyze the image and present a build plan:

1. **Page type**: e.g. landing page, portfolio, dashboard, blog
2. **Sections**: list them top to bottom (nav, hero, features, footer...)
3. **Layout**: columns and grid structure, how it should adapt on mobile
4. **Colors**: approximate hex values picked from the image
5. **Typography**: closest Google Font matches, heading and body sizes
6. **Text content**: text read from the image, plus anything that will be placeholder
7. **Images/icons**: what will be placeholders (no copyrighted assets)
8. **Interactivity**: menus, buttons, forms, and how they'll behave
9. **Tech stack**: default is plain HTML + CSS + vanilla JS unless the user asks otherwise
10. **Output folder**: `./sites/<site-name>/`

Then ask: **"Does this plan look right? Reply 'yes' to build, or tell me what to change."**
- Don't create or modify any files until the user explicitly approves.
- If the user asks for changes, update the plan and ask for approval again.

## Step 3: Build the site locally
After approval:
- Create the site in `./sites/<site-name>/` with:
  - `index.html`
  - `styles.css`
  - `script.js` (only if interactivity is needed)
  - `assets/` (placeholder images, SVG icons)
- Requirements:
  - Responsive (desktop, tablet, phone)
  - Semantic HTML and basic accessibility (alt text, labels, contrast)
  - Match the image's layout, spacing, and colors as closely as possible
  - No build tools or frameworks unless requested; it should open by double-clicking
- When done:
  1. Open it in the browser: `Start-Process ./sites/<site-name>/index.html` (Windows), `open` (macOS), or `xdg-open` (Linux)
  2. Summarize what was built and list any differences from the image
  3. Ask if the user wants adjustments

## Rules
- Work only inside this folder. Never touch files outside `./sites/`.
- Never deploy or publish anything online. Everything stays local.
- Never overwrite an existing site folder without asking first.
- For revisions, edit the existing files instead of rebuilding from scratch.
