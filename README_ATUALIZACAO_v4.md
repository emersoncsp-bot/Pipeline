# Atualização v4 — Fluxo de Liberação

## Arquivo alterado
- `src/App.jsx`

## Como aplicar
1. Substituir `src/App.jsx` pelo arquivo deste pacote (mantém `package.json` da v2/v3, já com `xlsx`)
2. `npm install` (se necessário)
3. `npm run dev` / `npm run build`

## Alterações implementadas (conforme documento "projeto-bloqueio.docx")

1. **Agrupamento removido**: os botões G1/G2 foram retirados. Todas as colunas (Pedido, Item, Material, Descrição, Última Ordem, Qualidade QTS, Depósito SAP, Motivo Bloqueio) ficam sempre visíveis na tabela.

2. **Histórico em visualização lateral (cards horizontais)**: cada etapa do histórico agora aparece como um cartão lado a lado, com rolagem horizontal própria. Dentro de cada cartão:
   - 1ª linha: número + nome da etapa (em negrito)
   - 2ª linha: **Definição** (texto/recurso informado) — sempre em **azul** (posição invertida em relação ao usuário, conforme solicitado)
   - 3ª linha: usuário responsável
   - 4ª linha: data/hora
   A coluna Histórico foi alargada (min. 320px) para acomodar essa visualização.

3. **Checkbox de seleção fixado**: a coluna de checkbox (seleção de lote) agora é "sticky" à esquerda, permanecendo visível durante a rolagem horizontal da tabela.

4. **Indicadores do Dashboard alinhados**: os cartões de KPI agora têm altura mínima padronizada e os títulos/valores alinhados (topo/baixo) para manter o alinhamento horizontal entre os cartões.

5. **"Tempo médio por etapa" e "Bloqueio por Depósito" lado a lado**: ambos os indicadores dividem 50% do espaço horizontal (grid 1fr/1fr) na parte inferior do Dashboard.

6. **Departamentos renomeados**:
   - "Controle da Qualidade [Área Técnica]" → **"Controle da Qualidade"**
   - "Controle da Qualidade [Liberação Intermediária]" → **"Liberação de produtos"**

7. **Coluna "Descrição" com largura dobrada** (min-width 220px, o dobro das colunas padrão).

8. **Termos da Pipeline atualizados**:
   - "Análise de Recurso" → **"Avaliar Recurso"**
   - "Definição de Ordem" → **"Criar Ordem"**
   - "Instrução" → **"Atualizar IC"**
   - "Lib. Vínculo" → **"Desbloqueio"**
   - "Pend. Execução" → **"Execução"**

9. **Coluna "Definição"**: tanto a coluna "Recursos Necessários" (Etapa 1) quanto "Tratativa do Lote" (demais etapas) passam a se chamar **"Definição"**.

10. **Novas colunas ao final (lado direito) da tabela**: "Motivo Bloqueio Texto", "Razão Bloq." e "Descrição Motivo" (nova coluna importável — cabeçalho aceito: "Descrição Motivo" / "Descricao-Motivo"), seguidas, por último, pela coluna **"Definição"**.

## Observações
- A página de Histórico também usa o novo layout de cards horizontais na coluna "Histórico".
- A tabela ficou mais larga (min-width 1400px) devido às novas colunas — a rolagem horizontal é nativa do container, com o checkbox fixo à esquerda.
