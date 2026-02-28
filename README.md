# Portfólio v2 (2026) · Davy Andrade

Portfólio pessoal desenvolvido com foco em **aprendizado deliberado**. Cada decisão técnica é uma oportunidade de praticar e consolidar conceitos modernos de desenvolvimento web.

> Este projeto faz parte de uma stack strategy pessoal: **Astro + React** para sites e landing pages; **Next.js** para aplicações fullstack.

---

## 🚀 Stack

| Camada | Tecnologia |
|---|---|
| Framework | [Astro 5](https://astro.build) |
| UI | [React 19](https://react.dev) + TypeScript |
| Estilização | [TailwindCSS 4](https://tailwindcss.com) + [Shadcn UI](https://ui.shadcn.com) + [Radix UI](https://radix-ui.com) |
| Ícones | [Lucide React](https://lucide.dev) |
| State | [Zustand](https://zustand.docs.pmnd.rs) |
| Data fetching | [TanStack Query](https://tanstack.com/query) |
| Forms | [React Hook Form](https://react-hook-form.com) + [Zod](https://zod.dev) |
| Animações | [Framer Motion](https://www.framer.com/motion) |
| Testes | [Vitest](https://vitest.dev) + [React Testing Library](https://testing-library.com/react) + [Playwright](https://playwright.dev) |
| Runtime | [Bun](https://bun.sh) |
| Bundler | [Vite](https://vite.dev) (via Astro) |

---

## 📁 Estrutura do projeto

```
/
├── docs/
│   ├── CLAUDE.md        # Instruções para Claude
│   ├── GEMINI.md        # Instruções para Gemini
│   └── TUTOR.md         # Filosofia de tutoria para IAs
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/          # Imagens e SVGs
│   ├── components/
│   │   ├── react/       # React islands (interativos)
│   │   └── ui/          # Componentes Shadcn (gerados por CLI)
│   ├── hooks/           # Custom hooks (use-*.ts)
│   ├── layouts/         # Layouts Astro
│   ├── lib/
│   │   ├── queries/     # TanStack Query (*.queries.ts)
│   │   └── validations/ # Schemas Zod (*.schema.ts)
│   ├── pages/           # Rotas Astro
│   ├── stores/          # Zustand stores (*.store.ts)
│   ├── styles/          # CSS global
│   └── types/           # TypeScript types (*.types.ts)
├── MILESTONES.md        # Roadmap de desenvolvimento
├── CHANGELOG.md
└── package.json
```

---

## 📄 Páginas

| Rota | Descrição |
|---|---|
| `/` | Home — Hero section |
| `/about` | Sobre mim |
| `/projects` | Projetos (GitHub API + filtros) |
| `/skills` | Habilidades e tecnologias |
| `/blog` | Lista de posts |
| `/blog/[slug]` | Post individual |
| `/contact` | Formulário de contato |

---

## 🧞 Comandos

| Comando | Ação |
|---|---|
| `bun install` | Instala as dependências |
| `bun dev` | Inicia o servidor de desenvolvimento em `localhost:4321` |
| `bun build` | Gera o build de produção em `./dist/` |
| `bun preview` | Preview local do build de produção |
| `bun test` | Executa os testes unitários e de componentes (Vitest) |
| `bun test:e2e` | Executa os testes E2E (Playwright) |
| `bunx astro add` | Adiciona uma integração Astro |
| `bunx shadcn add` | Adiciona um componente Shadcn UI |

---

## 🗺️ Roadmap

Ver [MILESTONES.md](./MILESTONES.md) para o roadmap detalhado com todos os milestones e conceitos praticados em cada fase.

---

## 🤖 Trabalhando com IA

Este projeto usa arquivos de contexto para IAs:

- [`docs/TUTOR.md`](./docs/TUTOR.md) — Filosofia socrática para sessões de aprendizado
- [`docs/CLAUDE.md`](./docs/CLAUDE.md) — Contexto e instruções para Claude
- [`docs/GEMINI.md`](./docs/GEMINI.md) — Contexto e instruções para Gemini

---

## 📝 Licença

[MIT](./LICENSE)
