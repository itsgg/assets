# Web fonts for itsgg.com

The site loads these files through jsDelivr, by the full commit hash of the
latest tag (`fonts-v2`):

```text
https://cdn.jsdelivr.net/gh/itsgg/assets@<full commit hash of fonts-v2>/fonts/<file>
```

The hash itself is in the site's `_sass/itsgg/_fonts.scss` (`$font-cdn`).

jsDelivr serves a full commit hash with a one-year immutable cache. A tag
name that is not a semantic version (`fonts-v2`) or a short hash gets only
seven days, checked 2026-10-11, so the site uses the hash and the tag is
the label for people.

GitHub Pages, which hosts the site, caches every file for ten minutes, after
which a returning visitor's browser re-checks each font and shows the
fallback face while it waits. To change a font, add the new files, tag the commit
`fonts-v3` and point the site at its full hash; never move an existing tag.
`fonts-v1` is the same set without JetBrains Mono.

| File | Family | Version | Covers |
| --- | --- | --- | --- |
| `inter-latin.woff2`, `inter-latin-ext.woff2` | Inter, weights 400 to 700 | 4.001 | body text |
| `space-grotesk-latin.woff2`, `space-grotesk-latin-ext.woff2` | Space Grotesk, weights 500 to 700 | 2.000 | headings |
| `fraunces-latin.woff2`, `fraunces-latin-ext.woff2` | Fraunces, weights 600 to 700 | 1.000 | book titles |
| `fraunces-italic-latin.woff2`, `fraunces-italic-latin-ext.woff2` | Fraunces Italic, weights 400 to 500 | 1.000 | book subtitles, quotes |
| `jetbrains-mono-400.woff2`, `jetbrains-mono-500.woff2` | JetBrains Mono, 400 and 500 | 2.211 | code, dates, labels |

Inter, Space Grotesk and Fraunces are variable fonts as Google Fonts serves them
(fetched 2026-10-11 from the css2 API), split into Google's latin and
latin-ext subsets; the site's
`@font-face` rules carry the matching `unicode-range`, so a page downloads
latin-ext only when it uses one of those letters. JetBrains Mono is a custom
subset that keeps latin, box drawing, block elements and arrows, so ASCII
diagrams in code blocks line up.

All four families are licensed under the SIL Open Font License 1.1
([OFL.txt](OFL.txt)): Copyright 2016 The Inter Project Authors, Copyright 2020
The Space Grotesk Project Authors, Copyright 2018 and 2020 The Fraunces Project
Authors, Copyright 2020 The JetBrains Mono Project Authors.
