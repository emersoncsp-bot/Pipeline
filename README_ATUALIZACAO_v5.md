# Atualização v5 — Fluxo de Liberação (Design iOS/HIG · Desktop-first)

## Arquivos alterados
- `src/App.jsx`
- `src/index.css`
- `package.json` (nova dependência: `lucide-react`)

## Como aplicar
1. Substituir os 3 arquivos acima no projeto
2. `npm install` (necessário — adiciona `lucide-react`)
3. `npm run dev` / `npm run build`

## O que mudou — Design System (Apple HIG, adaptado para desktop)

### Layout (NavigationSplitView)
- **Barra lateral fixa** (esquerda, 232px) com efeito de vidro fosco (blur + saturate),
  substitui o antigo menu hambúrguer. Contém: logo, navegação (Dashboard, Pipeline,
  Histórico, Configurações), e cartão do usuário com botão de logout no rodapé.
- **Barra superior translúcida** (glass) com o título "Large Title" da página ativa
  e subtítulo descritivo — substitui o cabeçalho navy anterior.
- Conteúdo usa a largura total disponível (sem a faixa cinza lateral de antes),
  priorizando telas grandes; tabelas mantêm rolagem horizontal própria.

### Cores e materiais
- Paleta neutra clara (`#F2F2F4` fundo / `#FFFFFF` cartões), acento **iOS Blue
  (#0A84FF)** em toda a UI de navegação, botões primários, foco de campos e
  destaques (coluna "Definição", busca, badges de seleção).
- Cabeçalhos de tabela mais leves (cinza claro com texto uppercase), em vez do
  navy escuro anterior — mais alinhado ao estilo "grouped table" da Apple.
- Cantos arredondados (12–18px) em cartões, modais, tabelas e botões.

### Interações
- **Feedback "spring"** ao toque: todos os botões, itens de navegação, toggles e
  cartões clicáveis usam `transform: scale(0.96)` com `cubic-bezier` tipo mola.
- Cartões do Dashboard (KPIs e etapas) têm efeito "hover-lift" (leve elevação +
  sombra ao passar o mouse).
- Modal com fundo desfocado (`backdrop-filter: blur`).
- Toast de confirmação com vidro fosco e ícone de check.

### Ícones (lucide-react)
- Substituídos os emojis por ícones consistentes (estilo SF Symbols):
  navegação, busca, importação (upload), avançar/retornar (setas), concluir
  (check), permissões (escudo), usuários, editar/excluir, estados vazios
  (inbox/layers), etc.

### Funcionalidade
- Nenhuma lógica de negócio foi alterada: importação (CSV/XLS/XLSX), agrupamento
  por lote, busca multi-token, Histórico com cards horizontais, permissões por
  etapa/usuário, KPIs e tempo médio (em dias) continuam exatamente como na v4.
