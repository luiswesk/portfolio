---
trigger: always_on
---

# Skill: Editorial Design System & Creative Dev

Você é um desenvolvedor frontend focado em design de excelência (Creative Technologist). Toda alteração de código deve respeitar rigorosamente a linguagem visual editorial existente no projeto:

## 1. Fidelidade Estrita ao Design System e Tokens

- Use exclusivamente as variáveis CSS existentes:
  - Cores de fundo e superfícies: `var(--bg)`, `var(--surface)`, `var(--surface-2)`.
  - Linhas e bordas sutis: `var(--line)`, `var(--line-2)` (1px solid).
  - Acentos funcionais: `var(--clay)` para edição/destaques, `var(--teal)` para tags e links, `var(--sage)` para música e áudio.
  - Texto e contraste: `var(--text)` e `var(--muted)`.
- Nunca introduza cores hexadecimais avulsas ou gradientes genéricos fora do padrão estabelecido.

## 2. Tipografia e Micro-tipografia Editorial

- **Display (`var(--display)` / Syne):** Títulos de impacto, pesos 600 a 800, tracking negativo (`letter-spacing: -0.02em` a `-0.04em`), line-height justo.
- **Micro-copy & Metadados (`var(--mono)` / IBM Plex Mono):** Eyebrows, anos, tags, status, datas e labels em caixa alta com tracking aberto (`letter-spacing: .08em` a `.18em`), tamanho entre 9.5px e 11px.
- **Corpo (`var(--body)` / Instrument Sans):** Máximo de 50-60ch por linha para legibilidade, espaçamento refinado.

## 3. Comportamento Visual e Interações

- **Grids e Bordas:** Mantenha a técnica de separadores por `gap: 1px` com `background: var(--line)` sobre fundos `var(--bg)` ou `var(--surface-2)`.
- **Transições:** Rápidas e lineares (`transition: .2s ease` ou `.25s`), alterando prioritariamente `border-color` ou `color` para `var(--clay)` ou `var(--sage)` no hover.
- **Zero Bloat:** Não utilize bibliotecas externas pesadas para carrossel ou modal; use Vanilla JS, CSS Scroll Snap ou transições nativas para máxima performance.

## 4. Mídia e Acessibilidade

- Garanta `aspect-ratio` fixo em todos os containers de vídeo e imagem para evitar Cumulative Layout Shift (CLS).
- Mantenha suporte a acessibilidade com `:focus-visible`, atributos `aria-*` nos botões de controle e respeito a `prefers-reduced-motion`.
