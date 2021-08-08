# Malha aérea brasileira
Este repositório contém registro de voôs realizado no Brasil nos anos de 2020 e 2021, os dados foram retirados do site da ANAC (Agência Nacional de Aviação Civil - National Civil Aviation Agency), temos ainda um comparativo entre as malhas dos anos citados anteriomente através de métricas. 

## Datasets
O conjunto de dado utilizados está em resumo_anual_2020.csv e resumo_anual_2021.csv.
Em PDF1.csv estãos os valores das métricas que foram utilizados para gerar a PDF (Probability Density Function) e analisar os dados de maior complexidade. 
Os datasets utilizados foram baixados do site: https://www.gov.br/anac/pt-br/assuntos/dados-e-estatisticas/dados-estatisticos.

## Métricas
Diameter: Diâmentro da rede.


Center: Conjunto de todos os nós em uma rede cujo a eccentricity é igual ao raio da rede.


Closeness Centrality: Distância média entre os vértices.


Eigenvector Centrality: Importância de um dado nó baseada na importância dos nós vizinhos.


Centrality Distributions: Distribuição de centralidade, nesse caso foi utilizado a PDF(Probability Density Function) ou Função Densidade de Probabilidade para realizar uma análise mais complexa dos dados.


Core Decomposition:



## Comparativo

Diameter: Antes de saber o diâmentro de uma rede propriamente dito, se faz necessário conhencer sua eccentricity (excentricidade) que se refere basicamente a distância máxima de um referido nó aos demais nós da rede, assim sendo o diâmetro é o maior valor (valor máximo) da excentricidade presente na rede. A malha da rede referente ao resumo anual dos vôos em 2020 possuí cento e oito (108) nós com excentricidade máxima de seis (6), ou seja o valor do diâmetro nessa rede é seis (6).
Já ....


Center: Como mencionado anteriormente o valor referente ao center é o conjunto de valores presente na rede cuja a excentricidade é igual valor do raio, vale salientar que o valor do raio em uma rede será sempre o valor mínimo da excentricidade. Na malha de rede do resumo anual dos vôos em 2020 o valor do centro é três (3). Na malha que se refere ao resumo anual dos vôos em 2021...


Closeness Centrality: O objetivo dessa métrica é descobrir a distância média de um determinado nó aos demais nós da rede considerando sempre o menor caminho, dessa forma quanto menor o valor do closeness centrality atribuído a um dado, menor serar sua distância média aos nós da rede. Na malha da rede do resumo anual dos vôos em 2020 o menor valor do closeness centrality é igual à 0.24429223744292236.


Eigenvector Centrality: Essa métrica diz a importância de um determinado nó aos demais nós da rede, levando em consideração a importância dos nós vizinhos. Quanto maior for o valor atribuido a um nó, maior será sua importância na rede. Assim o maior valor atribuido a um nóno resumo anual dos vôos em 2020 é igual a 0.3927799650843763.


Centrality Distributions: 
Na imagem a seguir temos.... 2020

![1](https://user-images.githubusercontent.com/41967839/128634008-0b57833b-1ecf-4b20-9fe0-77284c9f7d3f.png)

2021
![2](https://user-images.githubusercontent.com/41967839/128640301-e690de38-06b0-489c-bedb-c3776225c38d.png)



Core Decomposition:
