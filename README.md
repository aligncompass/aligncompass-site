# AlignCompass — marketing site

The AlignCompass apex marketing site (`aligncompass.com`), a content-driven static **Astro** site built from the AlignCompass customer-site template. This is the **root** site: it builds with `base: "/"` and serves the domain root, not a `/slug/` subdirectory.

Built and maintained by AlignCompass. To edit copy, design tokens, or image slots, change **`src/data/content.json`** only — the Astro components render entirely from it. Push to the linked Vercel project and it rebuilds automatically. Imagery is served from Cloudinary (cloud `aligncompass`, folder `aligncompass-site`); never self-host binaries or hotlink third-party images.

```
npm install
npm run dev      # local preview
npm run build    # static output to dist/
```
