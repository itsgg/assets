# Web fonts for itsgg.com

The site loads these files through jsDelivr from a tag of this repository:

```text
https://cdn.jsdelivr.net/gh/itsgg/assets@fonts-v1/fonts/<file>
```

A tag never changes, so jsDelivr serves them with a one-year immutable cache.
GitHub Pages, which hosts the site, caches every file for ten minutes, after
which a returning visitor's browser re-checks each font and shows the
fallback face while it waits. To change a font, add the new files under a new
tag (`fonts-v2`) and point the site at it; never move an existing tag.

| File | Family | Version | Covers |
| --- | --- | --- | --- |
| `inter-latin.woff2`, `inter-latin-ext.woff2` | Inter, weights 400 to 700 | 4.001 | body text |
| `space-grotesk-latin.woff2`, `space-grotesk-latin-ext.woff2` | Space Grotesk, weights 500 to 700 | 2.000 | headings |
| `fraunces-latin.woff2`, `fraunces-latin-ext.woff2` | Fraunces, weights 600 to 700 | 1.000 | book titles |
| `fraunces-italic-latin.woff2`, `fraunces-italic-latin-ext.woff2` | Fraunces Italic, weights 400 to 500 | 1.000 | book subtitles, quotes |

Each is a variable font as Google Fonts serves it (fetched 2026-10-11 from the
css2 API), split into Google's latin and latin-ext subsets; the site's
`@font-face` rules carry the matching `unicode-range`, so a page downloads
latin-ext only when it uses one of those letters.

All three families are licensed under the SIL Open Font License 1.1
([OFL.txt](OFL.txt)): Copyright 2016 The Inter Project Authors, Copyright 2020
The Space Grotesk Project Authors, Copyright 2018 and 2020 The Fraunces Project
Authors.
