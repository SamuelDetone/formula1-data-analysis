# Formula 1 Data Analysis - Exploratory Data Analysis

Projeto de analise exploratoria de dados com informacoes de stints, pneus, pit stops, clima e desempenho da Formula 1 entre 2018 e 2024.

## Objetivo

Investigar padroes de corrida na Formula 1 a partir de dados historicos, com foco em:

- duracao media de stints por composto de pneu;
- comportamento dos tempos de pit stop;
- identificacao de outliers em pit stops;
- relacao entre variaveis climaticas e desempenho operacional;
- comparacao de metricas de agressividade e desgaste de pneus.

## Dataset

Fonte informada no notebook original:

Kaggle - F1 Stint Data with Aggression Scores  
https://www.kaggle.com/datasets/akashrane2609/f1-stint-data-with-aggression-scores

O notebook inspecionado trabalha com dados de 2018 a 2024, contendo 7.374 linhas e 30 colunas.

## Ferramentas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab


## Competencias demonstradas

- Exploratory Data Analysis
- Data Cleaning
- Data Visualization
- Outlier Detection
- Descriptive Statistics
- Data Quality

## Etapas da analise

1. Carregamento e inspecao inicial dos dados.
2. Correcao de nomes de pilotos com problemas de codificacao.
3. Analise de estrutura, tipos de dados e estatisticas descritivas.
4. Identificacao de duplicadas, valores nulos e inconsistencias logicas.
5. Remocao de registros sem pit stop real.
6. Preenchimento de variaveis climaticas com mediana por corrida.
7. Deteccao de outliers em `Pit_Time` com intervalo interquartil.
8. Analise de correlacao entre variaveis numericas.
9. Visualizacoes sobre pneus, pit stops, temperatura e agressividade.

## Principais resultados observados

- O dataset original nao apresentou linhas duplicadas.
- Apos remover registros sem pit stop real, a base de analise ficou com 4.564 linhas.
- O metodo IQR marcou pit stops acima de 39,24s como outliers.
- Os maiores outliers de `Pit_Time` aparecem no British Grand Prix de 2022, evento marcado por bandeira vermelha.
- No recorte de `AvgPitStopTime` ate 120s, considerando um unico registro por piloto/corrida, a media foi 25,03s e a mediana 23,76s.
- Os compostos SUPERSOFT, ULTRASOFT e HARD apresentaram as maiores medias de voltas por stint no dataset analisado.

## Observacoes metodologicas

Este projeto e uma analise exploratoria. Portanto, correlacoes e linhas de tendencia devem ser interpretadas como associacoes observadas nos dados, nao como prova de causalidade.

Alguns graficos exigem revisao antes de uso em conclusoes finais. Em especial, a analise de podios deve contar combinacoes unicas de temporada, corrida, piloto e posicao, pois o dataset esta em nivel de stint e pode repetir pilotos na mesma corrida.

## Estrutura sugerida do repositorio

```text
f1-data-analysis/
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── f1_exploratory_data_analysis.ipynb
├── src/
│   ├── f1_analysis.py
├── images/
│   ├── stint_length_by_tire_compound.png
│   ├── avg_pit_stop_by_season.png
│   └── pit_stop_distribution.png
```

## Como executar

1. Baixe o dataset pelo link do Kaggle informado acima.
2. Coloque o arquivo em `data/`.
3. Instale as dependencias:

```bash
pip install -r requirements.txt
```

4. Execute o notebook em `notebooks/`.
