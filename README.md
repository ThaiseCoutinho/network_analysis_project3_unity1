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


Core Decomposition: Possibilita encontrar o núcleo do grafo, ou seja, os nós que possuem maiores quantidades de conexões com os demais nós do grafo.



## Grafo da rede
Como os valores dos datasets utilizados são muito próximos o grafo abaixo se refere as malhas de ambas as redes.
![3](https://user-images.githubusercontent.com/41967839/128645330-9a07c46a-7fa0-406f-86ca-77bd9fe079f4.png)



## Comparativo

Diameter: Antes de saber o diâmentro de uma rede propriamente dito, se faz necessário conhencer sua eccentricity (excentricidade) que se refere basicamente a distância máxima de um referido nó aos demais nós da rede, assim sendo o diâmetro é o maior valor (valor máximo) da excentricidade presente na rede. A malha da rede referente ao resumo anual dos vôos em 2020 possui cento e oito (108) nós com excentricidade máxima de seis (6), ou seja o valor do diâmetro nessa rede é seis (6). A malha de rede do resumo anual de 2021 possui cento e oito nós, com excentricidade máxima seis, dessa forma percebe-se que não houve mundança significativa nas malhas de rede dos anos analisados.


Center: Como mencionado anteriormente o valor referente ao center é o conjunto de valores presente na rede cuja a excentricidade é igual valor do raio, vale salientar que o valor do raio em uma rede será sempre o valor mínimo da excentricidade. Na malha de rede do resumo anual dos vôos em 2020 o valor do centro é três (3). Na malha que se refere ao resumo anual dos vôos em 2021 temos que o valor atribuído ao center é igual ao do ano anterior, não havendo alterações nesta métrica.


Closeness Centrality: O objetivo dessa métrica é descobrir a distância média de um determinado nó aos demais nós da rede considerando sempre o menor caminho, dessa forma quanto menor o valor do closeness centrality atribuído a um dado, menor serar sua distância média aos nós da rede. Na malha da rede do resumo anual dos vôos em 2020 o menor valor do closeness centrality é igual à 0.24429223744292236. O valor do closeness centrality do resumo anual de 2021 é igual a 0.24429223744292236, assim como o valor referente ao ano anterior.


Eigenvector Centrality: Essa métrica diz a importância de um determinado nó aos demais nós da rede, levando em consideração a importância dos nós vizinhos. Quanto maior for o valor atribuido a um nó, maior será sua importância na rede. Assim o maior valor atribuido a um nóno resumo anual dos vôos em 2020 é igual a 0.3927799650843763. Assim como nas métricas anteriores, também não houve alteração no valor do eigenvector centrality para o resumo anual dos vôos no ano de 2021, sendo este igual ao do ano anterior.


Centrality Distributions: Uma das estratégias que se pode usar ao analise de diferentes redes é a comparação das métricas par a par, na imagem abaixo temos uma comparação das métricas closeness centrality e eigenvector centrality, na diagonal principal temos a PDF das nossas variáveis (métricas), essa distribuição de probalidade possui uma assimetria positiva, no primeiro gráfico podemos observar uma alta quantidade de nós com um valor baixo de eigenvector, ou seja muitos nós na rede possuem uma baixa importância, enquanto que uma menor quantidade de nós são realmente impotantes na rede. No triângulo superior temos um gráfico de dispersão, onde percebemos que mesmo os nós de maior importância possuem uma distância média pequena. No triângulo inferior temos  e uma versão do KDE (kernel density estimation) multivariável, neste é possível notar que temos uma aglomerado de nós onde a distância média é baixa e a importância dos nós também é pequena assim como o gráfico analisado anteriormente percebe-se que mesmo a importância de alguns nós aumentando a distância média ainda continua baixa. Essa análise foi utilizada para os gráficos de ambas as malhas de rede (2020 e 2021), visto que os valores das métricas não sofreram alterações. 


![1](https://user-images.githubusercontent.com/41967839/128634008-0b57833b-1ecf-4b20-9fe0-77284c9f7d3f.png)



Core Decomposition: O Core Decomposition é semelhante a encontrar o núcleo do planeta terra uma vez que a mesma é subdividida em camadas. Usar esta métrica consiste em dividir o grafo de acordo com o grau de cada nó, ou seja, a quantidade de conexões que possibilita sair de um nó para outro, quando o k=1, temos todos os nós do grafo pois até o que não se liga a nenhum outro nó é apresentado no grafo, quando partimos para o segundo core, k=2, os nós que estão conectados a apenas um outro nó são excluídos do grafo e assim por diante até chegar nos nós centrais, ou seja, os que possuem o máximo de conexões.
![WhatsApp Image 2021-08-08 at 19 19 48](https://user-images.githubusercontent.com/41967839/128647387-836c0356-606c-4a66-861e-92da665af159.jpeg)


No nosso caso, foram gerados 9 núcleos, ou seja, os nós do núcleo da rede se ligam com até outros 9 nós. 
![WhatsApp Image 2021-08-08 at 19 19 47](https://user-images.githubusercontent.com/41967839/128647395-67a9a962-b119-4f58-96ed-dcdc40b0ec0a.jpeg)


Na imagem acima, temos os nós mais externos, em azul, que se ligam a, pelo menos, um outro nó do grafo e que são excluídos quando avança para a camada de k=2. Essa análise foi feita para ambas as malhas de rede (2020 e 2021), pois apresentam os mesmo resultados. 



Conlusão:
A partir da análise dos resultados obtidos conclui-se que não houve alterações nas malhas aéreas dos anos de 2020 e 2021, podemos atribuí isso ao estado de pademia que o país vem enfrentado no decorrer deste dois anos. 
