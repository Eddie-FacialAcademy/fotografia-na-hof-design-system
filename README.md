# Fotografia na HOF — Design System

Design system da **Fotografia na HOF** (fotografia clínica para profissionais de HOF, marca do ecossistema Facial Academy). Cor predominante **violeta `#7A1AD6`**, com lavanda `#C286FF` e azul profundo `#204A8A` extraídos do gradiente do logo; tipografia **Silka** (embutida em woff2, headers em **Medium 500**).

Desenvolvido por **Edegar Junior**.

## Entregas

- **index.html** — design system reutilizável (showcase navegável): paleta (institucional + derivada), temas **dark/light**, tipografia (Silka), **gradientes**, **ícones** (Phosphor Thin, copiar SVG), **logos** (copiar/baixar SVG) e sistema de **botões** (variantes/tamanhos/estados); os botões fill/solid usam o token `--cta` (CTA escuro clareado para passar contraste de componente). Click-to-copy em cores, valores e código; download PNG dos gradientes.
  - 🌐 **Online (para compartilhar):** https://eddie-facialacademy.github.io/fotografia-na-hof-design-system/ — GitHub Pages (repo público `fotografia-na-hof-design-system`).

## Design System portátil (`design-system/`)

Pacote para aplicar a marca em **qualquer projeto/ferramenta** (web, React, Framer, agentes de IA).

- **silka.css** — fonte **Silka** (pesos 300–700) embutida em woff2/base64, self-contained; linke antes do CSS principal.
- **fotografia-na-hof-design-system.css** — drop-in (tokens dark/light, inclui CTA theme-aware via `--cta` (dark `#8B33E3`, light `#7A1AD6`) + reset + foco + motion + tipografia + botões + chips/badges/status).
- **fotografia-na-hof-design-tokens.json** — tokens legíveis por máquina (Style Dictionary, Framer, IA).
- **Button.tsx** — Code Component Framer/React com Property Controls.
- **DESIGN-SYSTEM.md** — spec completa, 3 formas de aplicar e **prompt pronto para IA**.
- **THEME.md** — como o claro/escuro é configurado e ativado pelo tema do sistema do visitante (web + Framer).

## Notas técnicas

- **Cores:** extraídas do **gradiente do logo** (violeta `#7A1AD6`, lavanda `#C286FF`, azul profundo `#204A8A`) mais o apoio herdado da família (amarelo claro `#FFE4A4`, vermelho claro `#FFB1BD`, amarelado `#FFCA9B`) e branco/preto de marca. Derivadas medidas em WCAG AA nos dois temas.
- **Tipografia:** Silka (institucional), embutida em base64/woff2; Poppins como fallback (quando a Silka não estiver disponível), depois system-ui. **Headers em Medium (500)**; eyebrow 600; numeral 700; body 300.
- **Ícones:** biblioteca **Phosphor**, peso **Thin** (stroke 1pt na grade 24), `currentColor`.
- **Tema:** dark por padrão; light via `data-theme="light"`; sem atributo segue `prefers-color-scheme`. Toggle persiste em `fnh-theme`.
- **Acessibilidade:** contraste em 2 níveis — (1) texto ≥4.5:1; (2) componente/botão vs fundo ≥3:1 (WCAG 1.4.11). O CTA do tema escuro foi clareado para `#8B33E3` para passar o nível 2.

## Publicação

Repo público `fotografia-na-hof-design-system` (conta `Eddie-FacialAcademy`), branch `main`, `index.html` na raiz, GitHub Pages. `.git` fora do OneDrive (`AppData\Local\gitdirs\`); line-endings LF (`.gitattributes`). Deploy: editar → `git add/commit/push` (credencial no Cofre do Windows, sem token). Ver `HANDOFF.md`.

## CHANGELOG

- **1.0.0** (2026-08-28) — primeira versão da marca, derivada do molde Facial Academy com paleta do logo (violeta, lavanda e azul). Histórico completo em `design-system/CHANGELOG.md`.
