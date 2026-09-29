# trythisone-site

The marketing and support pages for **Try This One**, an iPhone app.

Plain HTML pages and one stylesheet. No build step, no dependencies —
edit a file, commit, push, and GitHub Pages republishes it.

```
index.html     the landing page      (App Store "Marketing URL")
support.html   help and contact      (App Store "Support URL")
tto.css        every colour, size and surface, in one file
assets/        the app icon, at the three sizes a browser asks for
images/        screenshots — see images/README.md
```

## Where the design comes from

Nothing here was invented. The palette, the type scale, the corner radii and
the frosted-glass recipe are all lifted from the app's own design system, and
each one is commented in `tto.css` with the Swift file it came from:

| In `tto.css`               | In the app                       |
|----------------------------|----------------------------------|
| accents, tab colours, grounds | `DesignSystem/Colors.swift`   |
| the shipped accent trio    | `DesignSystem/TTOTheme.swift`    |
| Quicksand / Mali, the size scale | `DesignSystem/Typography.swift` |
| `.glass`, the radius scale | `Shared/TTOGlass.swift`          |
| the dot grid, the corner glows | `Shared/TTOBackground.swift` |

If one of those moves in the app, move it here.

## Things still to do

- **The App Store badge is a placeholder.** It's drawn in the app's own style
  and links to `#`. Apple requires its own artwork — when the app is approved,
  take the badge from
  [Apple's marketing guidelines](https://developer.apple.com/app-store/marketing/guidelines/)
  and replace the whole `<a class="badge">` element with it and the real link.
- **The landing copy is the pitch.** `index.html` is built from the pitch
  written Sep 28. Every feature it names is in the release build; if a
  `Features` flag changes what v1 ships, change the page with it.
- **The FAQ copy is a first draft.** Read it through before submitting. It
  matches what the app does today; the billing answer is the one to revisit if
  the app ever stops being free.

## Editing

Open a file in any editor. To see a change before pushing:

```bash
python3 -m http.server 8000
```

then visit <http://localhost:8000>.
