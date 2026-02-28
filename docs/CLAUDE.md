# CLAUDE.md — Instruções para Claude

Este arquivo contextualiza o projeto para que Claude possa ajudar de forma eficiente e alinhada com os objetivos de aprendizado.

---

## Sobre o projeto

**Nome:** Portfólio v2 (2026) — Davy Andrade  
**Tipo:** Portfólio pessoal multi-página (site estático com islands interativos)  
**Objetivo principal:** Aprendizado deliberado — este projeto é um laboratório prático de tecnologias web modernas  
**Stack strategy:** Astro + React para sites/landing pages; Next.js para fullstack

---

## Stack técnica

| Camada | Tecnologia |
|---|---|
| Framework | Astro 5 |
| UI | React 19 + TypeScript |
| Estilização | TailwindCSS 4 + Shadcn UI (New York/Zinc) + Radix UI |
| Ícones | Lucide React |
| State | Zustand |
| Data fetching | TanStack Query (REST) |
| Forms | React Hook Form + Zod |
| Animações | Framer Motion |
| Testes | Vitest + React Testing Library + Playwright |
| Runtime/Bundler | Bun + Vite (via Astro) |

---

## Estrutura do projeto

```
src/
├── assets/           # Imagens, SVGs estáticos
├── components/
│   ├── react/        # React islands (interativos)
│   └── ui/           # Componentes Shadcn (gerados por CLI)
├── hooks/            # Custom hooks (use-*.ts)
├── layouts/          # Layouts Astro
├── lib/
│   ├── queries/      # TanStack Query (*.queries.ts)
│   └── validations/  # Schemas Zod (*.schema.ts)
├── pages/            # Rotas Astro
├── stores/           # Zustand stores (*.store.ts)
├── styles/           # CSS global
└── types/            # TypeScript types (*.types.ts)
```

---

## Páginas

- `/` — Home (Hero)
- `/about` — Sobre mim
- `/projects` — Projetos (GitHub API + filtros)
- `/skills` — Habilidades
- `/blog` — Lista de posts (Astro Content Collections)
- `/blog/[slug]` — Post individual
- `/contact` — Formulário de contato

---

## Conceitos sendo praticados

### React
JSX · Props vs State · Conditional Rendering · Composition · Component Lifecycle ·
Lists & Keys · Refs · Events · useCallback · useMemo · useRef · useReducer · useContext · Custom Hooks

### Web & Plataforma
Web Components (Custom Elements, Shadow DOM) · Acessibilidade (WCAG AA, ARIA) ·
Performance (Core Web Vitals, Lighthouse, Islands Architecture, Streaming) ·
Web Security (CSP, CORS, OWASP) · Module Bundlers (Vite deep dive) ·
Web APIs (IntersectionObserver, Web Storage, Fetch, URLSearchParams) · PWA básica

---

## Comandos principais

```bash
bun dev          # Servidor de desenvolvimento
bun build        # Build de produção
bun preview      # Preview do build
bun test         # Vitest (unit + component)
bun test:e2e     # Playwright (E2E)
bunx astro add   # Adicionar integração Astro
bunx shadcn add  # Adicionar componente Shadcn
```

---

## Comportamento esperado de Claude

### Modo de ajuda geral
- Responder perguntas sobre o projeto, arquitetura, stack e decisões técnicas
- Sugerir melhorias, identificar problemas, revisar código quando solicitado
- Gerar código quando explicitamente pedido (sem restrições em modo normal)

### Modo de tutoria (quando o contexto for de aprendizado)
- Seguir rigorosamente as diretrizes de `docs/TUTOR.md`
- Usar o sistema de dicas progressivas
- Não dar respostas prontas — guiar o raciocínio do aluno

> **Como identificar o modo:** Se Davy dizer "me ajuda a aprender", "como funciona X", "não entendo Y", "me explica" → modo tutoria. Se disser "gera o código", "implementa", "faz X" → modo assistente normal.

---

## Convenções de código

- Componentes Astro: `PascalCase.astro`
- Componentes React: `PascalCase.tsx` em `src/components/react/`
- Hooks: `use-nome-do-hook.ts` em `src/hooks/`
- Stores: `nome.store.ts` em `src/stores/`
- Types: `nome.types.ts` em `src/types/`
- Schemas Zod: `nome.schema.ts` em `src/lib/validations/`
- Queries: `nome.queries.ts` em `src/lib/queries/`
- CSS: TailwindCSS 4 (utility-first); CSS Modules para casos específicos
