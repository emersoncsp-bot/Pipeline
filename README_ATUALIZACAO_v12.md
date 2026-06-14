# Atualização v12 — Ajustes na tabela da aba Pipeline

## Arquivo alterado
- `src/App.jsx`

## Ajustes implementados

### 1. Largura da tabela ajustável
- O painel da tabela (na Pipeline) agora pode ser redimensionado pelo
  usuário: arraste a alça no canto inferior direito do painel para ajustar
  sua largura/altura conforme necessário.

### 2. Largura de cada bloco do Histórico ajustável
- Cada registro do Histórico (bloco de 4 linhas: Etapa / Definição / Usuário
  / Data) agora pode ser redimensionado individualmente — arraste a alça no
  canto inferior direito do bloco para alargá-lo quando o texto da
  "Definição" for longo (ex.: "Inspeção VD, Serra, Inspeção EMI,
  Inspeção...").

### 3. Texto completo ao passar o mouse
- Quando qualquer linha do bloco de Histórico estiver truncada (com "..."),
  basta posicionar o mouse sobre o texto para ver o conteúdo completo (dica
  nativa do navegador).

### 4. Botão "Tela cheia"
- Novo botão "Tela cheia" no topo da tabela de cada etapa da Pipeline. Ao
  ativá-lo, a tabela (com cabeçalho, contadores, ações de avançar/retornar/
  concluir e mensagens de validação) ocupa toda a janela, facilitando a
  visualização de tabelas largas. Use o botão "Sair" ou a tecla **Esc** para
  retornar ao layout normal.
