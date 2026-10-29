# Car Info

A static car information website built with current HTML and CSS. The project
is a boilerplate: the layout, styling system, and content structure are in
place, while car data, copy, and photography are placeholders ready to replace.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Home page with hero, featured cars, and editorial approach |
| `cars.html` | Car listing grid |
| `car-detail.html` | Reusable car profile with specifications and overview |

## Project structure

```text
.
├─ index.html
├─ cars.html
├─ car-detail.html
├─ favicon.svg
├─ assets/
│  ├─ fonts/            Empty, reserved for self-hosted fonts
│  ├─ icons/            Logo and specification icons
│  └─ images/           Placeholder car artwork
├─ css/
│  ├─ main.css          Layer order and imports
│  ├─ reset.css         Modern reset
│  ├─ tokens.css        Colors, type, spacing, and layout tokens
│  ├─ base.css          Element defaults
│  ├─ layout.css        Page structure and grids
│  └─ components.css    Buttons, cards, navigation, and other components
├─ .editorconfig
└─ README.md
```

## Preview locally

Open `index.html` directly in a browser, or serve the folder for a more
representative setup:

```sh
npx serve .
```

There is no build step, package manager, or JavaScript requirement.

## Styling system

CSS is split into modules and loaded through `css/main.css`. Cascade layers keep
the order predictable regardless of selector specificity:

```css
@layer reset, tokens, base, layout, components;
```

Edit design decisions in `css/tokens.css`. Colors use the CSS `light-dark()`
function and follow the visitor's system preference automatically. The header
and footer intentionally use a fixed dark palette in both themes so the brand
stays consistent.

Typography uses locally available font stacks. To use a custom typeface, add
the font files to `assets/fonts/`, declare `@font-face` in `css/base.css`, and
update `--font-display` or `--font-body` in `css/tokens.css`. Avoid linking
third-party font services if the project should stay self-contained.

## Placeholder content

The following items are intentionally generic:

- Car names, specification values, prices, and editorial copy.
- SVG car artwork in `assets/images/`.
- Social sharing metadata, which is commented out until a real domain and
  raster image are available.
- Year and copyright line.

Header and footer markup is duplicated across the three pages because plain HTML
has no template include. When changing navigation, update all three files.

## Before publishing

1. Replace placeholder car data and artwork with verified information.
2. Update titles, descriptions, canonical URLs, and Open Graph tags.
3. Add real raster images and an `og-cover.png` for social sharing.
4. Run the pages through an HTML validator and a Lighthouse audit.
5. Check keyboard navigation, focus states, and both color schemes.
6. Add `robots.txt`, `sitemap.xml`, and a privacy policy if the site collects
   analytics or personal data.

## License

MIT. See [LICENSE](LICENSE).
