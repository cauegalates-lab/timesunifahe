PAINEL DE TIMES — APP SCRIPT COMO FONTE DE VERDADE

ARQUIVOS
- index.html: interface do painel. Não mantém nomes, membros ou metas fixos dos times.
- assets/: logos dos times e identidade UNIFAHE.
- app-script-completo.gs: código completo do Google Apps Script. A parte de Times foi atualizada sem alterar os demais módulos.

COMO FUNCIONA O PAINEL DE TIMES
1. O painel abre automaticamente no mês atual no fuso America/Sao_Paulo.
2. O seletor de mês permite consultar normalmente janeiro a dezembro do ano corrente; o mês e o ano selecionados são enviados ao Apps Script.
3. Ao virar o ano, uma nova abertura da página assume automaticamente o novo ano corrente.
4. As semanas são calculadas pelo calendário real do mês selecionado, considerando somente segunda a sexta.
5. Sábado e domingo não entram no resultado semanal nem no resultado mensal.
6. O Apps Script lê as vendas da aba Vendas e soma o faturamento de cada vendedor.
7. O resultado de cada time é calculado no Apps Script a partir dos membros configurados.
8. O index.html recebe do Apps Script: nome do time, logo, membros, meta, realizado e períodos das semanas.

EXEMPLO — SETEMBRO/2026
1ª semana: 01 a 04
2ª semana: 07 a 11
3ª semana: 14 a 18
4ª semana: 21 a 25
5ª semana: 28 a 30

COMO ALTERAR TIMES, MEMBROS E METAS
1. Abra app-script-completo.gs.
2. Localize CONFIG_TIMES.
3. Cada bloco possui:
   - id: identificador interno do time;
   - nome: nome exibido no painel;
   - logo: caminho da imagem dentro de assets/;
   - membros: vendedores que pertencem ao time;
   - metas: semana1, semana2, semana3, semana4 e semana5.
4. Para usar uma meta mensal específica, adicione `mes: VALOR` dentro de `metas`.
5. Se `mes` não existir, a meta mensal será a soma das cinco metas semanais.
6. É possível adicionar ou remover times no CONFIG_TIMES; o index monta os cards dinamicamente.

DEPOIS DE ALTERAR O APP SCRIPT
Implantar > Gerenciar implantações > Editar > Nova versão > Implantar.
A URL publicada pode continuar a mesma.

ARQUIVOS PARA ATUALIZAR
- Google Apps Script: app-script-completo.gs
- GitHub/site: index.html e os assets necessários para logos novas

COLUNAS LIDAS DA ABA VENDAS
B: dia
C: mês
D: ano
E: vendedor
T: valor total da venda
