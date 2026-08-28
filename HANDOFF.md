# Handoff — Fotografia na HOF Design System (Versão 1.0.0 · estado em 2026-08-28)

Desenvolvido por **Edegar Junior**. Ponto de retomada; atualizar conforme avançar.

## ✅ Concluído

### Design system online (GitHub Pages)
- **URL pública:** https://eddie-facialacademy.github.io/fotografia-na-hof-design-system/
- Repo público `fotografia-na-hof-design-system` (conta `Eddie-FacialAcademy`), branch `main`, `index.html` na raiz.
- `index.html`: showcase self-contained, dark/light automático + toggle (chave `fnh-theme`), click-to-copy, **copiar/baixar SVG** de logos, **download PNG** dos gradientes, menu "Design systems" entre as marcas e favicon do diafragma.

### Marca
- Derivada do molde **Facial Academy** (mesma arquitetura, seções e JS).
- Paleta extraída do **gradiente do logo**: violeta `#7A1AD6` (predominante), lavanda `#C286FF` (accent), azul profundo `#204A8A` (segunda cor). Derivadas: violeta profundo `#341060`, violeta brilhante `#8B33E3`, azul médio `#2E5FA8`, azul luz `#7FA9EA`. Apoio herdado da família: amarelo `#FFE4A4`, vermelho claro `#FFB1BD`, amarelado `#FFCA9B`.
- **Logo:** wordmark "fotografia na hof"; o "o" de hof é um diafragma com gradiente fixo azul→violeta→lavanda. Composições: horizontal, monocromática (currentColor) e ícone. **Não existe versão vertical nem tipografia sem o diafragma.** Texto segue o tema por `currentColor` com as cores do arquivo: gelo `#F3F3F3` no escuro, preto `#101010` no claro. Não recolorir.
- **Domínio:** fotografia clínica (registro de antes e depois, luz, enquadramento, padronização, consentimento). Glossário em `design-system/glossario-marca.md`.

### Acessibilidade (medida, não estimada)
- 44 pares de contraste da paleta medidos antes do build: todos AA (texto ≥4.5:1, componente ≥3:1).
- CTA por tema: escuro gradiente `#8B33E3 → #2E5FA8` (branco 5.7:1 e 6.3:1; botão vs fundo 3.4:1 e 3.1:1), claro `#7A1AD6 → #204A8A`.
- Anel de foco em 2 camadas: `--focus-ring` escuro `#C286FF`, claro `#7A1AD6`; guard forced-colors com `outline !important`.

### Pacote portátil (`design-system/`)
- `silka.css` · `fotografia-na-hof-design-system.css` (prefixo `fnh-`) · `fotografia-na-hof-design-tokens.json` · `Button.tsx` · `THEME.md` · `DESIGN-SYSTEM.md` · `IMPLEMENTACAO.md` · `CHANGELOG.md` · `CONTRIBUTING.md` · `copy-deck.fotografia-na-hof.json` · `glossario-marca.md` · `voz-e-tom.md`.

## 📌 Próximos passos possíveis
- Landing/página da marca no Framer (subir Color Styles e Text Styles a partir dos tokens).
- Fotografia real da marca (o DS é image-light por padrão).
- Opcionais do roadmap (i18n/RTL, imagery, densidade global) sob demanda.

## Como publicar mudanças
Editar → `git add/commit/push` na `main` (credencial no Cofre do Windows; `.git` em `AppData\Local\gitdirs\fotografia-na-hof-design-system`; line-endings LF via `.gitattributes`). O GitHub Pages atualiza sozinho em ~1 minuto.
