# Análise da Campanha de Marketing do iFood

Projeto de análise de dados desenvolvido com **Excel** (tratamento e exploração da base) e **Looker Studio** (dashboard e visualizações).

# Problema de negócio

O iFood é o maior aplicativo de delivery de comida do Brasil e está presente em mais de mil cidades. Manter os clientes engajados é essencial para o crescimento da empresa e para que ela continue na liderança do mercado.

Neste projeto, simulei o trabalho de uma pessoa analista de dados dentro dessa empresa. Recebi uma base de amostra com informações dos clientes e de como eles reagiram a uma campanha de marketing. O desafio era entender os dados, enxergar oportunidades de negócio e sugerir ações baseadas em dados para melhorar os resultados das próximas campanhas.

**Meu objetivo:** fazer uma análise descritiva do comportamento dos clientes para descobrir quais características estão associadas a um maior gasto, ajudando a empresa a lucrar mais na próxima campanha.

# Contexto

O time de marketing do iFood faz campanhas com frequência para aumentar o faturamento. Mas, para isso funcionar bem, é preciso entender quais ações deram resultado e quais não deram, de modo a repetir o que funcionou e corrigir o que não funcionou.

É nesse ponto que a análise de dados entra: coletar as informações, analisá-las e transformá-las em insights que o time de negócio consiga usar.

# Premissas da análise

1. A campanha analisada aconteceu entre **15 e 30 de janeiro de 2025**.
2. Todas as compras feitas com cupom foram **removidas** da base.
3. Foram considerados apenas os **produtos do catálogo da campanha**.

# Estratégia da solução

Para organizar o raciocínio, usei o método **Fato-Dimensão**: primeiro defino o que quero medir (o fato) e depois as características que ajudam a explicar essa medida (as dimensões).

## Passo 1: Resumir o contexto em uma pergunta aberta

Uma pergunta aberta é uma demanda ampla, com várias soluções possíveis. Cabe a quem analisa avaliar as alternativas e escolher a que traz mais retorno com menos esforço. A pergunta definida foi:

**Como aumentar o resultado da próxima campanha de marketing?**

## Passo 2: Transformar a pergunta aberta em fechada

Uma pergunta fechada é objetiva e já indica exatamente o que precisa ser analisado, normalmente escolhendo um caminho entre todos os possíveis. A pergunta fechada definida foi:

**Quais são as características dos clientes que mais gastaram na campanha de marketing?**

## Passo 3: Definir a coluna fato

O fato é a coluna que está no centro da análise. Aqui, é a coluna **Gasto-Clientes**, que mostra quanto cada cliente gastou durante a campanha. Ela foi escolhida porque o problema de negócio é aumentar o faturamento.

## Passo 4: Identificar as dimensões

Agrupei as colunas da base em quatro dimensões, que trazem mais detalhes sobre o fato:

| Dimensão | Colunas |
| -------- | ------- |
| **Cliente** | Salário, Idade, Faixa-Etária, Dias-Cliente, Estado-Civil, Formação, Crianças-Casa, Adolescentes-Casa, Recência |
| **Produto** | Qtde-Vinhos, Qtde-Frutas, Qtde-Carnes, Qtde-Peixes, Qtde-Doces, Qtde-Premium |
| **Comportamento de compra** | Qtde-Compras, Qtde-Compras-Web, Qtde-Compras-Loja, Visitas-Site-Mes |
| **Comportamento de marketing** | Reclamações |

## Passo 5: Hipóteses analíticas

Cada hipótese junta o **fato** (gasto) com uma **dimensão** e uma **comparação** (maior, menor ou igual).

**Cliente – Idade**
1. Clientes com menos de 30 anos gastam mais do que as outras faixas etárias.
2. Clientes entre 20 e 30 anos gastam mais do que as outras faixas etárias.
3. Clientes com mais de 30 anos gastam mais do que as outras faixas etárias.

**Cliente – Estado civil**

4. Clientes solteiros gastam mais do que os outros grupos.
5. Clientes solteiros gastam menos do que os outros grupos.
6. Clientes casados gastam mais do que os outros grupos.

**Cliente – Estado civil + Idade**

7. Clientes solteiros com mais de 30 anos gastam mais do que clientes casados da mesma faixa de idade.

**Cliente – Formação**

8. Clientes com formação avançada (doutorado) gastam mais do que clientes com ensino fundamental.
9. Clientes com salários maiores têm maior nível de escolaridade.

## Passo 6: Critérios de priorização

Para decidir quais hipóteses analisar primeiro, usei dois critérios:

- **Dados disponíveis:** a base precisa ter as informações necessárias para testar a hipótese.
- **Insight acionável:** o resultado precisa permitir uma ação concreta do marketing.

## Passo 7: Hipóteses priorizadas

1. Clientes com menos de 30 anos gastam mais com produtos do iFood do que as outras faixas etárias.
2. Clientes solteiros gastam menos do que os outros grupos.
3. Clientes solteiros com menos de 30 anos gastam mais do que as outras faixas etárias.
4. Clientes com crianças em casa compram mais pelo iFood.
5. Clientes que compram mais carne também compram mais vinho.


### Visão geral da campanha
Panorama do faturamento e do desempenho geral da campanha.

### Visão dos clientes
Como o gasto varia de acordo com idade, estado civil, formação e composição familiar.

### Conclusão: resultado por cliente
Cruzamento das características que formam os melhores e os piores segmentos.

### Conclusão: visão por produto
Quais categorias de produto mais contribuíram para o faturamento.

# Resultados

**Melhor segmento:** clientes casados, com idade entre 41 e 50 anos, sem filhos em casa e com graduação completa.

**Piores segmentos:** clientes viúvos de todas as faixas etárias, além de clientes com menos de 30 anos (de qualquer estado civil) que têm duas ou mais crianças em casa e apenas o ensino fundamental.

**Recomendação:** para aumentar o lucro da próxima campanha, o marketing deve direcionar as ações para o melhor segmento e reduzir o investimento nos demais, principalmente nos de pior desempenho.

# Ferramentas utilizadas

- **Excel:** limpeza, organização e exploração inicial dos dados.
- **Looker Studio:** construção do dashboard com as visões geral, de clientes e de produto.

# Dashboard completo

<!-- Cole aqui o link do seu dashboard no Looker Studio -->

# Próximos passos

1. Explorar outras características dos clientes.
2. Automatizar a coleta e a análise para acompanhamento contínuo.
