# Changelog — Fotografia na HOF Design System

Todas as mudanças relevantes deste design system são registradas aqui.
O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) e o
versionamento segue [SemVer](https://semver.org/lang/pt-BR/):

- **MAJOR** — muda ou remove um token/API público (quebra compatibilidade).
- **MINOR** — adiciona de forma retrocompatível (novo componente/token/variante).
- **PATCH** — correções que não mudam a API (bug, contraste, ajuste fino).

---

## [Não lançado]

_Nada pendente no momento._

## [1.0.0] — 2026-08-28

Primeira versão da Fotografia na HOF, derivada do molde Facial Academy.
Paleta extraída do gradiente do logo (azul profundo `#204A8A`, violeta
`#7A1AD6`, lavanda `#C286FF`) com derivadas medidas em WCAG AA nos dois
temas. Reúne fundações, camada de produto e camada de maturidade/processo.

### Marca
- Logo horizontal, versão monocromática e ícone (diafragma) embutidos como
  `symbol` SVG; texto segue o tema por `currentColor`, diafragma mantém o
  gradiente oficial da marca.
- Favicon com o diafragma em badge azul `#204A8A`, SVG data-URI no `head`.

### Fundações
- Arquitetura de tokens em 3 camadas (`primitive → semantic/intent → component`).
- Tema escuro com fundos violeta-azulados (`#0A0A14` a `#221E40`) e tema claro
  off-white; paridade total e contraste **WCAG AA** medido em todos os pares.
- CTA theme-aware com o gradiente da marca: escuro `#8B33E3 → #2E5FA8`, claro
  `#7A1AD6 → #204A8A`; acessibilidade em 2 níveis (texto 4.5:1, botão vs
  fundo 3:1).
- Anel de foco em duas camadas (`--focus-ring` escuro `#C286FF`, claro
  `#7A1AD6`) e guard de alto contraste com `outline` `!important`.
- Tokens `--azul` e `--azul-luz` para a segunda cor de marca.
- Numerais com `tabular-nums` global; prefixo de classe `fnh-`; tema em
  `localStorage` na chave `fnh-theme`.

### Produto
- Forms com validação e matriz de estados; feedback (alertas, notificação,
  esqueleto, estado vazio); overlays (janela modal, dica, balão); estrutura
  (abas, acordeão, avatar, trilha de navegação, paginação, cartões); avançados
  (tabela de dados, paleta de comandos, seletor de data, app shell).
- Copy de demonstração no domínio da marca: fotografia clínica, registro de
  antes e depois, casos e acervo (ver `glossario-marca.md`).

### Navegação do showcase
- Menu "Design systems" (seletor entre as marcas do ecossistema) e scrollspy
  por categorias, herdados do molde.
