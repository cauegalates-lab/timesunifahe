PAINEL DE EQUIPES — TIMES INDEPENDENTES POR SEMANA

ARQUIVOS
- index.html: mostra somente os dados recebidos do Apps Script.
- assets/: logos das equipes e símbolo da UNIFAHE.
- app-script-completo.gs: código completo do Google Apps Script, incluindo R2, equipes, crescimento e meta de 1 milhão.

COMO FUNCIONA AGORA
1. O Apps Script lê as vendas da aba Vendas.
2. Identifica a semana de cada venda pela data.
3. Consulta a formação da baia cadastrada para aquela semana.
4. Soma o valor individual atribuído a cada membro.
5. Calcula o realizado de cada baia no próprio Apps Script.
6. Envia ao index os membros, valores individuais por baia, metas, realizados e total geral das baias.
7. O index apenas exibe os dados recebidos e não soma o realizado das baias.

COMO ALTERAR OS MEMBROS DAS BAIAS
1. Abra app-script-completo.gs.
2. Localize CONFIG_MEMBROS_EQUIPES.
3. Cada baia possui cinco listas independentes:
   - semana1
   - semana2
   - semana3
   - semana4
   - semana5
4. Edite os nomes dentro da semana desejada.
5. Cada semana pode ter uma composição totalmente diferente.

COMO FUNCIONA O BOTÃO MÊS
- As vendas da Semana 1 contam para as baias configuradas em semana1.
- As vendas da Semana 2 contam para as baias configuradas em semana2.
- O mesmo acontece nas semanas 3, 4 e 5.
- Se uma pessoa mudar de baia, o valor permanece atribuído à baia em que ela estava na semana da venda.
- O total mensal de cada baia já é enviado pronto pelo Apps Script.

COMO ALTERAR AS METAS
1. Localize CONFIG_METAS_EQUIPES.
2. Altere semana1, semana2, semana3, semana4 e semana5.
3. No modo MÊS, a meta é a soma automática das cinco semanas.
4. Para usar uma meta mensal fixa, adicione mes: VALOR dentro da equipe.

DEPOIS DE ALTERAR O APP SCRIPT
Implantar > Gerenciar implantações > Editar > Nova versão > Implantar.
A URL atual pode continuar a mesma.

ARQUIVOS PARA ATUALIZAR
- No Google Apps Script: substitua o código pelo conteúdo de app-script-completo.gs e faça uma nova implantação.
- No GitHub: substitua o index.html.

COLUNAS LIDAS DA ABA VENDAS
B: dia
C: mês
D: ano
E: vendedor
T: valor total da venda
