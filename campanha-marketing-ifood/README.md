# Análise da Campanha de Marketing do iFood

## 1. Problema de negócio

_(Descreva com as suas palavras o contexto: o time de marketing faz campanhas recorrentes e precisa entender quais perfis de clientes geram mais faturamento, para direcionar melhor as próximas ações.)_

**Pergunta aberta:** Como aumentar o resultado da próxima campanha de marketing?

**Pergunta fechada:** Quais são as características dos clientes que mais gastaram na campanha?

## 2. Premissas

- _(Período da campanha)_
- _(Tratamento de cupons)_
- _(Escopo de produtos considerados)_

## 3. Estratégia da solução (método Fato-Dimensão)

**Fato:** `Gasto-Clientes` (faturamento por cliente na campanha).

**Dimensões:**

| Dimensão | Atributos |
| -------- | --------- |
| Cliente | Salário, idade, faixa etária, estado civil, formação, crianças e adolescentes em casa, recência |
| Produto | Quantidade por categoria (vinhos, frutas, carnes, peixes, doces, premium) |
| Comportamento de compra | Total de compras, compras web, compras em loja, visitas ao site |
| Comportamento de marketing | Reclamações |

## 4. Hipóteses analíticas

| # | Hipótese | Priorizada? | Resultado |
| - | -------- | ----------- | --------- |
| 1 | _(ex.: clientes abaixo de 30 anos gastam mais)_ | | |
| 2 | _(ex.: clientes solteiros gastam menos)_ | | |
| 3 | _(ex.: clientes com filhos em casa compram mais)_ | | |

**Critérios de priorização:** dados disponíveis e insights acionáveis.

## 5. Insights

_(Insira aqui os gráficos da pasta `img/` e comente cada um.)_

## 6. Resultados e recomendações

_(Qual foi o melhor e o pior segmento? O que o marketing deve fazer na próxima campanha?)_

## 7. Próximos passos

- Explorar mais características dos clientes
- Automatizar a coleta e a análise
- Segmentar clientes em grupos (clusterização)
- Montar um dashboard de acompanhamento

## 8. Estrutura do projeto

```
campanha-marketing-ifood/
├── data/
│   ├── raw/          # dados originais (não alterar)
│   └── processed/    # dados tratados
├── notebooks/        # análises em Jupyter
├── img/              # gráficos usados no README
├── requirements.txt
└── README.md
```

## 9. Como reproduzir

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/
```

## 10. Dashboard

_(Cole aqui o link do Looker Studio, se for criar um.)_
