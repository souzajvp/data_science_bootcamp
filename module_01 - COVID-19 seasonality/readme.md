
![img](https://raw.githubusercontent.com/souzajvp/data_science_bootcamp/main/modulo_01/projeto%201.png)

## Warning:
This project was carried out at the beginning of November 2020. Since then, we know that the situation of COVID-19 has seriously worsened in the world, especially in Brazil.

# What is this project about??

My objective was to evaluate the distribution of COVID-19 cases and compare them with the distribution of cases of Severe Acute Respiratory Syndrome (SARS), caused by several respiratory viruses. Thus, evaluating the behavior of these two manifestations and causative agents, with the intention of raising awareness for the future of the COVID-19 pandemic in Brazil.

** Definition of some terms **:
1. Severe Acute Respiratory Syndrome (SARS) - severe respiratory complication that can be caused by several respiratory viruses (Influenza, Parainfluenza, SARS-CoV, etc.);
2. COVID-19 - disease caused by SARS-CoV-2, pandemic 2020;
3. SARS - disease caused by SARS-CoV, registered in the years 2002 and 2003.
<br> **Important**: The term SARS in English is equivalent to the translation of the term SRAG. In this notebook, the terms SARS and SRAG will be used with different meanings, mentioned in items 1 and 2.
4. Epidemiological week - Standard reporting form for some epidemiological data.
> By international convention, epidemiological weeks are counted from Sunday to Saturday. The first week of the year is the one that contains the greatest number of days in January and the last one that contains the greatest number of days in December. [Source (PT-BR)](https://www.saude.go.gov.br/acesso-a-informacao/712-suvisa/vigil%C3%A2ncia-epidemiol%C3%B3gica/8412-calend%C3%A1rio-epidemiol%C3%B3gico) 

## Data sources

1. COVID-19 - Data were collected from the [Brasil.io](https://brasil.io/dataset/covid19/) initiative(referent to early November 2020), and the names of the selected databases are `caso.csv` and` caso_full.csv`;
2. Data on influenza and Severe Acute Respiratory Syndrome (SRAG) - were collected from the [InfoGripe](http://info.gripe.fiocruz.br/) initiative of FIOCRUZ, more specifically the base `serie_temporal_com_estimativas_recentes_sem_filtro_febre.csv` *;
*** 
**Observation**: the complete database contains a large number of entries, considering different levels of records. To use in my project, I processed the database previously, extracting more general data, at the level of: country, cases, both sexes, etc. Complete information on how I did this filtering can be found [here (PT-BR)](https://github.com/souzajvp/data_science_bootcamp/blob/main/modulo_01/dataset_gripe.ipynb). <BR>
**Observation2**: The Brasil.io initiative's database contained incomplete information for the latest available dates (at the time I downloaded it), so some graphs will bring a sharp drop in the indexes on those dates.
> [With incomplete data for 5 days, Brazil registers 264 deaths by Covid-19 (PT-BR)](https://oglobo.globo.com/sociedade/com-dados-incompletos-ha-5-dias-brasil-registra-264-mortes-por-covid-19-24737450) (published on of November 9).
