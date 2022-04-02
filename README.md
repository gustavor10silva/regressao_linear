# regressao_linear
Este repositório armazena um notebook sobre Regressão Linear.

Essa é a fórmula geral da regressão linear:

$$\hat{y} = \theta_0 + \theta_1x_1 + \theta_2x_2 + \ldots + \theta_nx_n$$

Queremos aproximar o valor de $y$ com a expressão à direita, onde:

* $\hat{y}$ é o valor predito
* $n$ é o número de variáveis preditoras
* $x_i$ é o valor da i-ésima variável
* $\theta_j$ é o j-ésimo parâmetro do modelo ($\theta_0$ é chamado de **viés** (bias), e os demais são chamados de **pesos** das variáveis)

* **Observação:** na equação acima, se $n=1$, temos uma **regressão linear simples**; caso $n>1$, temos uma **regressão linear múltipla**.

Note que a equação acima pode ser reescrita na forma matricial:

$$\hat{y} = h_\theta(x) = \theta^T \cdot x$$

Onde:

* $\theta$ é o vetor de parâmetros: $\theta = [\theta_0, \theta_1, \theta_2, \ldots, \theta_n]$
* $x$ é o vetor das variáveis preditoras: $x = [1, x_1, x_2, \ldots, x_n]$
* $\theta \cdot x$ é o produto vetorial dos vetores $\theta$ e $x$: $\theta \cdot x = \theta_0 + \theta_1x_1 + \theta_2x_2 + \ldots + \theta_nx_n$

Seja $y$ o vetor de rótulos reais. Estamos aproximando $y$ por $\hat{y}$, então estamos cometendo um erro $|\hat{y}_i - y_i| = |\theta^Tx_i - y_i|$. Tecnicamente, o que queremos com a regressão linear é minimizar esse erro, o que é o mesmo que minimizar o MSE (Mean Squared Error, ou Erro Quadrático Médio):

$$MSE(X, h_\theta) = \dfrac{1}{m}\sum_{i=1}^n\left(\theta^Tx_i - y_i\right)^2$$
