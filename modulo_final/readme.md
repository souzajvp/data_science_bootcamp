![img](https://raw.githubusercontent.com/souzajvp/data_science_bootcamp/main/modulo_final/Prancheta%205.png)

**Alvo de estudo**:
O banco de dados utilizado para este projeto está depositado no Kaggle, e é aberto para todos.
* [Dataset Kaggle](https://www.kaggle.com/S%C3%ADrio-Libanes/covid19)

## Problema
Classificar os pacientes internados com COVID-19 no hospital Sírio Libanês (Brasília-DF e São Paulo-SP) de acordo com a necessidade ou não as instalações das Unidades de Terapia Intensiva (UTIs). <br>

### Objetivos/Tarefas:
1. Prever quais pacientes necessitarão de UTI;
2. Prever quais pacientes NÃO necessitarão de UTI.

### Variável de interesse e Janela: 
* UTI ou não - `ICU` - (0,1);
* Janela de tempo - `WINDOW` - ['0-2', '2-4', '6-12', 'Above-12');
    
### Critérios obrigatórios
Não se pode utilizar os dados quando o paciente deu entrada na UTI -> `ICU = 1`
    
### Aspectos dos dados
Os dados foram **anonimizados e escalados** para manterem-se entre 0 e 1 de acordo com valores máximos e mínimos;

### Entendendo as variáveis disponíveis:
***
* Informações demgráficas (03);
* Agrupamento de doenças (09);
* Resultados de exames de sangue (36);
* Sinais vitais (06). <br>

Diversas variáveis foram expandidas para versões `média`, `mediana`, `máximo`, `mínimo`, `diff` e `diff relativo`.
* diff = `valor máximo` - `valor mínimo`;
* diff relativo = `diff` / `mediana`

### Entendendo a estrutura dos dados:
***
Neste desafio, temos dados de pacientes positivos para COVID-19 internados no Hospital Sírio Libânes de São Paulo-SP e Brasília-DF. De forma geral, temos até 5 entradas que representam dados de um mesmo paciente. Essas entradas são referentes à diferentes janelas de tempo (`0-2, 2-4, 4-6, 6-12, >12`) em que os pacientes foram acompanhados. Para cada uma das janelas, foram dosados diversos marcadores biológicos e sinais vitais. <br>
Resumidamente, a estrutura do banco é a seguinte:

**Tabela 1. Estrutura de repetição dos dados no banco usado no desafio.**

| **Paciente** | **Janela** | **Exame_1** | **Exame_2** | ... | **UTI** |
|:------------:|:----------:|:-----------:|:-----------:|-----|:-------:|
|       A      |     0-2    |      1      |      4      | ... |    0    |
|       A      |     2-4    |      1      |     3.5     | ... |    0    |
|       A      |     4-6    |     1,1     |     3.7     | ... |    0    |
|       A      |    6-12    |     1,2     |     3.8     | ... |    0    |
|       A      |     >12    |     1,3     |     4.1     | ... |  **1**  |
|              |            |             |             |     |         |
|       B      |     0-2    |      2      |      2      | ... |    0    |
|       B      |     2-4    |     1,9     |     2.5     | ... |  **1**  |



Essa estrutura de repetição para cada paciente representa um problema de **medições repetidas** (do inglês *multiple measures* ou *repeated measures*), que é comum para bancos ou estudos na área da saúde. Nesse tipo de dados temos uma dependência entre as amostras de cada paciente. Ou seja, os dados da janela `2-4` do paciente A são muito dependentes dos dados da janela anterior (`0-2`) desse mesmo paciente A. <br>
Em situações assim, podem ser empregados **modelos lineares mistos** ou **modelos para análise de sobrevivência que consideram esse agrupamento dos pacientes**:
* >[Introduction to linear mixed models](https://ourcodingclub.github.io/tutorials/mixed-models/#what);
* >[Piecewise exponential models and creating custom models](https://lifelines.readthedocs.io/en/latest/jupyter_notebooks/Piecewise%20Exponential%20Models%20and%20Creating%20Custom%20Models.html);
* >[How Linear Mixed Model Works](https://towardsdatascience.com/how-linear-mixed-model-works-350950a82911);
* > [Comparing common analysis strategies for repeated measures data](https://eshinjolly.com/2019/02/18/rep_measures/).

Apesar de entender que esses modelos seriam úteis, a complexidade dos nossos dados e desses modelos mais refinados me impediu de seguir com a implementação e testes. Desta forma segui com uma abordagem mais "convencional".
***
Deste modo, percebemos que  **escolha da conduta para trabalhar com os dados não é trivial**.
