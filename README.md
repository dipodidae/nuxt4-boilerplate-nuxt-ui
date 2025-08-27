# Nuxt 4 Boilerplate with Nuxt UI

> A modern Nuxt 4 starter template, using [Nuxt UI](https://ui.nuxt.com/) instead of UnoCSS. This boilerplate is designed for rapid prototyping and production-ready Nuxt apps, with batteries included and sensible defaults.

**Repo:** [github.com/dipodidae/nuxt4-boilerplate-nuxt-ui](https://github.com/dipodidae/nuxt4-boilerplate-nuxt-ui)

## Features

- 💚 [Nuxt 4](https://nuxt.com/) — SSR, file-based routing, auto-imported components, and more
- ⚡️ Vite — Fast HMR and build
- 🎨 [Nuxt UI](https://ui.nuxt.com/) — Beautiful, customizable UI components for Nuxt
- 🔥 `<script setup>` syntax
- 🍍 [Pinia](https://github.com/vuejs/pinia) — State management
- 📑 Layout system
- 📥 Auto-imported APIs for Composition API, VueUse, and custom composables
- 🏎 Zero-config serverless functions (Nitro)
- 🦾 TypeScript-first
- 📲 [PWA](https://github.com/vite-pwa/nuxt) with offline support and auto-update
- 🧹 ESLint and code quality tools pre-configured
- 🚀 [Commitlint](https://commitlint.js.org/) — Conventional commit messages with git hooks
- 🪝 [Husky](https://typicode.github.io/husky/) — Git hooks for automated quality checks

## Plugins & Modules

- [Nuxt UI](https://ui.nuxt.com/) — UI components
- [Pinia](https://github.com/vuejs/pinia) — Store
- [VueUse](https://github.com/vueuse/vueuse) — Useful composition utilities
- [VitePWA](https://github.com/vite-pwa/nuxt) — PWA support
- [Nuxt DevTools](https://github.com/nuxt/devtools) — Enhanced DX
- [ESLint](https://eslint.org/) — Linting
- [Commitlint](https://commitlint.js.org/) — Conventional commits
- [Husky](https://typicode.github.io/husky/) — Git hooks

## IDE

We recommend [VS Code](https://code.visualstudio.com/) with [Volar](https://github.com/johnsoncodehk/volar) for the best experience. (Disable [Vetur](https://vuejs.github.io/vetur/) if you have it.)

## Usage

### Online

### Clone to local

To start a new project with this boilerplate:

```bash
npx degit dipodidae/nuxt4-boilerplate-nuxt-ui my-nuxt-app
cd my-nuxt-app
pnpm i # Or npm install -g pnpm && pnpm i
```

Or just copy this repo and start hacking!

## Development

### Commit Messages

This project uses [Commitlint](https://commitlint.js.org/) with [Conventional Commits](https://www.conventionalcommits.org/) to enforce consistent commit messages.

Examples of valid commit messages:

```bash
feat: add new counter store example
fix: resolve pageview API response type
docs: update README with commitlint info
style: format code with prettier
refactor: simplify component structure
test: add unit tests for counter store
chore: update dependencies
```

Git hooks are automatically installed via Husky to validate commit messages on `git commit`.

## Inspiration

- [vitesse-nuxt](https://github.com/antfu/vitesse-nuxt) — The original inspiration
- [nuxt/ui](https://ui.nuxt.com/) — Nuxt UI documentation

## License

MIT
