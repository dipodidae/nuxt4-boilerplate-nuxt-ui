<div align="center">

# Nuxt 4 + Nuxt UI Boilerplate

Fast, typed, production‑oriented starter for Nuxt 4.
Clone → Install → Build features. No trimming required.

<sup>Nuxt 4 • Vite • TypeScript • Nuxt UI • Pinia • VueUse • PWA • Nitro • ESLint • Git Hooks</sup>

</div>

---

## Purpose

A minimal but opinionated baseline for apps that need:

- Instant DX (Vite HMR + typed pages)
- A coherent, accessible design system (Nuxt UI)
- Hybrid delivery (SSR, prerender, API routes)
- Progressive enhancement (offline + SW auto update)
- Guardrails for commits, linting, typing
- Straightforward SSR or static deployment paths

Remove pieces freely—nothing is tangled.

---

## Highlights

| Area      | Included                                      |
| --------- | --------------------------------------------- |
| Framework | Nuxt 4 (hybrid SSR / SSG)                     |
| UI Layer  | Nuxt UI (tokens, components, theming)         |
| State     | Pinia (auto registered)                       |
| Utilities | VueUse auto imports                           |
| PWA       | `@vite-pwa/nuxt` (autoUpdate)                 |
| Types     | TypeScript + `typedPages`                     |
| Quality   | ESLint (Antfu) + lint-staged + commitlint     |
| Tooling   | Nuxt DevTools (dev only)                      |
| Deploy    | Docker (multi-stage) + static generate option |

---

## Installation

```bash
npx degit dipodidae/nuxt4-boilerplate-nuxt-ui my-app
cd my-app
pnpm install
pnpm dev
```

Dev with service worker:

```bash
pnpm dev:pwa
```

Open http://localhost:3000

---

## Scripts

| Command             | Description                      |
| ------------------- | -------------------------------- |
| pnpm dev            | Dev server (HMR)                 |
| pnpm dev:pwa        | Dev + PWA (SW opt‑in)            |
| pnpm build          | Production SSR build → `.output` |
| pnpm preview        | Preview SSR locally              |
| pnpm generate       | Static export (experimental)     |
| pnpm start          | Run built SSR server             |
| pnpm start:generate | Serve generated static bundle    |
| pnpm lint           | ESLint (staged files use hooks)  |
| pnpm typecheck      | vue-tsc / TS checks              |

---

## PWA

Config: `app/config/pwa.ts`

- `registerType: autoUpdate`
- Google Fonts runtime caching
- Maskable + standard icons
- Navigation fallback excludes `/api/*`
- Dev opt‑in via `VITE_PLUGIN_PWA=true` (`pnpm dev:pwa`)

---

## API Example

`server/api/pageview.ts` returns JSON. Any file in `server/api` becomes `/api/<name>`. Extend with caching, adapters, or platform presets as needed.

---

## Git Workflow

| Hook       | Action                            |
| ---------- | --------------------------------- |
| pre-commit | lint-staged (ESLint + auto-fix)   |
| commit-msg | commitlint (Conventional Commits) |

Reapply after editing config:

```bash
pnpm dlx simple-git-hooks
```

---

## Deployment

### Docker (SSR)

```bash
docker build -t my-app .
docker run -p 3000:3000 my-app
```

### Static Hosting

```bash
pnpm generate
# deploy dist/
```

### Netlify

SSR:

1. Set `NITRO_PRESET=netlify`
2. Build with `pnpm build`
3. Publish `.output/public`

Static:

1. `pnpm generate`
2. Publish `dist`

Ensure `netlify.toml` matches chosen mode.
