# Atualização v6 — Fluxo de Liberação (Ajustes conforme "Ajustes-v5.docx")

## Arquivo alterado
- `src/App.jsx`

(`package.json` e `src/index.css` permanecem como na v5)

## Ajustes implementados

1. **Aba lateral de menu sob hover**: a barra lateral agora fica oculta por
   padrão e aparece ao posicionar o cursor próximo à borda esquerda da tela
   (zona de 14px). Ao retirar o cursor, ela se recolhe automaticamente
   (deslizamento com efeito "spring"). O conteúdo principal ocupa toda a
   largura da tela.

2. **Usuário logado no canto superior direito**: avatar, nome, departamento e
   botão de logout foram movidos da barra lateral para a barra superior
   (top-right), já que a lateral agora é ocultável.

3. **Fonte dos títulos**: títulos das abas (Dashboard, Pipeline, Histórico,
   Configurações), o logotipo "Fluxo de Liberação" na lateral, os títulos de
   cada etapa do Pipeline (Importar Tubos Bloqueados, Definição do Recurso,
   Criação de Ordem, Instrução da Qualidade, Liberação para Vínculo, Vínculo
   dos Lotes, Ativação de Flag, Pendente Execução) e os números grandes dos
   KPIs do Dashboard agora usam uma família "SF Pro Rounded" (com fallback
   para SF Pro Display), dando um tom mais "display" e arredondado aos
   títulos.

4. **Dashboard revisado (estilo relatório executivo)**: cabeçalho "Visão
   Geral" com data/hora de atualização; cartões de KPI redesenhados com
   ícone em selo colorido (tinted badge) no canto superior direito de cada
   cartão e número grande em destaque — visual mais próximo de relatórios
   estilo Apple para apresentação à Diretoria.

5. **Cassete e Data Bloqueio como colunas**: removidos do detalhe expandido
   de IPPN e adicionados como colunas próprias da tabela ("Data Bloqueio" e
   "Nº Cassete", logo após "IPPNs"). O detalhe expandido do lote agora mostra
   apenas o IPPN agrupado.

6. **Coluna "Histórico" ao final**: reposicionada como última coluna (à
   direita) da tabela principal e da página de Histórico.

7. **Histórico em formato "clean"**: os registros de cada etapa agora são
   exibidos em linha, separados por uma barra vertical "|" — sem cards.
   Em cada registro: "Etapa: Definição (em azul) — Usuário (data/hora)".

## Observação
Nenhuma lógica de negócio foi alterada (importação, agrupamento por lote,
busca, permissões, conclusão para o Histórico, etc.).
