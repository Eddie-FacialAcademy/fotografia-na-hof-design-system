# Changelog · Fotografia na HOF Design System

Todas as mudanças relevantes deste design system são registradas aqui.
O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) e o
versionamento segue [SemVer](https://semver.org/lang/pt-BR/):

- **MAJOR**: muda ou remove um token/API público (quebra compatibilidade).
- **MINOR**: adiciona de forma retrocompatível (novo componente/token/variante).
- **PATCH**: correções que não mudam a API (bug, contraste, ajuste fino).

---

## [Não lançado]

_Nada pendente no momento._

## [1.1.0] · 2026-09-29
### Alterado
- **Nomes de cor organizados em duas camadas.** Cores da marca (`--brand-*`) levam o nome real da cor nesta marca; tokens de uso têm nomes neutros e iguais em todos os DS do grupo (`--primary`, `--accent`, `--highlight`, `--support`, `--glow`), para o código continuar portável entre marcas. Valores não mudaram: comparação de cor computada em todos os elementos do showcase, antes e depois, nos dois temas, deu zero diferença.
- Tokens de uso: `--roxo-bright` → `--primary-bright`, `--lilas-soft` → `--accent-soft`, `--gold-deep` → `--highlight-deep`, `--gold-line` → `--highlight-line`, `--rose-line` → `--support-line`, `--gold-ink` → `--highlight-ink`, `--rose-ink` → `--support-ink`, `--azul-luz` → `--secondary-bright`, `--roxo2` → `--primary`, `--lilas` → `--accent`, `--peach` → `--glow`, `--roxo` → `--primary-deep`, `--gold` → `--highlight`, `--rose` → `--support`, `--azul` → `--secondary`.
- Cores da marca: `--brand-amarelo` → `--brand-dourado`, `--brand-vermelho` → `--brand-rosa`, `--brand-amarelado` → `--brand-pessego`, `--brand-roxo` → `--brand-violeta`, `--brand-lilas` → `--brand-lavanda`, `--brand-branco` → `--brand-gelo`.
- JSON de tokens: chaves renomeadas igual aos tokens (camelCase) e mapa de/para em `$deprecated`.
- Variantes de botão `fnh-gold` e `fnh-gold-o` viraram `fnh-highlight` e `fnh-highlight-o`; os nomes antigos continuam valendo no CSS de colar no site.
- Nomes exibidos no showcase ligados à cor real: acentos compartilhados do grupo como **Dourado claro**, **Rosa claro** e **Pêssego** (antes "Amarelo claro", "Vermelho claro" e "Amarelado", com a mesma cor chamada de formas diferentes entre DS); rótulos de gradiente gerados a partir das cores de cada gradiente.
- Documentação técnica: seção 13 virou "Relação com o molde", só com valores deste DS (a tabela anterior repetia valores de outra marca e desatualizava).
### Descontinuado
- Os nomes antigos listados acima continuam funcionando como apelidos no CSS de colar no site e saem na 2.0. Use os nomes novos em código novo.

## [1.0.3] · 2026-09-29
### Corrigido
- CTA do tema escuro: degradê `#8B33E3 → #2E5FA8` vira `#8C35E3 → #3267B6`; o fim passava 2.7:1 contra o modal e agora fica ≥3:1; texto branco 5.6:1.
- Dia selecionado do calendário usa `--cta-solid` e `--cta-ink` (o roxo base ficava abaixo de 3:1 contra o fundo do calendário no tema escuro).
- Prévia de tema (cartões escuro e claro) mostra o CTA real de cada tema.
- `--brand-azul` presente também no showcase e no JSON (antes só no CSS).
- Tabela de acessibilidade do showcase com valores medidos nos dois temas (antes repetia números do molde que não eram desta paleta) e linha nova "CTA contra o fundo" (nível 2).
### Alterado
- Seletor de design systems inclui a Facial Premium, na ordem única usada em todos os DS.
- Versão alinhada em todos os arquivos: tokens, CSS, copy-deck e documentação estavam presos em uma versão anterior ao CHANGELOG.
- Documentação sem travessão e sem "&", com valores de cor, contraste e classe conferidos contra o CSS e o JSON; referências a versões e arquivos inexistentes corrigidas.

## [1.0.2] · 2026-08-28
### Corrigido
- Cores de marca branco e preto alinhadas ao arquivo do logo: gelo `#F3F3F3`
  e preto `#101010` no lugar dos absolutos `#FFFFFF`/`#000000` (a marca não
  usa branco nem preto puros).

## [1.0.1] · 2026-08-28
### Alterado
- Menu "Design systems" agora inclui HArmonyCa Performance e Expert em
  Lábios 2026.
### Corrigido
- Tabela de Color Styles: coluna Escuro de "text/Secundário" alinhada ao
  token `--mut` real.
- Galeria de gradientes retintada por completo na paleta da marca (sobras do
  molde removidas; a aurora agora termina no azul `#2E5FA8`).

## [1.0.0] · 2026-08-28

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
