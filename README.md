# Dotline marketing site

A buildless, static marketing website for Dotline. The deployable site is entirely inside `dist/`: HTML, CSS, SVG, and locally hosted WebP screenshots. No JavaScript, dependencies, analytics, forms, or third-party fonts are required.

## Preview and edit

```sh
cd "/Users/iandorosh/Documents/DotLine Marketing/site"
python3 -m http.server 4173 --directory dist --bind 127.0.0.1
```

Open http://127.0.0.1:4173. Edit `dist/index.html` for copy, navigation, contact and privacy; edit `dist/styles.css` for layout and styles. Upload the contents of `dist/` to any static web host. The Sites configuration lives in `.openai/hosting.json`.

## Content and imagery

- Brand, colors, and rounded system typography match the native Dotline app.
- Contact links open `mailto:ian.dorosh@outlook.com`; no email is sent by the website.
- Privacy policy is at the bottom of the page and directly addressable with `#privacy`.
- `duo-nine-dark.webp`: real 9×9 level 75 screenshot from the iPhone Duo simulator, unfolded, dark appearance.
- `duo-five-light.webp`: real 5×5 level 32 screenshot from the iPhone Duo simulator, unfolded, light appearance.
- `duo-start.webp`: real start screen from the iPhone Duo simulator, folded, dark appearance.
- The device surrounds are CSS illustrations. Game screenshots are not fabricated; temporary simulator progress used for capture was isolated from player saves and removed afterward.
- Original captures are in the app workspace under `build/MarketingScreenshots` and `build/DotlineNameScreenshots`. WebP exports are resized and compressed for the web.
- The line diagram in “Find your flow” is an illustrative explanation, not an interactive puzzle.

The page describes the current development build: 525 levels in seven chapters. It does not claim App Store availability or include a nonworking download button. Add the verified public App Store URL when the app is released. The App Store Connect record currently uses the previous name, Unbroken Dots.

Privacy copy reflects the current CloudKit progress implementation: completed levels, chapter unlocks, and the last played level sync through Apple's CloudKit to the player's private iCloud database when available. Progress is also cached on the device for offline play; preferences remain local to each device. No separate Dotline account is required, and the app has no ads or analytics. Website hosting may process technical information; the static page adds no tracking scripts. Revisit this copy if app or hosting behavior changes.

## Hosting

Sites publication starts owner-private at https://dotline-game.fragrantgoldfinch.chatgpt.site. Preserve that audience until a public launch is requested. If moving to another domain, update the canonical and Open Graph URLs in `dist/index.html`.

## Verification

Verified November 11, 2026:

- Desktop (1440px) and mobile (390px) screenshots reviewed; captures are in the marketing folder's `preview/` directory.
- No horizontal overflow at 320px, 390px, 900px, or 1440px.
- Navigation, contact email, privacy anchor, image loading, and local asset references checked.
- No browser errors or warnings. All three images include descriptive alternative text.
- Deployable files total approximately 96 KB, with no external script or font requests.
