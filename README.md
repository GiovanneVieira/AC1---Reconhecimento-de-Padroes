# AC1 — Reconhecimento de Padrões: Regressão Linear do Crescimento de Milho 🌽

Atividade continua (AC1) da disciplina de **Reconhecimento de Padrões**: projeto de Machine Learning completo — da aquisição e pré-processamento dos dados ao treinamento de um modelo de **Regressão Linear Múltipla** e à avaliação/interpretação das métricas de desempenho.

## Dataset

[Corn Crop Growth (Kaggle)](https://www.kaggle.com/datasets/miguelh65/corn-crop-growth) — 1000 registros de sensores em plantação de milho, disponível em `data/crop_growth_dataset.csv`.

| Variável | Papel | Descrição |
|---|---|---|
| `Temperature` | Preditor (X) | Temperatura do ambiente |
| `Humidity` | Preditor (X) | Umidade do ar |
| `Soil_Moisture` | Preditor (X) | Umidade do solo |
| `Growth` | **Alvo (y)** | Crescimento da cultura |

## Etapas da atividade

| Etapa | Peso | Conteúdo |
|---|---|---|
| **Q1** — Aquisição e Pré-processamento | 30% | Carga (`pd.read_csv`), validação de schema (pandera), exploração (`info`/`describe`), ausentes/duplicados/outliers, seleção de `X` e `y` |
| **Q2** — Treinamento do Modelo | 30% | `train_test_split`, ajuste do `LinearRegression`, previsões e coeficientes |
| **Q3** — Avaliação e Interpretação | 40% | `r2_score`, MSE, RMSE, gráficos (dispersão, previsto vs. real, resíduos) e conclusões |

## Como rodar

O ambiente roda em Docker (imagem `jupyter/scipy-notebook`):

```bash
docker compose up
```

Acesse o JupyterLab em **http://localhost:8888** (token: `rec_padroes`) e abra `work/LinearRegressionCornGrowth-AC1.ipynb`. As dependências (`work/requirements`: pandas, numpy, scikit-learn, matplotlib, pandera) são instaladas pela primeira célula do notebook.

## Estrutura

```
.
├── README.md                        # este arquivo
├── docker-compose.yaml              # serviço Jupyter (work/ e data/ montados)
├── data/
│   └── crop_growth_dataset.csv      # dataset (Kaggle Corn Crop Growth)
└── work/
    ├── requirements                 # dependências Python
    └── LinearRegressionCornGrowth-AC1.ipynb   # notebook da AC1
```
