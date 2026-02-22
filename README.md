# TalShiar — Romulan Violet Roundcube Skin

A dark Romulan-themed skin for [Roundcube Webmail](https://roundcube.net/), inspired by the Tal Shiar intelligence service. Deep violet surfaces, emerald green accents, sharp angular UI elements, and a cloaking device shimmer animation.

**VIGILANCE ETERNAL**

## Features

- Deep violet/purple primary color palette with emerald green accents
- Angular clip-path buttons with cloaking shimmer animation
- Intelligence terminal scan-line overlay (thin, refined)
- Violet glow headers/footers with emerald focus states
- Dark background email reading with forced light text
- Stylized raptor emblem logo
- Noto Sans typography
- Full dark mode support
- Mobile-optimized (animations disabled on small screens)

## Color Palette

| Role | Value | Description |
|------|-------|-------------|
| Primary accent | `#7b2d8e` | Deep violet |
| Secondary accent | `#1a8a5a` | Emerald green |
| Links | `#20c080` | Bright emerald |
| Base black | `#0c0a10` | Near-black purple |
| Body text | `#c8c0d8` | Cool silver-lavender |
| Error | `#cc2200` | Red alert |
| Warning | `#c87020` | Amber-orange |

## Installation

Copy the skin into your Roundcube `skins/` directory:

```bash
cp -r TalShiar /path/to/roundcube/skins/
```

Then activate in `config/config.inc.php`:

```php
$config['skin'] = 'TalShiar';
$config['skin_logo'] = [
    '*'           => '/skins/TalShiar/images/logo.svg',
    '[dark]'      => '/skins/TalShiar/images/logo.svg',
    '[small]'     => '/skins/TalShiar/images/logo.svg',
    '[small-dark]'=> '/skins/TalShiar/images/logo.svg',
];
```

## Building CSS from Source

The skin uses Less CSS. To rebuild after modifying `.less` files:

```bash
npm init -y
npm install less less-plugin-clean-css
npx lessc --clean-css="--s1 --advanced" styles/styles.less styles/styles.min.css
npx lessc --clean-css="--s1 --advanced" styles/print.less styles/print.min.css
npx lessc --clean-css="--s1 --advanced" styles/embed.less styles/embed.min.css
rm -rf node_modules package.json package-lock.json
```

## Based On

The Elastic skin by The Roundcube Dev Team, licensed under [Creative Commons Attribution-ShareAlike](http://creativecommons.org/licenses/by-sa/3.0/).

## License

Creative Commons Attribution-ShareAlike 3.0
