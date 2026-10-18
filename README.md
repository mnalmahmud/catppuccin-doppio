<div align="center">

# ☕ Doppio

**DOP-pyoh**

An unofficial [Catppuccin](https://catppuccin.com/)-inspired color palette, built around pure black.

<img src="assets/palette.svg" alt="Doppio palette showing accents, background colors, and typography colors" width="100%">

</div>

## Palette

### Accents

| Color | Hex | Color | Hex |
| :-- | :-- | :-- | :-- |
| Rosewater | `#e2d3d0` | Yellow | `#efdcb0` |
| Flamingo | `#e1c3c2` | Green | `#96d99a` |
| Pink | `#e3b6d5` | Teal | `#8bdbcd` |
| Mauve | `#bf9ded` | Sky | `#70cedf` |
| Red | `#e680a7` | Sapphire | `#5bb8e1` |
| Maroon | `#dc95a5` | Blue | `#7babf1` |
| Peach | `#edab7d` | Lavender | `#a2aeee` |

### Background Colors

| Color | Hex | Color | Hex |
| :-- | :-- | :-- | :-- |
| Crust | `#0c0a15` | Mantle | `#06050c` |
| Base | `#000000` | Surface 0 | `#2c2c3c` |
| Surface 1 | `#414253` | Surface 2 | `#55576a` |
| Overlay 0 | `#6a6d81` | Overlay 1 | `#7e8298` |
| Overlay 2 | `#9398ae` | | |

### Typography

| Color | Hex |
| :-- | :-- |
| Text | `#c5cee9` |
| Subtext 1 | `#b2b9d1` |
| Subtext 0 | `#9ea4bc` |

## Files

| File | Format |
| :-- | :-- |
| [`doppio.json`](doppio.json) | Named hex colors |
| [`doppio.css`](doppio.css) | CSS custom properties (`--ctp-doppio-*`) |
| [`whiskers-overrides.json`](whiskers-overrides.json) | Optional Whiskers color overrides |

### CSS

Load [`doppio.css`](doppio.css) and reference the variables:

```css
@import url("./doppio.css");

body {
  background: var(--ctp-doppio-base);
  color: var(--ctp-doppio-text);
}

a {
  color: var(--ctp-doppio-blue);
}
```

<details>
<summary>Whiskers</summary>

Render a [Whiskers](https://whiskers.catppuccin.com/concepts/overrides/) template with Doppio colors and flavor names:

```sh
sed -E \
  -e 's/\{\{[[:space:]]*flavor\.identifier[[:space:]]*\}\}/doppio/g' \
  -e 's/\{\{[[:space:]]*flavor\.name[[:space:]]*\}\}/Doppio/g' \
  template.tera | whiskers - -f mocha --color-overrides whiskers-overrides.json
```

</details>

## License

[MIT](LICENSE). Doppio is an independent project, not affiliated with or endorsed by Catppuccin.
