# Atualização v10 — Ajustes conforme "update_V9.docx"

## Arquivo alterado
- `src/App.jsx`

## Ajustes implementados

### 1. Tipografia e barra superior
- Fonte da tabela da Pipeline reduzida para 10px (cabeçalhos e células).
- Barra superior (TopBar) reduzida: menos altura/padding, título da página
  ("Dashboard", "Pipeline", "Histórico", "Configurações") com fonte menor —
  aplicado a todas as abas.
- Texto do usuário logado (nome e departamento, canto superior direito)
  reduzido, junto com o avatar e o botão de logout.

### 2. Cabeçalho da tabela mais escuro
- A barra de títulos da tabela ficou ainda mais escura (cinza mais
  perceptível), incluindo o cabeçalho "Definição" (agora em azul opaco).

### 3. Histórico — layout horizontal corrigido
- Os blocos de histórico (Etapa / Definição / Usuário / Data) agora ficam
  sempre lado a lado na mesma linha (não quebram mais para baixo), com
  rolagem horizontal própria quando necessário — conforme o exemplo
  "Como deve ser" do documento.

### 4. Seleção múltipla com Shift+clique — corrigida
- O recurso de selecionar um intervalo de lotes (clique no primeiro,
  Shift+clique no último) foi reimplementado de forma mais robusta e agora
  funciona corretamente.

### 5. Linhas de Faturamento — destaque sólido
- O destaque vermelho claro das linhas de Faturamento (incluindo a célula do
  checkbox, fixa à esquerda) agora usa uma cor sólida/opaca, eliminando o
  efeito de "transparência" na coluna de seleção.

### 6. Dashboard — busca na tabela "Pedidos / Itens"
- Adicionados dois campos de busca ("Pedido" e "Item") acima da tabela
  "Pedidos / Itens", filtrando as linhas exibidas (combináveis com os
  filtros de Etapa e Motivo de Bloqueio já existentes).

### 7. Pipeline — copiar coluna inteira (para Excel)
- Os cabeçalhos das colunas de dados da tabela (Lote, Tubos, IPPNs, Data
  Bloqueio, Nº Cassete, Pedido, Item, Material, Descrição, Última Ordem,
  Qualidade QTS, Depósito SAP, Motivo Bloqueio, Motivo Bloqueio Texto, Razão
  Bloq., Descrição Motivo, Definição) agora são clicáveis: um clique copia
  todos os valores daquela coluna (na ordem exibida) para a área de
  transferência, prontos para colar como uma coluna no Excel. Uma notificação
  confirma a cópia e a quantidade de valores copiados.
