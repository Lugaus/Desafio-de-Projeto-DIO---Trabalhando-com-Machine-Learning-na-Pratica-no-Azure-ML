# Trabalhando com Machine Learning-na Pratica no Azure ML



## Criando um Modelo de Previsão

### Acessando o Azure Machine Learning

- Acesse a página do Azure em [https://ml.azure.com](https://ml.azure.com).
- Na direção padrão, crie um novo Workspace.
- Dentro do Workspace, clique em "ML Automatizado" e selecione "Novo trabalho de ML automatizado".

### Configurações Básicas

- Edite o nome do trabalho e do experimento.
  - Nome do trabalho: mslearn-bike-automl2
  - Novo nome do experimento: mslearn_bike_rental
  - Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas.
- Avance para a próxima etapa.

### Tipo de Tarefa e Dados

- Selecione o tipo de tarefa, no caso, "Regressão".
- Crie um novo conjunto de dados.
  - Tipo: Tabular
  - Fonte: De arquivos da WEB
  - Insira a URL dos dados.
- Configure os detalhes do conjunto de dados e avance.

### Configuração de Tarefas

- Defina a coluna de destino como "Rentals (Integer)".
- Escolha as métricas e modelos permitidos.
- Configure os limites e a validação.
- Avance para a configuração de computação e prossiga.



### Análise e Teste do Modelo

- Em "Pontos de Extremidade", teste o modelo com o seguinte código:

*Input*
{
  "input_data": {
    "data": [
 {
      "day": 1,
      "mnth": 2,
      "year": 2024,
      "season": 1,
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
*jsonOutput*
[
  223.00077924442866
]
---

Esta apresentação abrange os passos para criar um modelo de previsão no Azure Machine Learning, bem como uma prática inicial realizada na plataforma.
Segue em anexo arquivos referentes a:
- Teste de ponto de extremidade
- Arquivo JSON bruto da aplicação
- Arquivo JSON do teste de ponto de extremidade
