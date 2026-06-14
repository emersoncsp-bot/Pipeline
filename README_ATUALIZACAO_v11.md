# Atualização v11 — Ajustes conforme "update_V10.docx"

## Arquivo alterado
- `src/App.jsx`

## Ajustes implementados

### 1. Barra superior — mais compacta
- Altura/preenchimento reduzidos.
- Título da página ("Dashboard", "Pipeline", "Histórico", "Configurações") e
  o subtítulo ("Etapas do fluxo de liberação", etc.) com fonte menor —
  aplicado a todas as abas.
- Nome/departamento do usuário logado, avatar e botão de logout reduzidos.
- "Visão Geral" (Dashboard) agora usa o mesmo tamanho de fonte do título
  "Dashboard" no topo da página.

### 2. Pipeline — botões mais compactos
- Botões de ação (Retornar / Avançar / Concluir) reduzidos (fonte e
  preenchimento menores) para otimizar espaço.

### 3. Histórico — tipografia ajustada
- Fonte dos blocos de histórico igualada à fonte da tabela (10px).
- Removido o negrito da primeira linha (nome da etapa).

### 4. Seleção de texto nas células — habilitada
- Agora é possível selecionar o texto de uma célula individual (ex.: o
  Pedido de uma linha específica) para copiar manualmente. A restrição de
  seleção foi limitada apenas à coluna de checkbox e aos cabeçalhos
  (necessário para o recurso de copiar coluna via clique).

### 5. Seleção múltipla com Shift — corrigida
- Reimplementada com uma abordagem mais robusta: o estado da tecla Shift é
  monitorado globalmente (keydown/keyup), e o checkbox volta a usar o evento
  padrão de mudança. Marcar um lote e, em seguida, marcar outro com Shift
  pressionado seleciona corretamente todo o intervalo entre eles.

### 6. Notificação de cópia de coluna — centralizada
- O toast de confirmação ("Coluna X copiada...") agora é centralizado em
  relação à largura total da página (antes considerava o espaço de uma
  barra lateral fixa que não existe mais).

### 7. Filtro "Faturamento" — contagem de tubos corrigida
- Ao ativar o filtro pela legenda "Faturamento", tanto o número de lotes
  quanto o número de tubos exibidos no topo da tabela agora refletem somente
  os itens filtrados (antes, o total de tubos permanecia com o valor geral).
