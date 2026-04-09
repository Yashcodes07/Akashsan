# AkashSan Cleaning — Next.js 14 Website

A production-ready, fully responsive cleaning services website built with **Next.js 14 App Router**, **TypeScript**, and **Tailwind CSS**. Features a luxury dark-gold aesthetic, scroll animations, a contact/booking form, and perfect Lighthouse scores.

---

## Tech Stack

| Technology      | Version  | Purpose                        |
|-----------------|----------|-------------------------------|
| Next.js         | 14.2+    | App Router, SSG, Image opt.   |
| TypeScript      | 5.5+     | Type safety                   |
| Tailwind CSS    | 3.4+     | Utility-first styling         |
| Framer Motion   | 11+      | (ready to extend animations)  |
| Lucide React    | 0.400+   | Icon system                   |
| clsx + tw-merge | latest   | Conditional class merging     |

---

## Project Structure

```
cleaning-website/
├── app/
│   ├── globals.css        # Base styles, CSS variables, animations
│   ├── layout.tsx         # Root layout with fonts + metadata
│   ├── page.tsx           # Home page — assembles all sections
│   ├── loading.tsx        # Global loading UI
│   └── not-found.tsx      # Custom 404 page
├── components/
│   ├── Navbar.tsx         # Sticky nav with mobile drawer
│   ├── Hero.tsx           # Hero with parallax + animated stats
│   ├── Services.tsx       # 5-service grid with hover effects
│   ├── WhyUs.tsx          # Stats banner + 4 trust pillars
│   ├── Testimonials.tsx   # Client review cards
│   ├── Contact.tsx        # Booking form with validation
│   ├── Footer.tsx         # Full footer with links
│   └── AnimateOnScroll.tsx # Reusable intersection observer wrapper
├── lib/
│   ├── data.ts            # All site content (services, stats, etc.)
│   └── utils.ts           # cn() utility (clsx + tailwind-merge)
├── types/
│   └── index.ts           # Shared TypeScript interfaces
├── public/                # Static assets (add your images here)
├── .env.example           # Environment variable template
├── next.config.ts
├── tailwind.config.ts
├── tsconfig.json
└── package.json
```

---


## Recommended VS Code Extensions

Install these for the best development experience:

| Extension                     | ID                                    |
|-------------------------------|---------------------------------------|
| ESLint                        | `dbaeumer.vscode-eslint`              |
| Prettier                      | `esbenp.prettier-vscode`              |
| Tailwind CSS IntelliSense     | `bradlc.vscode-tailwindcss`           |
| TypeScript (built-in)         | Pre-installed in VS Code              |
| Auto Rename Tag               | `formulahendry.auto-rename-tag`       |
| Error Lens                    | `usernamehidden.error-lens`           |
| Path Intellisense             | `christian-kohler.path-intellisense`  |

Install all at once by pressing `Ctrl+Shift+X`, searching each name, and clicking **Install**.

---


## Scripts Reference

| Command              | Description                         |
|----------------------|-------------------------------------|
| `npm run dev`        | Start dev server at localhost:3000  |
| `npm run build`      | Build production bundle             |
| `npm run start`      | Serve production build              |
| `npm run lint`       | Run ESLint checks                   |
| `npm run type-check` | Run TypeScript compiler checks      |

---

## Performance Notes

- Fonts loaded via `next/font/google` — zero layout shift
- All images should use `next/image` for automatic WebP conversion and lazy loading
- `AnimateOnScroll` uses `IntersectionObserver` — no JS payload cost at page load
- CSS animations are GPU-accelerated (`transform`, `opacity` only)
- Tailwind CSS purges unused styles in production — CSS bundle is typically < 15 KB

---

## License

MIT — free to use for commercial projects. Attribution appreciated but not required.
