# Image to Website

A [Claude Code](https://claude.com/claude-code) workflow template that turns images into working websites. You give it a screenshot, mockup, sketch, or wireframe, and it builds a responsive site in plain HTML, CSS, and JavaScript.

## How it works

The instructions are in [CLAUDE.md](CLAUDE.md). Claude Code reads that file automatically and follows three steps:

1. **Receive the image.** Paste it, drag it in, or give a file path.
2. **Verify the plan.** Before writing any files, Claude presents a build plan: sections, layout, colors, fonts, text, placeholders, interactivity, and output folder. Nothing gets built until you reply "yes".
3. **Build locally.** The site is created in `sites/<site-name>/` and opened in your browser.

## Usage

```bash
git clone https://github.com/aceashburn-hub/image-to-website.git
cd image-to-website
claude
```

Then paste an image and say something like "build this".

## Output

Each site goes in its own folder:

```
sites/
  my-site/
    index.html
    styles.css
    script.js     # only if the site needs interactivity
    assets/       # placeholder images and SVG icons
```

Sites are responsive, use semantic HTML with basic accessibility, and need no build tools. Double-click `index.html` to open one.

## Customizing

Edit `CLAUDE.md` to change the defaults. For example, you can switch the tech stack to Tailwind or React, change the output folder, or add your own design rules.

## Notes

- Generated sites go in `sites/`, which git ignores, so your builds stay private.
- Images and icons are placeholders. Claude won't copy copyrighted assets from your reference image.

## License

[MIT](LICENSE)
