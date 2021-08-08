# Malha aeria brasileira
Este repositório contém registro de voôs realizado no Brasil nos anos de 2020 e 2021, os dados foram retirados do site da ANAC (Agência Nacional de Aviação Civil - National Civil Aviation Agency), temos ainda uma comparação entre as malhas dos anos citados anteriomente através de métricas. 

## Datasets
O conjunto de dado utilizados está em resumo_anual_2020.csv e resumo_anual_2021.csv.
Em PDF1.csv estãos os valores das métricas que foram utilizados para gerar o Centrality Distributions .....
Os datasets utilizados foram baixados do site: https://www.gov.br/anac/pt-br/assuntos/dados-e-estatisticas/dados-estatisticos.

## Métricas
Diameter: Diâmentro da rede.
Center: Conjunto de todos os nós em uma rede cujo a eccentricity é igual ao raio da rede.
Closeness Centrality: Distância média entre os vértices.
Eigenvector Centrality: Importância baseada na importância dos nós vizinhos.
Centrality Distributions: 

## Generate
In your environment:

```shell
# Install requirements for scripts
pip install -r requirements.txt

# Download csv files from sources
python3 extract.py

# Transform to final files
python3 transform_to_anac_csv.py
python3 transform_to_airports_csv.py
python3 transform_to_graphml.py
```

## Contributing
Contributions are more than welcome. Fork, improve and make a pull request. For bugs, ideas for improvement or other, please create an [issue](https://github.com/alvarofpp/dataset-flights-brazil/issues).

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
