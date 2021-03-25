![img](https://raw.githubusercontent.com/souzajvp/data_science_bootcamp/main/modulo_04/Prancheta%202.png)

# Sobre o que é o meu projeto?
Meu objetivo é avaliar o comportamento da série temporal (ST) de casos de SRAG antes da COVID-19.

## Alvos de estudo:
1. Casos de SRAG (sem especificação do agente causador) de 2009 a 2019 - Extraídos do [OpenDataSus](https://opendatasus.saude.gov.br/dataset?tags=SRAG), processados na minha máquina e disponíveis após limpeza no meu [GitHub](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_04/srag2009-2019_limpocaso.csv).

## Objetivos do projeto:
1. Avaliar a **sazonalidade dos casos de SRAG no Brasil** de 2009 a 2019;
2. Entender o **impacto das pandemias de H1N1 (2009 e 2016) na sazonalidade** de SRAG em geral;
3. Avaliar a autocorrelação da série temporal (ST) em períodos atrasados (lags) e propor hipóteses para explicá-las;
4. Treinar modelos ARIMA e de ExponentialSmoothing para **prever o número de casos de SRAG em 2019**;
5. Usar o melhor modelo obtido para prever o **esperado de casos de SRAG para 2020**, em um **cenário sem COVID-19**;
***
**Definição de alguns termos**:
1. Síndrome Respiratória Aguda Grave (SRAG) - complicação respiratória grave que pode ser causada por vários vírus respiratórios (Influenza, Parainfluenza, SARS-CoV, etc);
2. COVID-19 - doença causada pelo vírus SARS-CoV-2, pandemia de 2020/21;
3. Influenza - vírus da gripe;
4. H1N1 - variante do vírus Influenza que causou a pandemia de gripe suína em 2009 e 2016. **Também responsável pela pandemia de 1918** (chamada de gripe espanhola).

## Conclusões e limitações do estudo
***
Neste projeto, pude [expandir o trabalho realizado no primeiro módulo do bootcamp](https://github.com/souzajvp/data_science_bootcamp/tree/main/modulo_01), onde comparei a sazonalidade de SRAG e COVID-19 (até novembro de 2020). Através das análises, fica clara a sazonalidade de casos de SRAG e como a auto-correlação nos permite entender a dinâmica desse tipo de manifestação, pelo menos pré-COVID-19. <br>
Apesar de eu não ter trabalhado diretamente com os casos de COVID-19, os resultados aqui permitem **algumas reflexões**:
1. A pandemia de COVID-19 continua, agora mais forte do que nunca. Considerando a sazonalidade clara de SRAG (causada por vírus respiratórios), é bem possível que efrentemos ondas e ondas de COVID-19 no futuro. *O que faremos como sociedade para sobreviver às próximas ondas?*;
2. Apesar de o número de casos emergenciais ou fatais de Influenza serem muito menores do que os de COVID-19, não podemos esquecer que isso só é possível graças a vacinação anual. Agora, *não podemos deixar de nos vacinarmos para COVID-19*;
3. O surgimento de próximas pandemias não é uma dúvida: é só questão de tempo. *Somente o investimento em ciência, saúde e educação pode nos preparar para futuros desafios*. Além disso, cooperações internacionais e senso de comunidade serão essenciais para a sobrevivência da humanidade!


***
Apesar de progredir com a análise, é necessário deixar evidente **as limitações encontradas**:
1. Decidi trabalhar com os casos de SRAG agrupados por mês de notificação. Provavelmente, modelos que sejam capazes de estimar com (*relativa*) precisão o **pico de casos por semana seriam mais úteis para planejamentos estratégicos** de saúde;
2. Com os testes feitos com as médias (2010-2019 ou 2018-2019), notei que o **uso de um modelo "sofisticado" nem sempre é necessário**. Para Influenza e SRAG, já temos conhecimento acumulado no mundo há décadas e um sistema de vigilância eficaz no Brasil há pelo menos 10 anos. Desta forma, sabemos que a sazonalidade e manifestação dessas infecções são bastante constantes (*sem contar com epidemias ou pandemias*). Finalmente, o **uso das médias + SD nos daria uma ótima ideia do que seria esperado para 2020**;
3. Os parâmetros que eu utilizei para treinar os modelos foram razoávelmente arbitrários. Por falta de conhecimento mais aprofundado na área, parte dos resultados foi obitida por testagem até chegar em algo que parecia justo. Nesse sentido, minha limitação teórica no assunto pode ter prejudicado o resultado do trabalho.

## Agradecimentos
Como sempre, agradeço à minha parceira [Letícia Murase](https://www.researchgate.net/profile/Leticia-Murase) pelas discussões sobre o projeto, paciência e também pela arte da capa. Além disso, agradeço ao amigo [Matheus](https://github.com/MatheusOrange211) pelas discussões e apoio!

## Descrição dos arquivos nesse repositório

| **Arquivo**                                              | **Descrição**                                                                          | **Fonte**                                                         |
|----------------------------------------------------------|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Projeto_final_módulo_04_João_Vítor_Perez_de_Souza_.ipynb | Python notebook contendo todas as análises e conclusões                                | Autoria própria                                                   |
| srag2009-2019_limpo.csv                                  | Arquivo .csv contendo todos os óbitos por SRAG de 2009 a 2019, após pré-processamento. | [OpenDatasus](https://opendatasus.saude.gov.br/dataset?tags=SRAG) |
| srag2009-2019_limpocaso.csv                              | Arquivo .csv contendo todos os casos de SRAG de 2009 a 2019, após pré-processamento.   | [OpenDatasus](https://opendatasus.saude.gov.br/dataset?tags=SRAG) |
| Prancheta 2..png                                         | Capa do projeto                                                                        | Autoria de Letícia Sayuri Murase                                  |
