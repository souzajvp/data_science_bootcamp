
![img](https://raw.githubusercontent.com/souzajvp/data_science_bootcamp/main/modulo_01/projeto%201.png)
# Sobre o que é o projeto final realizado neste módulo?

Meu objetivo é avaliar a distribuição dos casos de COVID-19 e compará-los com a distribuição de casos de Síndrome Respiratória Aguda Grave (SRAG), causada por diversos vírus respiratórios. Desta forma, avaliando o comportamento dessas duas manifestações e agentes causadores, com intuito de conscientização para o futuro.
*** 
**Definição de alguns termos**:
1. Síndrome Respiratória Aguda Grave (SRAG) - complicação respiratória grave que pode ser causada por vários vírus respiratórios (Influenza, Parainfluenza, SARS-CoV, etc);
2. COVID-19 - doença causada pelo SARS-CoV-2, pandemia de 2020.;
3. SARS - doença causada pelo SARS-CoV, registrada nos anos de 2002 e 2003. 
<br> **Importante**: O termo SARS em inglês é equivalente à tradução do termo SRAG. Neste notebook, os termos SARS e SRAG serão usados com significados diferentes, apontados nos itens 1 e 2.
4. Semana epidemiológica - Forma de relato padrão para alguns dados epidemiológicos.     
> Por convenção internacional as semanas epidemiológicas são contadas de domingo a sábado. A primeira semana do ano é aquela que contém o maior número de dias de janeiro e a última a que contém o maior número de dias de dezembro. [Fonte](https://www.saude.go.gov.br/acesso-a-informacao/712-suvisa/vigil%C3%A2ncia-epidemiol%C3%B3gica/8412-calend%C3%A1rio-epidemiol%C3%B3gico) 

## Fonte dos dados

1. COVID-19 - Dados foram coletados da iniciativa [Brasil.io](https://brasil.io/dataset/covid19/), e o nome das bases selecionadas são `caso.csv` e `caso_full.csv`;
2. Dados de gripes e Síndrome Respiratória Aguda Grave (SRAG) - foram coletados da iniciativa [InfoGripe](http://info.gripe.fiocruz.br/) da FIOCRUZ, mais especificamente a base `serie_temporal_com_estimativas_recentes_sem_filtro_febre.csv`*;
*** 
***Obs**: a base de dados completa contém um grande número de entradas, considerando diversos níveis de registros. Para utilizar no meu projeto, processei a base previamente, extraíndo dados mais gerais, a nível de: país, casos, ambos os sexos e etc. Informações completas de como eu fiz essa filtragem podem ser encontradas [aqui](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_01/dataset_gripe.ipynb). <BR>
**Obs2**: O banco de dados da inciativa Brasil.io continha informações incompletas para as últimas datas disponíveis (no momento que fiz o download), assim alguns gráficos trarão uma queda brusca nos índices nessas datas.
> [Com dados incompletos há 5 dias, Brasil registra 264 mortes por Covid-19](https://oglobo.globo.com/sociedade/com-dados-incompletos-ha-5-dias-brasil-registra-264-mortes-por-covid-19-24737450) (publicada em de 9 de novembro).
