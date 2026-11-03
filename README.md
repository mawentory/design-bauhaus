# Bauhaus — design reference

**Primaries on cream**

One page showing every component in this design, rendered from its own design
tokens. No build step, no dependencies: open `index.html`.

**[View the component gallery →](https://mawentory.github.io/design-bauhaus/)**

![Bauhaus](preview.png)

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Component gallery — every component on one page |
| `DESIGN.md` | The design notes: origin, palette, type, shape, measured contrast |
| `theme.css` | The 66 design tokens, plus derived accessibility values |
| `design.css` | Component styles, written against tokens only |
| `fonts.css` | `@font-face` declarations for the fonts this design uses |
| `fonts/` | Latin-subset woff2 files, self-hosted |

`design.css` contains no colour, radius or font literal. That is deliberate: the
same stylesheet drives all ten designs and only `theme.css` differs, so the
gallery doubles as a test that the token set is complete.

## The design

Bauhaus print and signage: cream stock, red/yellow/blue primaries used as structure, and geometry that stays orthogonal.

**Type** — Space Grotesk at 700 for display, Inter for body. The display face is geometric; the body face is neutral so long copy stays quiet.

**Shape** — Zero radii and 3px borders, weighty enough to read as drawn geometry.

**Signature moves**

- Sequence markers cycling through the primaries, one per item.
- A coloured band under the header.
- Square geometry with borders as the only ornament.

## Colour

| Token | Value | Role |
| --- | --- | --- |
| `--paper` | `#f2e9d8` | Page ground |
| `--sheet` | `#faf4e8` | Raised surfaces |
| `--ink` | `#1a1a1a` | Primary text |
| `--signal` | `#e03a2f` | Action |
| `--signal-text` | `#bc3127` | Action, when it has to be read |
| `--focus-ring` | `#e03a2f` | Focus indicator |

## Accessibility

Every colour pair this design can render as text is checked against WCAG 2.1
when the repo is generated — page surfaces, panel surfaces, and the tinted fills
of badges and diff lines. The full table is in
[DESIGN.md](DESIGN.md#contrast-measured); the gallery is separately audited in a
real browser for heading order, duplicate ids, unlabelled controls and
horizontal overflow at 1280px and 390px.

## Using it

Set the theme attribute on your root element and load the two stylesheets:

```html
<html data-theme="bauhaus">
  <link rel="stylesheet" href="fonts.css" />
  <link rel="stylesheet" href="theme.css" />
  <link rel="stylesheet" href="design.css" />
</html>
```

Because the tokens are namespaced by attribute, this theme can sit alongside
another one in the same page.

## The rest of the set

[Placa](https://github.com/mawentory/design-placa), [Blueprint](https://github.com/mawentory/design-blueprint), [Phosphor](https://github.com/mawentory/design-fosforo), [Press](https://github.com/mawentory/design-imprensa), [Swiss](https://github.com/mawentory/design-suico), [Neon](https://github.com/mawentory/design-neon), [Brutalist](https://github.com/mawentory/design-brutalista), [Botanical](https://github.com/mawentory/design-botanico), [Vidro](https://github.com/mawentory/design-vidro).

---

Part of the MarvinRouter design set. Generated from a single template; see
`DESIGN.md` for the values behind it.
