# Atualização v13 — Ajuste de colunas + Faturamento

## Arquivo alterado
- `src/App.jsx`

## Ajustes implementados

### 1. Removido o ajuste de largura do painel da tabela
- A alça de redimensionamento geral do painel da tabela (adicionada na v12)
  foi removida.

### 2. Ajuste de largura por coluna
- Cada coluna de dados da tabela da Pipeline (Lote, Tubos, IPPNs, Data
  Bloqueio, Nº Cassete, Pedido, Item, Material, Descrição, Última Ordem,
  Qualidade QTS, Depósito SAP, Motivo Bloqueio, Motivo Bloqueio Texto, Razão
  Bloq., Descrição Motivo e Definição) agora pode ser redimensionada
  individualmente: arraste a borda direita do cabeçalho da coluna para
  alargar ou estreitar. As células da coluna acompanham a nova largura, com
  reticências (…) quando o texto não couber.
- O clique para copiar a coluna (recurso da v10) continua funcionando
  normalmente ao clicar no restante do cabeçalho.

### 3. Faturamento — Descrição automática também na importação
- Ao importar um arquivo (CSV/XLS/XLSX) na aba Configurações → Faturamento,
  se a planilha não tiver a coluna "Descrição" (ou ela vier vazia para
  algum item), o sistema agora busca automaticamente a descrição do produto
  com base no Pedido/Item correspondente nos tubos da Pipeline — mesmo
  comportamento já existente para o cadastro manual.
