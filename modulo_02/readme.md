# Sobre o que é o meu projeto?

Meu objetivo é avaliar como anda a cobertura vacinal no Brasil, com foco especial na Febre Amarela (FA).
***

**Alvos de estudo**:
1. Cobertura vacinal geral por Unidade da Federação (UF) desde 1994 - Extraída do Tabnet e disponibilizada no meu [GitHub](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/cobertura_ano_geral.csv);
2. Cobertura vacinal de FA apor UF desde 1994 - Extraída do Tabnet e disponibilizada no meu [GitHub](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/cobertura-vacinal-FA-UF.csv);
3. Casos de FA registrado nas UFs de [2001 a 2006](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/FA_casos_2001_2006.csv) e [2007 a 2016](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/FA_casos_2007_2016.csv) - extraídas do Tabnet;
4. Casos e letalidade da FA no Brasil de [2001 a 2018](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/absoluto_2018.csv);
5. Cobertura vacinal de FA nos municípios de Minas Gerais desde 1994 - Extraída do TabNet e disponibilizada no meu [GitHub](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_02/mg_cobertura_vacinacao_fa.csv);
6. Lista de municípios de MG em estado de emergência para FA (MGEFA) durante o surto de FA em 2017.
>[Governo de Minas decreta situação de emergência em áreas com surto de febre amarela](https://g1.globo.com/minas-gerais/noticia/governo-de-minas-decreta-situacao-de-emergencia-em-areas-com-surto-de-febre-amarela.ghtml)
***
**Objetivos do projeto:**<br>
1. Conscientizar o leitor quanto à importância da vacinação;
2. Demonstrar o perigo que a queda na cobertura vacinal apresenta;
3. Avaliar se os municípios de MG em estado de emergência (MGEFA) durante o surto de 2017 apresentavam cobertura vacinal média menor que os outros;
4. Avaliar se os MGEFA retomaram a vacinação para os níveis recomendados.
5. Avaliar quantos municípios estão em risco para novos surtos em 2020.
*** 
**Definição de alguns termos**:
* Cobertura vacinal (%): porcentagem da meta de indivíduos a serem vacinados atingida no período;
* Epizootia: evento de morte de primatas não humanos. Importante fator de monitoramento para possíveis surtos de FA;

## Por quê estudar a FA? <br>
Apesar de ser uma doença controlada, surtos de FA em 2016, 2017 e 2018 mostraram como é necessário atenção à essa arbovirose. Adicionalmente, ao passo que a **cobertura vacinal para FA vem caindo**, o **desmatamento aumenta** radicalmente. Essas interações aumentam a chance de contato do ser humano com regiões em matas/florestas que tenham o mosquito infectado. <br>
Importante ainda é o fato que a FA pode ser transmitida pelo *Aedes aegypti*, vetor da Dengue, Zika, Chikungunya. Como sabemos, os casos de dengue continuam em alta e a grande concentração desse mosquito pode facilitar o surgimento de surtos de FA.

## Conclusões da análise

1. A **cobertura vacinal no Brasil vem caindo**, apesar de apresentar alguns picos recentes. Movimento antivacina, desinformação, posição das estratégias de saúde do Brasil são alguns dos possíveis motivos que explicam esse fenômeno; <br>
2. Para Febre Amarela, a situação não é diferente. Observamos quedas nas taxas de cobertura em todo o Brasil. **Quedas na cobertura em 2015 e 2016** foram seguidas por um  **surto importante de FA em 2017**. Só no estado de MG foram registrados <font color='red'> **1004 casos e 341 óbitos** </font> de 2016 a 2018;
> [Yellow fever in Africa and the Americas: a historical and epidemiological perspective](https://www.scielo.br/scielo.php?script=sci_arttext&pid=S1678-91992018000100207#B2)
3. Mesmo dentre os municípios de MG em estado de emergência durante o surto de FA em 2017, **apenas 44% destes regularizaram os esquemas vacinais** para o valor sugerido pelo Ministério da Saúde **até o ano de 2019**; 
4. Novamente observamos um **padrão similar ao de 2015-16**, com quedas na cobertura vacinal para **FA em 2019-20**. Isso indica um <font color='red'> **ponto de vulnerabilidade** </font> para futuros surtos no estado de MG!
<br>

Por fim, a vacina contra a COVID-19 está em alta como algo que pode nos salvar dessa pandemia. Porém, enquanto isso, negligenciamos diversas outras doenças sérias e que poderiam estar erradicadas (ou ao menos melhor controladas) como Sarampo, Poliomielite e Febre Amarela. <br>

## O que faltou no meu trabalho e perspectivas para continuidade!

1. Trabalhar mais a fundo com variáveis que podem ser <font color='red'> **indicadoras de vulnerabilidade para FA** </font> como: casos de epizootia, indices de desmatamento, prevalência de vetores (*Aedes*), estratégias de combate e conscientização da populção quanto a FA e talvez usar a incidência de dengue como modelo;

2. Buscar informações quanto a % de indivíduos vacinados em relação a população total;

3. Extrair o número de casos/óbitos por FA por UF dos boletins epidemiológicos, assim tendo **dados mais recentes**;

4. Determinar regiões em risco ao redor daquelas que foram afetadas pelo surto de acordo com os indicadores do item <font color='blue'> 1. </font>

## Descrição dos arquivos nesse repositório

| Nome do arquivo               | Descrição                                                                  | Fonte                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FA_casos_2001_2006.csv        | Casos de FA registrados entre 2001 e 2006 por UF                           | DataSus                                                                                                                                                                                                                    |
| FA_casos_2007_2016.csv        | Casos de FA registrados entre 2007 e 2016 por UF                           | DataSus                                                                                                                                                                                                                    |
| absoluto_2018.csv             | Casos e letalidade de FA a nível nacional entre 2001 e 2018                |                                                                                                                                                                                                                            |
| cobertura-vacinal-FA-UF.csv   | Cobertura vacinal para FA desde 1994 por UF                                | DataSus                                                                                                                                                                                                                    |
| cobertura_ano_geral.csv       | Cobertura vacinal média desde 1994 por UF                                  | DataSus                                                                                                                                                                                                                    |
| mg_cobertura_vacinacao_fa.csv | Cobertura vacinal para FA em MG desde 1994                                 | DataSus                                                                                                                                                                                                                    |
| mun_surto_2017_mg.csv         | Relação de municípios de MG em estado de emergência para FA em 2017        | [Governo de Minas decreta situação de emergência em áreas com surto de febre amarela](https://g1.globo.com/minas-gerais/noticia/governo-de-minas-decreta-situacao-de-emergencia-em-areas-com-surto-de-febre-amarela.ghtml) |
| geojs-31-mun.json             | Arquivo contendo coordenadas geográficas dos municípios de MG, processado. | [Geodata BR - Brasil](https://github.com/tbrugz/geodata-br)                                                                                                                                                                |
