# Projeto de Regressão Linear e Logística
Este repositório contém um projeto de análise estatística aplicado à modelagem de características morfológicas de gambás (possums). São apresentados modelos de regressão linear para prever o comprimento da cabeça e modelos de regressão logística para classificar o sexo (is_male) com base em diversas variáveis medidas.

## Visão Geral
O projeto foi dividido em duas partes principais:

## Regressão Linear:

Objetivo: Prever o comprimento da cabeça (hdlngth) utilizando variáveis morfológicas (por exemplo, skullw, totlngth, taill, footlgth, earconch, eye, chest, belly) e a variável categórica is_male (após transformação de 'sex' para 0 e 1).

### Abordagem:

- Análise exploratória (correlações, scatterplots, boxplots).

- Implementação de modelos com e sem interação.

- Seleção automática de variáveis usando o método backward elimination.

- Avaliação do modelo final por meio do Adjusted R², RMSE e análise de resíduos (histograma, QQ-plot e teste de Shapiro-Wilk).

## Regressão Logística:

Objetivo: Prever o gênero (is_male) a partir de variáveis morfológicas.

### Abordagem:

- Verificação do balanceamento das classes (58% machos e 42% fêmeas).

- Análise das correlações entre is_male e as variáveis preditoras.

- Criação de modelos logísticos, com testes de transformações (quadrado, raiz e log) e avaliação das métricas do modelo.

- Seleção das melhores variáveis (identificamos que hdlngth e totlngth eram as mais significativas) e comparação usando a métrica de pseudo R², log-likelihood e análise da matriz de confusão.

- Plot da curva ROC com cálculo de AUC para avaliar a performance preditiva do modelo.

## Principais Bibliotecas Utilizadas
- pandas e numpy para manipulação de dados

- seaborn e matplotlib para visualização

- statsmodels para implementação dos modelos de regressão (OLS e Logit)

- scipy.stats para testes estatísticos (ex.: Shapiro-Wilk)

- sklearn.metrics para calcular a curva ROC e AUC

## Instruções de Uso
1. Clonar o repositório:

```bash
git clone https://github.com/seu-usuario/seu-projeto.git
cd seu-projeto
```
2. Instalar as dependências:
Certifique-se de ter o Python 3 instalado. Em seguida, instale as bibliotecas necessárias:

```bash
pip install pandas numpy seaborn matplotlib statsmodels scipy scikit-learn
```

3. Executar o script principal:

```bash
python main.py
```

O script realizará:

Leitura e limpeza dos dados

Análise exploratória (correlações e gráficos)

Ajuste do modelo de regressão linear (com e sem interações)

Seleção de variáveis pelo método backward elimination

Avaliação do modelo final (Adjusted R², RMSE, gráficos de resíduos e testes de normalidade)

Ajuste do modelo de regressão logística e avaliação (coeficientes, pseudo R², matriz de confusão, curva ROC)

## Principais Resultados
#### Regressão Linear:

- O modelo final apresentou um Adjusted R² de aproximadamente 0.66 e um RMSE de 2.02.

- Os gráficos de resíduos (histograma, QQ-plot e teste de Shapiro-Wilk com p=0.542) indicam que os resíduos estão normalmente distribuídos.

#### Regressão Logística:

- O modelo logístico com as variáveis hdlngth e totlngth mostrou coeficientes significativos e um pseudo R² (McFadden) de aproximadamente 0.08.

- A análise da matriz de confusão, curvas ROC e AUC permitiu avaliar a performance preditiva do modelo.
