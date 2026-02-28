# MILESTONES — Portfólio v2 (2026) · Davy Andrade

Cada milestone representa uma fase de desenvolvimento e aprendizado. O objetivo não é apenas entregar funcionalidades, mas dominar os conceitos associados a cada fase.

---

## M0 — Setup & Infraestrutura

**Objetivo:** Base sólida antes de qualquer feature

- [ ] Migrar de pnpm para Bun
- [ ] Configurar ESLint + Prettier (ou Biome)
- [ ] Configurar path aliases (`@/`)
- [ ] Instalar dependências: Zustand, Framer Motion, TanStack Query, React Hook Form, Zod
- [ ] Instalar e configurar testes: Vitest + React Testing Library + Playwright
- [ ] Limpar arquivos placeholder (Welcome.tsx, astro.svg, background.svg)
- [ ] Escrever documentação inicial (README, MILESTONES, CLAUDE.md, GEMINI.md, TUTOR.md)

**Conceitos:** Tooling, configuração de projeto, bundler (Bun + Vite)

---

## M1 — Foundation & Design System

**Objetivo:** Estrutura visual e de navegação consistente

- [ ] Layout base com Header (navegação responsiva) e Footer
- [ ] Sistema de temas dark/light com Zustand + localStorage
- [ ] ThemeToggle component (Shadcn + Radix)
- [ ] Tokens de design e tipografia no `global.css`
- [ ] SEO base: meta tags, OG tags, canonical URL no `Layout.astro`
- [ ] Componentes atômicos reutilizáveis (Button, Badge, Card, Section wrapper)
- [ ] A11y base: skip-to-content, semântica HTML, foco visível

**Conceitos:** Props vs State, Composition, Zustand, Shadcn UI, Radix UI, a11y semântica

---

## M2 — Páginas Estáticas

**Objetivo:** Conteúdo principal do portfólio

- [ ] **Hero**: animação de entrada com Framer Motion, CTA buttons
- [ ] **About**: bio, foto, timeline de experiência
- [ ] **Skills**: grid de tecnologias com categorias e ícones (Lucide + Devicons)

**Conceitos:** JSX, Conditional Rendering, Lists & Keys, Framer Motion básico

---

## M3 — Página Projects

**Objetivo:** Dados dinâmicos com GitHub API

- [ ] Fetch de repositórios com TanStack Query (GitHub REST API)
- [ ] `ProjectCard` component (nome, descrição, stars, linguagem, links)
- [ ] Filtros por linguagem/tag com `useReducer`
- [ ] Estados de loading / error / empty com Suspense
- [ ] Query params na URL para filtros persistentes (`URLSearchParams`)

**Conceitos:** TanStack Query, useReducer, Conditional Rendering, Lists & Keys, Web APIs

---

## M4 — Contato

**Objetivo:** Formulário funcional e validado

- [ ] Formulário completo com React Hook Form + Zod (nome, email, mensagem)
- [ ] Validação client-side em tempo real com feedback visual
- [ ] Submit handler (mailto: ou API route futura)
- [ ] Estados de loading, sucesso e erro
- [ ] A11y: ARIA live regions para feedback, labels corretos

**Conceitos:** React Hook Form, Zod, Events, Controlled vs Uncontrolled, a11y de formulários

---

## M5 — Blog

**Objetivo:** Conteúdo editorial com Astro Content Collections

- [ ] Configurar Content Collections para posts (MDX)
- [ ] `BlogList` com paginação
- [ ] `BlogPost` layout com Table of Contents, leitura estimada
- [ ] Tags e categorias com filtros
- [ ] RSS feed (Astro integration)

**Conceitos:** Astro Content Collections, MDX, Static Site Generation, SEO de conteúdo

---

## M6 — Polish, Performance, Segurança & Acessibilidade

**Objetivo:** Portfólio pronto para produção com qualidade profissional

### Animações
- [ ] Scroll animations com Framer Motion
- [ ] Page transitions
- [ ] Micro-interações em hover/focus
- [ ] Respeitar `prefers-reduced-motion`

### Acessibilidade (WCAG AA)
- [ ] Auditoria ARIA completa
- [ ] Focus management (modal, mobile menu, pós-submit)
- [ ] Color contrast WCAG AA (dark + light)
- [ ] Keyboard navigation em todos os componentes
- [ ] Screen reader testing (NVDA / VoiceOver)

### Web Components
- [ ] `<scroll-progress>` — barra de progresso de leitura com Shadow DOM
- [ ] `<back-to-top>` — botão flutuante com HTML Template

### Performance
- [ ] Core Web Vitals: LCP, INP, CLS — medir e otimizar
- [ ] Islands Architecture refinada (`client:idle` vs `client:visible`)
- [ ] Streamed Responses em páginas com dados assíncronos
- [ ] Astro `<Image />`, WebP, lazy loading
- [ ] Bundle analysis com vite-bundle-visualizer
- [ ] Font optimization (`font-display: swap`, self-hosted)
- [ ] PWA básica: Web App Manifest + Service Worker (offline fallback)
- [ ] DevTools: Performance panel, Coverage, Network analysis

### Segurança
- [ ] Content Security Policy (CSP) headers
- [ ] CORS configurado corretamente para GitHub API
- [ ] HTTPS (automático no deploy, entender o porquê)
- [ ] OWASP básico: XSS awareness, sanitização de input, Referrer-Policy/HSTS

### Vite & Bundler
- [ ] Entender configuração de plugins Vite no projeto
- [ ] Analisar chunking e tree-shaking no build
- [ ] Compreender o papel de esbuild (transpilação) e Rollup (build) no Vite

### Infraestrutura
- [ ] Sitemap + robots.txt (Astro integrations)
- [ ] Lighthouse: meta 100/100 Performance, Accessibility, SEO

**Conceitos:** Framer Motion avançado, WCAG AA, Web Components, Core Web Vitals, Islands Architecture, CSP, CORS, OWASP, Vite internals

---

## M6.5 — Testes

**Objetivo:** Confiança para deploy com cobertura de testes

### Vitest + React Testing Library
- [ ] Custom hooks (`useTheme`, `useGitHubRepos`, `useScrollProgress`)
- [ ] Componentes atômicos (renderização, props, eventos)
- [ ] Store Zustand
- [ ] Schema Zod (validações)
- [ ] Formulário de contato (validação + submit)

### Playwright (E2E)
- [ ] Navegação entre todas as páginas
- [ ] Fluxo completo de envio do formulário de contato
- [ ] Filtros de projetos (selecionar, limpar, URL params)
- [ ] Toggle de tema (dark/light + persistência)
- [ ] Acessibilidade E2E (axe-playwright)

**Conceitos:** Testing pyramid, unit vs integration vs E2E, mocking, test coverage

---

## M7 — Deploy

**Objetivo:** Portfólio no ar com CI/CD profissional

- [ ] Escolher plataforma (Vercel ou Cloudflare Pages — ambas excelentes para Astro)
- [ ] Configurar GitHub Actions com Lighthouse CI integrado
- [ ] Cache-Control headers para assets estáticos
- [ ] Domínio customizado
- [ ] Monitoramento básico (analytics privacy-friendly)

**Conceitos:** CI/CD, Lighthouse CI, Cache-Control, DNS, deploy de sites estáticos

---

## Projetos separados recomendados

| Projeto | Foco de aprendizado |
|---|---|
| **React Patterns Playground** | HOC, Render Props, Compound Components |
| **Task Manager** | useReducer avançado, state machine, Jotai |
| **GitHub Explorer** | Apollo Client + GraphQL (GitHub API v4) |
| **Mini Dashboard** | Jotai vs Zustand, TanStack Query avançado |
| **Web Components Workshop** | Custom Elements avançados, Shadow DOM, slots, lifecycle |
| **Pomodoro (reescrita)** | PWA completa, Service Workers, Cache strategies, Workbox, Background Sync |
| **Auth Project** | JWT, OAuth 2.0, Sessions, OWASP avançado (CSRF, rate limiting) |
| **Bundlers Playground** | Vite avançado, Rolldown, Parcel, comparação de configurações |
