# aligncompass.com

The AlignCompass marketing site — a one-pager about the product.

AlignCompass builds and hosts simple, professional one-page websites for local
small businesses on a $35/month subscription. This site is the front door for
that product. We eat our own dog food: the marketing site is itself a single,
focused page.

## Stack

- [Astro](https://astro.build) (static output)
- Tailwind CSS v4 (`@tailwindcss/vite`)
- Deployed to Vercel at `aligncompass.com`

> Note: customer sites built by the AlignCompass agent use a different stack
> (raw HTML + Tailwind via CDN). See the playbook repo for that flow. This
> repo is for the marketing site only.

## Develop

```sh
pnpm install
pnpm dev      # http://localhost:4321
pnpm build    # outputs to ./dist
pnpm preview  # serves ./dist
```

Requires Node 22+.

## Structure

```
src/
├── layouts/
│   └── Layout.astro      # html shell, meta tags, imports global.css
├── pages/
│   └── index.astro       # the one-pager (hero → problem → benefits → steps → examples → pricing → FAQ → CTA → footer)
└── styles/
    └── global.css        # Tailwind import + a few base overrides
public/                   # favicons, static assets
```

## Editing copy

All copy lives in the frontmatter of `src/pages/index.astro` as plain JS arrays
(`benefits`, `steps`, `examples`, `faqs`). Edit the strings, save, ship.
