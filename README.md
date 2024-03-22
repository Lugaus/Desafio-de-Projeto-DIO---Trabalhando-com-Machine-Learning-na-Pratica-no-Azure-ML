# Machine Learning na Prática com Azure ML

## Visão Geral do Projeto

Este projeto tem como objetivo fornecer uma introdução prática ao trabalho com Machine Learning utilizando o Azure Machine Learning. Abrangendo desde a criação de um modelo de previsão até a realização de testes de ponto de extremidade.

## Trabalhando com Machine Learning no Azure ML

### Criando um Modelo de Previsão

Para começar, siga os passos abaixo para criar um modelo de previsão no Azure Machine Learning:

1. Acesse a página do Azure em [https://ml.azure.com](https://ml.azure.com).
2. No diretório padrão, crie um novo Workspace.
3. Dentro do Workspace, clique em "ML Automatizado" e selecione "Novo trabalho de ML automatizado".

### Configurações Básicas

Na etapa de configurações básicas, personalize o nome do trabalho e do experimento de acordo com suas preferências:

- Nome do trabalho: mslearn-bike-automl2
- Novo nome do experimento: mslearn_bike_rental
- Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas.

### Tipo de Tarefa e Dados

Nesta etapa, selecione o tipo de tarefa como "Regressão" e configure o conjunto de dados:

- Tipo: Tabular
- Fonte: De arquivos da WEB
- Insira a URL dos dados.

### Configuração de Tarefas

Configure as métricas, modelos permitidos e limites para o experimento. Avance para a configuração de computação e prossiga.

### Análise e Teste do Modelo

Para testar o modelo, utilize o código abaixo:

**Entrada**
```json
{
  "input_data": {
    "data": [
      {
        "day": 1,
        "mnth": 1,
        "year": 2022,
        "season": 2,
        "holiday": 0,
        "weekday": 1,
        "workingday": 1,
        "weathersit": 2,
        "temp": 0.3,
        "atemp": 0.3,
        "hum": 0.3,
        "windspeed": 0.3
      }
    ]
  },
  "GlobalParameters": 1.0
}
```

**Saída**
```json
[
  223.00077924442866
]
```

## Arquivos Anexos

Este repositório inclui os seguintes arquivos:

- [application_JSON](application_JSON): Arquivo JSON bruto da aplicação.
- [extreme_point_JSON](extreme_point_JSON): Arquivo JSON do teste de ponto de extremidade.

---
