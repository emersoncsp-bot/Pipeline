# Atualização v9 — Ajustes conforme "update_V8.docx"

## Arquivos alterados
- `src/App.jsx`
- `index.html` (título da aba do navegador)
- `public/favicon.svg` (ícone da aba, alinhado à nova marca)

## Ajustes implementados

### 1. Tabela da Pipeline — ajustes visuais
- Fonte da tabela ligeiramente reduzida (cabeçalhos e células).
- Cor da barra de títulos da tabela escurecida (cinza mais perceptível).
- O cabeçalho "Definição" e o destaque de linha selecionada estavam com
  aparência "lavada"/transparente — ambos agora usam cores sólidas e opacas.

### 2. Colunas "Pedido" e "Item" voltam a ser separadas
- Revertido o agrupamento automático em "Pedido/Item" (Pipeline, pré-visualização
  de importação e Histórico). As duas colunas voltam a aparecer separadamente,
  como na v7.

### 3. Legenda "Faturamento" agora é interativa
- Clicar na legenda "Faturamento" (no topo da tabela da Pipeline) filtra a
  tabela, exibindo somente os lotes cujo Pedido/Item está cadastrado em
  Faturamento (linhas com destaque vermelho claro). Clicar novamente remove
  o filtro.

### 4. Campo de pesquisa da Pipeline
- O campo único "Pedido / Item" foi separado em dois campos: **Pedido**
  (primeiro) e **Item** (em seguida), cada um com seus próprios critérios
  de busca (aceitam múltiplos valores).

### 5. Seleção de múltiplos lotes com Shift
- Os checkboxes da tabela agora suportam seleção em intervalo: ao marcar um
  checkbox e, em seguida, marcar outro mantendo **Shift** pressionado, todos
  os lotes entre o primeiro e o segundo clique são selecionados.

### 6. Campo "Definição" obrigatório para avançar
- Antes de enviar lotes para a próxima etapa (ou concluir na Etapa 8), o
  sistema verifica se o campo "Definição" foi preenchido para todos os lotes
  selecionados. Caso falte algum, uma mensagem de alerta é exibida e o envio
  é bloqueado até o preenchimento.

### 7. Histórico em formato de 4 linhas
- Cada registro do histórico agora é exibido em bloco de 4 linhas:
  - Linha 1: Etapa, em negrito
  - Linha 2: Definição da etapa, em azul
  - Linha 3: Usuário, em cinza médio
  - Linha 4: Data/hora, em cinza claro
  Múltiplos registros continuam dispostos lado a lado, separados por uma
  linha vertical divisória.

### 8. Rebranding — "PipeLine"
- Título da aba do navegador alterado para **"PipeLine"**.
- Ícone da aba (favicon) atualizado para o novo símbolo (nós conectados em
  gradiente azul).
- Barra lateral flutuante: o ícone/título "Fluxo de Liberação" foi substituído
  pela nova marca **PipeLine** (ícone + wordmark "Pipe"+"Line" em destaque),
  com "Fluxo de Liberação" como subtítulo.
- Página de login: mesma atualização de marca (ícone PipeLine, wordmark e
  subtítulo "Fluxo de Liberação · Gestão de Pipeline").

### 9. Faturamento — Descrição automática
- Na aba Configurações → Faturamento, ao informar Pedido e Item, o campo
  "Descrição" é preenchido automaticamente com base na descrição do produto
  já presente nos tubos correspondentes na Pipeline (caso exista). O usuário
  ainda pode editar manualmente se necessário.

### 10. Dashboard — nova tabela "Pedidos / Itens"
- Nova tabela abaixo do gráfico "Motivos de Bloqueio", com as colunas:
  Pedido, Item, Descrição, Tubos e Motivos de Bloqueio.
- A tabela acompanha os filtros existentes: ao clicar em uma etapa do "Funil
  do Processo", exibe apenas os pedidos/itens daquela etapa.
- O gráfico "Motivos de Bloqueio" também se tornou clicável: ao selecionar um
  motivo, a tabela "Pedidos / Itens" é filtrada para mostrar somente os
  pedidos/itens com aquele motivo de bloqueio (combinável com o filtro de
  etapa). Um chip de filtro permite limpar a seleção.
